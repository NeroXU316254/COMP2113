# COMP2113 Project of Group 12
## —— An April Day in Hong Kong



## **Outline**
* [Game Introduction](#game-introduction)
  - Background
  - Game Rule
* [Coding Requirements](#coding-requirements)
  - Program Working Flow
  - Functions may Used 
* [Group Introduction](#group-introduction)
  - XU Shuoyuan
  - Guo Qianni



## Game Introduction

 - Background

It should have been a usual April day, but nobody hangs out on the streets of Hong Kong. Your alarm clock goes off in the morning, while the news is continually reporting the increasing number of people infected by COVID-19. You start to realize that today is an unusual April day in Hong Kong. During the period of Coronavirus Disease in the Spring of 2020, you still have to hold on and finish all your daily affairs. **KEEP HEALTHY, AND FINISH YOUR DAY!**
 
 - Game Rule

In this text-based game, you will act as an ordinary person in Hong Kong. With a set of daily affairs given to you, you need to choose your paths/actions/behaviors step-by-step to complete all the assignments on this day of the special period. 

We would design a comprehensive picture with a variety of scenes in your living area. And you bear the risk of approaching COVID-19 carriers and even infected people on your way to different places. If you are infected halfway, you will be immediately announced to fail this game. The original probability of getting infected of selecting each path/action/behavior is pre-dertermined, but you can choose to wear preventional items (e.g. masks, gloves, glasses) to reduce the probability of getting infected. But remember the number of available items is limited. After each selecting and item chosen, a random number between (0,1) will be generated to decide whether you get infected based on the new probability.

So you win this game if and only if you've completed all the assignments and go back home successfully without being infected. **STAY HEALTHY AND WORK EFFICIENTLY!**


## Coding Requirements

 - Program Working Flow

![](https://github.com/NeroXU316254/NeroXU/blob/master/Flow%20Chart.png)

 - Functions may Used 
   
     The functions listed below are designed in the game. In further programming, more functions may be needed but these below are the basis. Names of the functions may change.
   
   * **In Me file**
   
     This file is designed to store the basic information from the player, including **Namegiving**, **Eventselction**, **Save**, **Load**, **Itemlist** and so on. 

    1. Function **Namegiving** is to indentify different records, which is the name of the character in the game. 

    2. Function **Eventselction** is the main part--the process of the game. This gives a random number to flag the events/assignments and behavior selections that this record will include among the various events, connecting Me file with Events files. 

    3. Function **Save** is to write the new GameStatus in Me file. 

    4. Function **Load** is to read the record in Me file. 

    5. Function **Itemlist** is the list of the items used after the past events, connecting Me file with Events files. This can write the active status of the items in Item file. 
   
   * **In Events files**

     These files are designed to store the events and behavior selctions in this games. The functions included are similar. 

    1. Function **EventFlag** is to change the status of the event/assignment. The initial statuses of all the events/assignments are "Not happen". After **Eventselction** in Me file executed, **EventFlag** will change the status of relevant events/assignments to "Happen". 

    2. Function **Hidenchoose** is to give hidden behavior selections if some items are checked as used items.
   
   * **In Item file**
   
     This file includes all the preventional items in this game. 
     
    1. Function **ItemFlag** is to change the status of the event. The initial status of all the items is "Not used". After a certain behavior selection or events happened, **ItemFlag** will change the status of relevant items to "used".
     
    2. Function **ShowinList** is to display all the used items in Itemlist of the records in Me file. 
    
    
 - Code Requirement Satisfied
    
      The functions listed below are examples. At least one function are satisfied relevant requirements.
    
    1. Generation of random game sets or events
    
       **Eventselction** : give random options for players to have diverse experiences.
    
    2. Data structures for storing game status
    
       **EventFlag** and **ItemFlag** : use flags to clarify the status of the sections.
    
    3. Dynamic memory management
      
       **Save** and **Load** : use records to save or load different game status.
    
    4. File input/output (e.g., for loading/saving game status)
    
       **Save** and **Load** : use records to save or load different game status.
    
    5. Program codes in multiple files
    
       **Eventselction** and **Hidenchoose** : need to check the status of revelant sections in multiple files.
    
    6. Proper indentation and naming styles
    
       **Namegiving** : indentify different records.
    
    7. In-code documentation
    
       **EventFlag** and **ItemFlag** : read and write across files.
  


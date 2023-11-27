# Initial Design Document:

**Title:** Jersey Collection Catalog System

**Student:** Mitchell Zeleny

**Course:** COSC 2436 Fall 23

## Introduction:

This is a Jersey Collection Catalog System meant to allow a user to enter in their full sports jersey collection with each jersey's five attributes (player, team, year, color, jersey number). The user will then be allowed to add or delete jerseys, search for jerseys, organize the list of jerseys, display the list, and exit the collection catalog with having all of its data saved.

## Objects:

The object for my project is sports jerseys. Each jersey has five attributes: 

**Player:** First and last name of the player the jersey belonged to.  
**Team:** City and team name of the jersey.  
**Year:** The year the jersey was used.  
**Color:** Main color of the jersey.  
**Number:** Number on the front and/or back of the jersey.

## Data Structures:

**ArrayList:** Is used because we want to be able to insert or delete jerseys from our collection and we want the size to have ability to grow or shrink, an ArrayList is a suitable data structure for this collection catalog system. The ArrayList will give each jersey in the catalog a unique index that allows us to search each jersey individually. We will have an average indexing time of O(1).

**HashMap:** As each jersey has five attributes or keys to them, a hash function is needed to convert all this data into a hash table. This allows for each jersey and its attributes to be searched for instantaneously, or at O(1) time complexity.

## Search Algorithms:

**LinearSearch:** Has an average run time of O(n) and since each jersey in the collection and their attributes have already been given an address in the array at an index, this allows elements to be looked up instantly. This can be used to organize our jersey collection.

**Hashing:** Our HashMap will will convert all input data, or each of the jerseys attributes (player, team, year, color, number) and give each a unique hash value stored in an index. This gives us easy access to our jersey collection with each jersey and its attributes able to be searched quickly. The time complexity to search using hashing is 
O(1).

## Sorthing Alogrithm:

**QuckSort:** Will be the sorting algorithm used as it finds the average case most of the time at O(n logn) time complexity. Plus since all of our data is in an ArrayList, QuickSort will be able to find the index of the desired jersey.

## User Interface Design:

The user should begin with entering each jersey currently in their collection and its five attributes (player, team, year, color, number). They then will be given the option to add jerseys or delete jerseys from their collection, search for specific jerseys in their collection, organize their jerseys by any of their attributes, or display a list of their collection. While also being able to save their work and exit the program whenever desired.

## Persistent Storage:

The main file is the class of the collection (jersey), a subfile will be made for each of the five attributes, with the data being the index designated to each jersey through the Hash Table and ArrayList. After each input, you will get an option of exiting the program which will save the current data. I chose to use the CSV data format as it works well with lists, is compatible for multiple functionalities and is simple to use.

## Exception Handling:

For each task this algorithm can do, I plan to have a fail message set up. Where if the data entered does not fit, matches data already collected or has not been inputed yet, a message pops up to explain the issue, asks them to re-enter new data, or save their current updates and exit the program. This way an infinite loop is not possible as an exit is always offered. 
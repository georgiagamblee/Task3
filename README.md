# Task3
Task 3 - Playing the Game
Introduction
Now back to the game! For this task we're going to some code so the game can actually be played. To do this we will create a class called Game with appropriate methods. This builds on the work done in Task 1, but you are provided with the compiled version of a working implementation of Task 1 (in GameMap.class and Location.class), so you don't need to have completed Task 1 to complete this, though it will help. You can find the details of GameMap and Location in Task 1.

As usual there is a Runner class that lets you do your own testing, but does not form part of the assessment.

There is also a compiled class called TestRunner.class. Don't delete this - it facilitates the tests! (It just loads mazes from files in the right format and feeds them to Game.)

Game
Taking things one step further, we start without Game at all, so you will have to create the file and class from scratch. It should be a public class, and should have the following public methods:

A constructor that takes a GameMap as a parameter.

A method called playGame that returns nothing and has no parameters. This is the method that actually runs the game.

The rules of the game are simple. The player starts at coordinates (0,0), and moves along available directions. Once the player reaches any position that's an exit, the game ends.

There is a welcome message (see below for precise text), and at each turn a version of the map where only the visited parts of the maze are visible should be printed, and the current location of the player should be highlighted. Then the available directions should be printed along with a prompt for the player to choose.

The player then types in their choice of direction. If it is one of the available directions, the player is moved in that direction, if it is not an available direction, the player is informed of this and prompted to try again.

An example trace, which shows most possibilities (and an example of each type of interaction) is as follows:

Welcome to the maze!
╺ 
  
Available directions:
east
Which way would you like to go? east
╶┓
  
Available directions:
south
west
Which way would you like to go? north
You can't go that way! Try again.
Which way would you like to go? ;adsklfj
You can't go that way! Try again.
Which way would you like to go? west
╺┐
  
Available directions:
east
Which way would you like to go? east
╶┓
  
Available directions:
south
west
Which way would you like to go? south
╶┐
 ┛
Available directions:
north
west
Which way would you like to go? west
╶┐
━┘
You made it to an exit. You have escaped!
 Expand (36 lines) 
Advice and Answers
This appears more complicated than it is. If you have finished Task 1, you should know that there's quite a few methods there that make this much simpler. If you haven't, go back and read the specifications for Location and GameMap again. The main task here is to use those method correctly.

You should also think about what you need to keep track of in Game. In particular there is a relatively simple way to only show the visited parts of the map that doesn't require modifying GameMap or Location.

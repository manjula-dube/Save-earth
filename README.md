# AI--Questions

A small question I want every Software Developer to solve it and no worries even if you are not able to solve it in a day.
Because it took me one week to get through the solution:...

  [AI- Question](http://jsfiddle.net/zsvmuyj2/)  (Click on this link to know how planetary works as of now)

* You must write a solution to this using Javascript, but note that you do
not need to interact with the ‘document object model’ (DOM).

* Even if you have limited understanding of Javascript, you should be able to tackle this as far as i think
  For those of you new to Javascript, I would suggest review the math and
  array functions available in Javascript:

+ http://www.w3schools.com/jsref/jsref_obj_math.asp

+ http://www.w3schools.com/js/js_arrays.asp

# Introduction

- The Earth is under attack! You must write an AI to protect the Earth from an onslaught of red
  rocks.
- The action takes place on an 80x10 sensor grid:(See Image 1 for reference)

  [Image 1](https://s23.postimg.org/yzzlo4iwr/Screen_Shot_2017_01_09_at_5_23_23_PM.png)

- Note that (x=0, y=0) is the top-left, and (x=79, y=9) is the bottom-right.
- On the sensor grid you will see rocks hurling towards the Earth (which is itself off-screen somewhere
  to the right). The only thing that stands between the Earth and total annihilation is the Paddle:(See Image 2 for reference)
  
  [Image 2](https://s29.postimg.org/gkcp37vsn/Screen_Shot_2017_01_09_at_6_14_37_PM.png)
  
 - The Paddle is located along the x=80 axis, and can only move ‘up’ and ‘down’. You will need to
   create an AI for The Paddle so that it intercepts the rocks and saves the Earth.
 - NB: Due to technical limitations in Alien technology, the rocks are always 21 grid points apart
 
 # Implementing the AI
 
 - The game updates every ~100ms. For each update, the rocks advance one grid point to the right,
   and the Paddle can do one of the following: move up one grid point, move down one grid point, stay
   where it is.

 - To save the Earth, you must implement the AI for the Paddle. This is done via the ‘notify_player()’
   notification function that is called every time a rock enters or leaves the sensor grid:
   
      ```javascript
      defender.start(function notify_player(rocks, paddle_y){
      var moves = [];
      // compute your moves
      // ...
      return moves;
      } );
    ```
   

  
  

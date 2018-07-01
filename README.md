CSCI S-23a 2018 Assignment 0
Sean Broestl
broestls@gmail.com

Pong AI implementation

I made a few modifications to the code in order to finish this assignment. The first is that Paddle objects have been altered in Paddle.lua. They now have a property called 'cpu'. When this is set to true, code in the keyboard handling portion of main.lua's update callback is used to move the paddles in sync with the ball's y position.

There is a small modification I made to add some personal touch. Paddles also have another property called 'difficulty'. This is a modifier to the paddle speed. The user can make changes to the EASY,NORMAL, and HARD variables which will make the paddle able to respond faster (and in fact, faster than the human player will be able to move theirs on HARD!).

To help prevent tampering in a 2-human game, I added a function to Paddle.lua for setting the difficulty. It takes in a difficulty modifier, and if the Paddle is false on cpu control, then the modifier is ignored.

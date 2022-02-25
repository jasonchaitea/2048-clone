# 2048 Clone

Working on a clone of 2048 created by Gabriele Cirulli only using HTML, CSS, and JS

Original game can be found [here](https://play2048.co/).

Project Link: https://jasonchaitea.github.io/2048-clone/

# How does this work?

1. The first function “createBoard” loads a 4x4 playing board containing 16 squares and places a 0 in each of the squares. 
2. The second function “generate” generates a 2 in a random square if that square is 0. 
3. The following 4 functions “moveRight, moveLeft, moveDown, and moveUp” are how all the numbers move in the grid when pressing up, down, left, or right on the keyboard, 
    - It starts by getting the elements that is in the grid, and then parses them from a string into an integer. 
    - It then takes any number that is not a 0 by using a method called “filter”, and then puts it into an array. 
    - The function then invokes the “missing” variable that was created to filter all the elements that don’t have a number with a 0. 
    - We then create an array called “zeros” to create an array of 0 based on the number of elements that we are missing. 
    - The variable “newRow” is then created to attach the “zeros” array to the filtered array in the right order. 
    - Lastly, we then assign the new number to the rows by getting the square of the index.
4.	The next function “combineRow” combines the numbers if they are the same and next to each other. We only loop this 15 times as we do not want to check the square that is to the right of the last square on the bottom right of the grid.
5. The function “combineColumn” is similar to “combineRow”, with the main difference is that we are only loop 12 times as we only going to be checking the square directly below the square we are looping over.
6. We then assign keycodes for the arrow keys and add an event listener with “keyup”.
7. The functions “keyRight”, “keyLeft”, “keyDown”, “keyUp”, executes the functions that we have created earlier.
8. The “checkForWin” function shows a “You Win!” message once a square has 2048 and removes the event listener.
9. Lastly, the “checkForGameOver” shows a “You Lose!” message once there are no more zeros on the board and removes the event listener.


# Issues

- [ ] Numbers not adding correctly on right side of board.
- [ ] Need to center "You Win!" or "You Lose!" message

# Roadmap

- [ ] Center grid on top 1/3 of page
- [ ] Center "You Win!" or "You Lose!" message
- [ ] Blur screen when "You Win!" or "You Lose!" pops up
- [ ] Recreate game in React

# Credits

Thank you to Gabriele Cirulli for creating the original game!

Thank you Ania Kubów for inspiring and assisting me with recreating this game with your YouTube [guide](https://youtu.be/aDn2g8XfSMc)!
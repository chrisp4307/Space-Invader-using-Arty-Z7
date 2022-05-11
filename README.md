# space-invaders-FPGA
![image](https://user-images.githubusercontent.com/105385216/167924304-76c56bf7-3e5c-4426-880e-d29254b5e805.png)


**Space Invaders Game for the Digilent Artz Z-7 FPGA Board**

This project present the design and implementation of the game “Space Invader” taking its
inspiration from game “Star Fox”, a space shooter game for the Super Nintendo Entertainment
System.. The game is all about shooting stars in the sky by moving the space ship in the
left and right direction with the help of push buttons of the boards.The score of the game
keep increasing as we shoot the stars and once all the stars are shot, the level of the game
changes. The approach of designing a project was modular in nature, attempting to create
modules starting from display through a VGA controller then designing graphics for aliens and
spaceships and creating logics for lives,scores, shooting and shifting of spaceship. The game
is made using the software Vivado 2020.2 and is synthesized on the board Arty Z7 Zynq-7000
Development Board.

## Hardware/Software used
* Digilent Artz Z7 FGPA Board - Zynq-7000 Development Board
* VGA monitor that support 1024x768 resolution at 85Hz
* Vivado Xilinx 
* Digilent PMOD VGA (to connect board to monitor)

## I/O Pins
* SW3 - start switch
* BTN3 - move left
* BTN2 - shoot
* BTN1 - move right
* BTN0 - continue button
* VGA out - connected to a monitor
* Pmod ports-12pins



## About the Game:

![image](https://user-images.githubusercontent.com/105385216/167925072-3183ebce-ec98-40c6-85c4-0a46d0acf185.png)



1. space invader top
The space invader top module is the main file which will run all the other modules and
the whole game from the way the alien ships moves, to the different levels, to the VGA
display as well as the players ship and controls.
2. game controller
This is the module that will control the game .There are total of 5 levels, each level will
have a different score multiplier, it keeps on increasing with each level.
3. inv ship controller
This module is to control the alien ships. There are 5 levels, in each level the pattern in
which the alien ships moves and the position of the alien ships are different.
4. player
This module is for the player ship, which will be used to control the movement of the ship
using buttons on the board.It will also have the firing controls. There are three buttons,
two to move left and right and one to shoot.
5. vga top
This module is the main module for VGA connection, the size of the pixels for the player
ships as well as alien ships are specified in this module, it will content the title screen,
next level screen(blue screen), lost screen(red screen) and win screen (green screen).

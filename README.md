# Tower defense game engine
Tower defense game engine which was made as a school project, it's only interface is through the terminal.

[![asciicast](https://asciinema.org/a/CriNEXXSf0axrHKe6GQHJM7Qo.svg)](https://asciinema.org/a/CriNEXXSf0axrHKe6GQHJM7Qo)

## Description
Engine is using files in directory 'examples/' to load the definiton of the enemies, towers and the map

### Towers
Tower definiton is file named 'tower_def.csv' where each row represents the tower. For example row 'H,1000,2,50,yellow' means
  - H, the symbol which is representing the tower
  - 1000, the price of the tower
  - 2, range meaning how far can tower shoot
  - 50, damage dealt by the tower
  - yellow, color of the tower
    
Color of the tower can be one of following: green, brown, blue, purple, yellow

### Enemies
Enemy definition is file named 'enemy_def.csv' where each row represents the enemy. For example row '!,50,green' means
  - !, the symbol which is representing the enemy
  - 50, health
  - green, tower which is enemy immune to, meaning enemy will be dealt no damage from this tower (this parameter is optional, can be empty)

### Map
Map is simply defined by four symbols, 's' for start, 'x' for end, '.' for path and '#' for wall. Enemies will start coming form 's' to 'x' through the path which is represented as '.'. If no path is find in the map.txt file, engine will find the shortest path form s to x.

## How to run
I am using Makefile to keep all files together, so in order to run it use command `make run`

## Documentation
Documentation of the code can be generated with Doxygen, in order to generate documentation use command `make doc` or without the use of Makefile use command `doxygen Doxyfile`


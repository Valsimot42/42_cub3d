# Cub3D (done in collaboration with [thule-re](https://github.com/thule-re))
<p align="center"><img src="https://cdn-images-1.medium.com/v2/resize:fit:1200/1*mb0KkzYAZDDSvdYC2MM5hg.jpeg" width="150" height="150" />

#
<h3><b>¤ Table of contents ¤</b></h3>

1) <b>How to use</b>
2) <b>Introduction</b>
3) <b>Subject</b>
5) <b>Settings</b>
6) <b>Resources</b>

---
<h3><b>¤ How to use ¤</b></h3>

* Clone the git repository.
* Execute `make` in terminal.
* You can find executable maps in the `maps` folder.
* Execute the following line in the terminal: `./cub3d maps/map.cub`
* Refer to "Settings" for further information.

---
<h3><b>¤ Introduction ¤</b></h3>
<p align="center">"cub3d" project is heavily inspired by a Wolfenstein 3D game, reasons being that in this project we are introduced to the concept of raycasting. The goal of this project is to create a maze with a dynamic view, just like the mentioned Wolfenstein 3D game.

---
<h3><b>¤ Subject ¤</b></h3>

<details>
  <summary>Parameters</summary>
  

  |<b>cub3d</b>|
  |:----------------|
  |Turn in files: All your files|
  |Makefile: all, clean, fclean, re, bonus|
  |Arguments: a map in format *.cub|
  |External functions: open, close, read, write, printf, malloc, free, perror, strerror, exit, All functions of the math library, All functions of the MinilibX|
  |Libft authorized: yes|
  |Description: You must create a “realistic” 3D graphical representation of the inside of a maze from a first-person perspective. You have to create this representation using the Ray-Casting principles mentioned earlier.|

  * You must use the miniLibX. Either the version that is available on the operating
    system, or from its sources. If you choose to work with the sources, you will
    need to apply the same rules for your libft as those written above in Common
    Instructions part.

  * The management of your window must remain smooth: changing to another window, minimizing, etc.

  * Display different wall textures (the choice is yours) that vary depending on which
    side the wall is facing (North, South, East, West).

  * Your program must be able to set the floor and ceiling colors to two different ones.

  * The program displays the image in a window and respects the following rules:

    - The left and right arrow keys of the keyboard must allow you to look left and
      right in the maze.

    - The W, A, S, and D keys must allow you to move the point of view through
      the maze.

    - Pressing ESC must close the window and quit the program cleanly.
   
    - Clicking on the red cross on the window’s frame must close the window and
      quit the program cleanly

    - The use of images of the minilibX is strongly recommended.
   
  * Your program must take as a first argument a scene description file with the .cub
    extension:

    - The map must be composed of only 6 possible characters: 0 for an empty space,
      1 for a wall, and N,S,E or W for the player’s start position and spawning
      orientation. This is an example of how it should look:

        ```text
        111111
        100101
        101001
        1100N1
        111111
        ```

    - The map must be closed/surrounded by walls, if not the program must return
      an error.

    - Except for the map content, each type of element can be separated by one or
      more empty line(s).

    - Except for the map content which always has to be the last, each type of
      element can be set in any order in the file.

    - Except for the map, each type of information from an element can be separated
      by one or more space(s).

    - The map must be parsed as it looks in the file. Spaces are a valid part of the
      map and are up to you to handle. You must be able to parse any kind of map,
      as long as it respects the rules of the map.

    - Each element (except the map) firsts information is the type identifier (composed by one or two character(s)), followed by all specific informations for each
      object in a strict order such as:

      1\) North texture: `NO ./path_to_the_north_texture`

      2\) South texture: `SO ./path_to_the_south_texture`

      3\) West texture: `WE ./path_to_the_west_texture`

      4\) East texture: `EA ./path_to_the_east_texture`

      5\) Floor color: `F 220,100,0`

      6\) Ceiling color: `C 225,30,0`

    - Example of the mandatory part with a minimalist .cub scene:
   
      ```text
      NO ./path_to_the_north_texture
      SO ./path_to_the_south_texture
      WE ./path_to_the_west_texture
      EA ./path_to_the_east_texture
      F 220,100,0
      C 225,30,0
      1111111111111111111111111
      1000000000110000000000001
      1011000001110000000000001
      1001000000000000000000001
      111111111011000001110000000000001
      100000000011000001110111111111111
      11110111111111011100000010001
      11110111111111011101010010001
      11000000110101011100000010001
      10000000000000001100000010001
      10000000000000001101010010001
      11000001110101011111011110N0111
      11110111 1110101 101111010001
      11111111 1111111 111111111111
      ```

    - If any misconfiguration of any kind is encountered in the file, the program
      must exit properly and return "Error\n" followed by an explicit error message
      of your choice.

</details>

---
<h3><b>¤ Settings ¤</b></h3>

<details>
  <summary> Maps </summary>

  * You have the option of following maps:

    1\) 42.cub

    2\) map.cub

    3\) map2.cub

    4\) map3.cub

    5\) simple_map.cub

    6\) testing_map.cub

* For example, if you want to run `map3.cub`, your input will be as follows: `./cub3d maps/map3.cub`

</details>

<details>
  <summary> Textures </summary>

* You can change the textures that will show on the map. To see the available textures you can go
  to `textures` folder, where you will see the following options:

  1\) 42logo.xpm

  2\) bluestone.xpm

  3\) colorstone.xpm

  4\) dark_tiles.xpm

  5\) greystone.xpm

  6\) light_tiles.xpm

  7\) mossy.xpm

  8\) purplestone.xpm

  9\) redbrick.xpm

  10\) wood.xpm

* If you open one of the maps in `maps` folder, you will see the following structure:

  ```text
  NO textures/greystone.xpm
  SO textures/redbrick.xpm
  WE textures/mossy.xpm
  EA textures/colorstone.xpm
  
  F 100,100,100
  C 0,0,127
  ```

* `F` and `C` textures are represented in RGB values (range 0-255) and can be changed at will.

* WARNING: in `textures` folder you will also see .png files. Trying to execute the program with
  .png files will result in the program not launching. Execute only with .xpm files
  
</details>

  

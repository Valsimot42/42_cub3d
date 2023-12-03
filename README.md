# Cub3D (done in collaboration with [thule-re](https://github.com/thule-re))
<p align="center"><img src="https://cdn-images-1.medium.com/v2/resize:fit:1200/1*mb0KkzYAZDDSvdYC2MM5hg.jpeg" width="150" height="150" />

#
<h3><b>¤ Table of contents ¤</b></h3>

1) <b>How to use</b>
2) <b>Introduction</b>
3) <b>Instructions</b>
4) <b>Part 1: Parameters</b>
5) <b>Part 2: Example</b>

---
<h3><b>¤ How to use ¤</b></h3>

* Clone the git repository.
* Execute `make` in terminal.
* You can find executable maps in the `maps` folder.
* Execute the following line in the terminal: `./cub3d maps/map.cub`
* Use `W A S D` keys to move the player and `arrow keys` to move the camera.

---
<h3><b>¤ Introduction ¤</b></h3>
<p align="center">"cub3d" project is heavily inspired by a Wolfenstein 3D game, reasons being that in this project we are introduced to the concept of raycasting. The goal of this project is to create a maze with a dynamic view, just like the mentioned Wolfenstein 3D game.

---
<h3><b>¤ Instructions ¤</b></h3>

* Project must be written in C.

* Functions should not quit unexpectedly (segmentation fault, bus error, double free, etc) apart from undefined behaviors.

* All heap allocated memory space must be properly freed when necessary. No leaks will be tolerated.
If the subject requires it, you must submit a Makefile which will compile your source files to the required output with the flags -Wall, -Wextra and -Werror, use cc, and Makefile must not relink.

* Makefile must at least contain the rules $(NAME), all, clean, fclean and re.


---
<h3><b>¤ Part 1: Parameters ¤</b></h3>

<p align="left̨">

* You must use the miniLibX. Either the version that is available on the operating
system, or from its sources.
* The management of your window must remain smooth: changing to another window, minimizing, etc.
* Display different wall textures (the choice is yours) that vary depending on which
side the wall is facing (North, South, East, West).
* Your program must be able to set the floor and ceiling colors to two different ones.

---
<h3><b>¤ Part 2: Example ¤</b></h3>

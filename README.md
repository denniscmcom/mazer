# Mazer

A maze solver written in C using libpng. Takes a maze as a PNG image and
outputs the solution using the Wall Follower algorithm.

## Input

<img src="https://public.denniscm.com/repositories/mazer/maze.png" width="400">

## Output

<img src="https://public.denniscm.com/repositories/mazer/maze_solved.png" width="400">

## Features

- Reads and writes PNG files directly using libpng.
- Wall Follower pathfinding algorithm.
- Outputs solved maze with the path highlighted in red.
- Prints solve time to stdout.

## Build & Run

Requires libpng and CMake.

```
mkdir build && cd build
cmake ..
make
```

```
./mazer <path-to-maze.png>
```

The solved image is written to the current directory as
`solved_<filename>.png`.

## Maze Requirements

- PNG format with RGBA color.
- Black walls `rgb(0, 0, 0)` and white paths `rgb(255, 255, 255)`.
- 1px wall and path width.
- Entry at top-left `(0, 1)`, exit at bottom-right `(width-1, height-2)`.

You can generate compatible mazes with [this tool](https://keesiemeijer.github.io/maze-generator/).

## References

Inspired by Computerphile's [Maze Solving video](https://www.youtube.com/watch?v=rop0W4QDOUI). 
Algorithm details: [Wall Follower (Wikipedia)](https://en.wikipedia.org/wiki/Maze-solving_algorithm).


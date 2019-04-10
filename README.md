# Goal
The goal of the project is to develop code for computing data based on Beat Saber (a Virtual Reality rythm game whereby the player is tasked with using their arms to slice fast moving blocks in time with music) maps which can be used for interesting purposes such as generating maps automatically, recommending other songs based on a given player's favorite maps/songs, etc.

The name of the repo is based on the character Lynchman from one of the best animated movies of all time, Redline. He has a minor role in the movie but as an intergalactic mercenary for hire he spends a portion of his screen time stretching his arms and legs in preparation for his work, as one usually or should do before playing Beat Saber.

# JSON File Format for Beat Saber Maps
Maps are stored in .json files with a pretty self-explanatory format for the most part.


## tileIndex (columns), tileLayer (rows)
Denotes the position of the tile in a fixed 3x4 grid.

```
     --- --- --- ---
 2  |   |   |   |   |  l
    |   |   |   |   |   a
     --- --- --- ---     y
 1  |   |   |   |   |     e
    |   |   |   |   |      r
     --- --- --- ---
 0  |   |   |   |   |
    |   |   |   |   |
     --- --- --- ---
      0   1   2   3   index

```
tileLayer denotes the row as described in the diagram above.

tileIndex denotes the column as described in the diagram above.

## type
Denotes the color/side of the tile (left or right)

When type is 0, the tile must be hit with the left saber.
When type is 1, the tile must be hit with the right saber.

## cutDirection
Denotes the cardinal direction, or lack thereof, through which the tile must be cut.

N  : 1
NE : 6
E  : 2
SE : 4
S  : 0
SW : 5
W  : 3
NW : 7





```
       1
     -----
    /     \
 7 /       \ 6
  /         \
  |         |
3 |    8    | 2
  |         |
  \         /
 5 \       / 4
    \     /
     -----
       0

     1
   -----
  |     |
3 |     | 2
  |     |
   -----
     0

     -
    / \
 7 /   \ 6
  /     \
  \     /
 5 \   / 4
    \ /
     -
```


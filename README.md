# The Maze

### Overview

![begin3](docs/begin3.jpg)

Our **maze game** allows people to use keystrokes to walk in a 3D maze, in which the player needs to find keys, open gates, and find the exit. When exploring in the maze, the player will meet moving monsters and obstacles which could possibly wound the player. For each round, the player has three lives, and there is a timer to record how much time the player spent to finish the maze. There are three perspectives: first-person, third person, and global perspectives, each has different advantages when playing. Also, sounds are played when the player is performing different actions. 

### Usage
1. Download files
```
$ git clone https://github.com/yuan-shen-269/The-Maze.git
$ cd The-Maze
```

2. To Maximize experience, we will run a fake server.
- For Mac User:
```
$ chmod 777 host.bat
$ ./host.bat
```
- For Windows User:
```
$ chmod 777 host.command
$ ./host command
```
3. If succeeed, you will see "Serving HTTP on 0.0.0.0 port 8000 ..." on the console.
   Keep the console open, and open a new window of Google Chrome.
   Navigate Chrome to http://localhost:8000/, you will now be able to play the game.


### How to Play

To start the game, first press the Start Game button. 
6 keys are used for basic operations:
  ```
  W - Foward 
  A - Back 
  S - Left
  D - Right
  X - Squat
  Space - Jump
  J - Turn left
  K - Turn right
  O - Open door
  ```
  
3 keys are used to change perspectives:
  ```
  F - First-person perspective
  T - Third-person perspective
  G - Global perspective
  ```

Once the player has a move, the timer is triggered to record the time. 

The player has to keep away from the monsters and goes across the obstacles. Every time the player runs into a monster or an obstacle, the player will lose one life, and the player will die if all there is no live available. 

During the game, the player has to find all the keys and open the doors. 
`Notice: there are two keys in the maze, each for its corresponding door, you need to figure out which ones are paired.` 

There is a red flag placed at the exit, as soon as the player touches the flag, the timer is stopped and the winning scene will pop up.

### Advanced Features

- **Collision Detection** - Collision detection with walls and obstacles, prevent player entering the wall, and decrease health if the player hit obstacles.
- **OBJ Models** - 3D models in .obj formats, including Mario character, gates, keys, and flag, are imported with texture mapping and animations. 

### Individual Roles

#### Yuan Shen

- Constructed the model of the monsters and implemented the movement of their arms and legs.
- Wrote the basic algorithm for the movement of monsters. 
- Wrote the key-and-door method that detects if the player is qualified to open the door (the player has to pick up the corresponding key, be closer enough to the door, and hit the "open door" key).
- Refined the appearance of the obstacles using 9 individual obstacles and placed them into the maze.
- Added textures to the walls and the floor, and modified the appearance of the keys. 
- Implemented two test mode: 
  * Invincible mode where the player will not lose any life.
  * Walk-through mode where the player can go through all the walls and doors.

#### Ziyan Wang

- Built the prototype of the maze.
- Implemented the movement control of the player (WASD, jump/squat, turn left/right)
- Added collision detection with the wall and obstacles (spikes, monsters, and doors)
- Implemented the first person, third person, and global camera perspectives.
- Built the health system for the player and updated the health for each frame.
- Refined the movement of the monster in the maze.
- Refined the animation of the door opening.

#### Wenxuan Liu

- Wrote the animation for individual obstacles which is constructed by many cubes scaled and translated proportionally by time.
- Wrote the destination detection method to activate the winning scene when the player goes out of the maze.
- Drew and wrote the UI interfaces in HTML including the beginning, die, and win scenes.
- Added the timer, health, and key number UI, and wrote the algorithm to update the timer.
- Modified the obj models import methods, and collected all the models and constructed them into the appropriate textures, proportions, and positions.
- Added music and FX to the game, so that there are corresponding sounds when the character is winning, wounded, walking, opening gates, and died.

### Resource Citation

- **models** - all from TurboSquid.com

  **Mario** https://www.turbosquid.com/FullPreview/Index.cfm/ID/549984

  **Gate** https://www.turbosquid.com/FullPreview/Index.cfm/ID/1366455

  **Flag** https://www.turbosquid.com/FullPreview/Index.cfm/ID/974692

  **Key** https://www.turbosquid.com/FullPreview/Index.cfm/ID/448201

- **Sounds** - all from Logic Pro X FX library


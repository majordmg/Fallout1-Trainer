# Fallout 1 (Classic) Trainer

## About

![The trainer in action](https://github.com/danjaaron/Fallout1-Trainer/blob/master/fallout1-trainer-whole.PNG)

This repository contains the source code for a (mostly) complete cheat trainer for Fallout 1 (GOG).

This trainer attaches to a process called **falloutw.exe**. The fallout process must have this name because of the static pointers that were used to create this trainer.

If your game's process is not named **falloutw.exe**, you must either rename the process before running the standalone trainer, or run from Cheat Engine (option 2 below). 

## Setup

There are two options, depending on your system architecture.

### Option 1: Windows x86

If you're running Windows x86, simply run the standalone .EXE file after starting Fallout 1.

You can then edit any of the field values, open and close the CHAR screen, and your inputted values will update in-game.

### Option 2: Cheat Engine

Open the attached Cheat Table (.CT) in Cheat Engine. Run Fallout 1. Attach to the Fallout 1 process with Cheat Engine. 

Navigate to "Table" --> "Show Lua Script" and then click on "Execute Script". The trainer GUI shown above should open and the trainer will then activate. 

Note: the Cheat Table contains memory addresses for a few more critical values (e.g. the value of each skill) than are available via the trainer GUI.

## Usage

Simply edit any field, e.g. Carry Weight, and then open and close the in-game character menu. Your character's attributes should update accordingly. 

*Note: you can use this trainer to push in-game values beyond their intended purposes. From initial experiments I have found that this does make a meaningful difference.*

Example: your HP is calculated based on your STR. The maximum "natural" STR, without cheats, is 10. That results in a max "natural" HP of 47. This is the highest value of HP accessible to a non-cheating player. Using this trainer, you can change your STR to 999. That results in an HP of 1000+. 

Another way to max out a characteristic is to input -1. Because of how integer values work, inputting a '-1' for a value that the game expected to be a positive integer can cause that value to roll over to its maximum positive value. This is fun to do with things like MELEE_DAMAGE. When you kill an enemy in unarmed combat, the enemy corpse will slide away from the player for a duration that is dependent on the player's melee damage. Rolling over the melee damage to the maximum positive value, or even just maxing out the melee damage (e.g. 999) will cause enemy corpses to slide until they're off screen. Note that rolling over values in this way can cause the game to become unstable and sometimes will crash as a result. 

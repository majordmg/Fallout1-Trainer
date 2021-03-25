# Fallout 1 (Classic) Trainer

## About

![The trainer in action](https://github.com/danjaaron/Fallout1-Trainer/blob/master/fallout1-trainer-whole.PNG)

This repository contains the source code for a (mostly) complete cheat trainer for Fallout 1 (GOG).

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

Note: you can use this trainer to push in-game values beyond their intended purposes. From initial experiments I have found that this does make a meaningful difference.

Example: your HP is calculated based on your STR. The maximum "natural" STR, without cheats, is 10. That results in a max "natural" HP level accessible to a non-cheating player. If you use this trainer to change your STR to 999, the game will only show that your STR is 10 (Heroic), but you will notice that it has updated your HP far above the "natural" level. In other words, even though the Fallout GUI only shows a max STR of 10, you can indeed change your STR level higher and it does change increase other things in the game far beyond their normal limit as a result. 

Another way to max out a characteristic is to input -1. Because of how integer values work, inputting a '-1' for a value that the game expected to be a positive integer can cause that value to roll over to its maximum positive value. This is fun to do with things like MELEE_DAMAGE. Note that this can cause the game to become unstable and sometimes will crash as a result. 

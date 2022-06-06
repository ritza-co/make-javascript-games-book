# Getting started

Kaboom.js is a JavaScript library that contains many useful features to make simple in-browser games. It has functionality to draw shapes and sprites (the images of characters and game elements) to the screen, get user input, play sounds, and more.

Kaboom also makes good use of JavaScript's support for callbacks; instead of writing loops to read in keyboard input and check if game objects have collided (bumped into each other), Kaboom uses an event model, where it tells us when such an event has occurred. Then we can connect up callback functions that act on these events.

Using Kaboom in Replit takes care of all the boilerplate initialisation code, as well as asset loading, so we can concentrate on writing the game logic and making game graphics and sound.

## Creating a new project in Replit

Head over to [Replit](https://replit.com/) and create a new repl. Choose Kaboom as your project type. Give this repl a name, like "Flappy!".

![Creating a new repl](https://replit-docs-images.bardia.repl.co/images/tutorials/35-flappy-bird/new-repl.png)

## Setting up Kaboom

After the repl has booted up, you should see a main.js file under the "Code" section. This is where we'll start coding. There is already some code in this file, but we'll replace that.

In the "main" code file, delete all the example code. Now we can add reference to Kaboom, and initialize it:

```js
import kaboom from "kaboom";

kaboom();
```

Our edited code initializes Kaboom and gives us a blank canvas to work with.

## Scenes and layers

A Kaboom game is made up of scenes, which are like levels, or different parts and stages of a game. You can use scenes for game levels, menus, cut-scenes, and any other screens your game might contain.

There are generally three scenes in games:
- The intro scene, which gives some info and instructions, and waits for the player to press "start".
- The main game, where we play.
- An endgame, or game over scene, which gives the player their score or overall result, and allows them to start again.

Scenes are further divided into layers, allowing us to have game backgrounds, main game objects (like the player, bullets, enemies, etc), and UI elements (like the current score, health, etc). Layers are populated by game objects (also called sprites). The layer an object is on will determine when it gets drawn and which other objects it can collide with.

## Assets

Many of these games include a ZIP file of assets. Download the ZIP file for the game you’re building and extract it on your computer. Click the "Files" icon on the sidebar and upload everything in the extracted file's Sounds folder to the "sounds" section of your repl, and everything in the Sprites folder to the "sprites" section of your repl.

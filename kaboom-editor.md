# Kaboom editor

Kaboom.js is a game programming library that makes it fun and easy to build games! 

This doc explains the tools provided by the kaboom editor on Replit. To learn the kaboom library, check out the docs, guides and examples on the [kaboom website](https://kaboomjs.com/).


## Scene Manager

In plain kaboom.js, you would write each scene's content inside each scene block:

```js
scene("start", () => {
	add(...);
	action(...);
	keyPress(...);
});

scene("game", () => {
	// ...
});
```

In the Replit kaboom editor, scenes are treated as files and there's no need to wrap everything in a scene block.

![scene](/images/tutorials/kaboom/scene.png)

Each scene will receive a `args` argument which contains the argument that you pass from, e.g. `go("win", { score: 18, })`.

## Sprite Manager & Editor

The editor will take care of `loadSprite()` calls, so you can directly use these with the `sprite('name')` component.

There're two ways to add sprites right now:

1. Drag to upload your own files.

![drag](/images/tutorials/kaboom/drag.png)

2. Click '+' to create a sprite with the sprite editor.

![addsprite](/images/tutorials/kaboom/addsprite.png)

The edited sprites will be saved automatically. Once you have created a sprite you can load it into your game by opening your main code file, placing your cursor at the point in your file where you want the sprite to be loaded, and then selecting "Insert load code."

![Insert load code](/images/tutorials/kaboom/insert-load-code.png)

This should insert a line of code that looks like this:

```javascript
loadPedit("Sample", "sprites/Sample.pedit");
```

Notice the use of `loadPedit` instead of loadSprite. With this call in place you should be able to use the component `sprite("Sample")` in your game.

![pedit](/images/tutorials/kaboom/pedit2.png)
![workspace](/images/tutorials/kaboom/workspace.png)

(Right now, the sprite editor is not optimized for big sized sprites.)

## Sound Manager

Sound manager is currently just a place similar to sprite manager that lists your sounds. You can drag your sound files here and don't have to call `loadSound`. A built-in sound/music editor is in the works. 

## Debug

The debug menu contains some handy tools to help you inspect game states.

![debug](/images/tutorials/kaboom/debug.png)


## Settings

The settings menu contains some game-related configs, including:

- Size of the game canvas.
- If fullscreen or not (ignores the size setting).
- Pixel scale (try scale it up if you're making pixelated games).
- Starting scene.
- Library version. 

New kaboom repls defaults to the latest version. If a newer version comes out after you created the repl, you need to manually select it, unless you're on `dev` version, in which case you'll always be on the latest version and breaking change is possible.

![settings](/images/tutorials/kaboom/settings.png)
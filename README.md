# Cursor (NeoForge 1.20.4)

Adds one item: the **Cursor**, a Windows-style mouse pointer.

## How it works in game

- **Right-click** while pointing at a mob or the ground (up to 48 blocks away; see the config) to pick it up. A chunk of ground (5 to 10 blocks wide, 7 by default) lifts out of the world as one floating piece.
- It floats in front of you and follows where you look.
- **Left-click** to put it down. Mobs fall back down; blocks are placed back wherever the chunk is floating (anything that can't be placed comes back as an item).
- **Right-click again while carrying** to open the menu: Copy, Rename, Delete (asks twice), Properties.
- **Sneak + right-click** (when not carrying) cycles the grab size 5 to 10.
- Switching away from the Cursor drops what you carry.
- Not picked up: players, the Ender Dragon, unbreakable blocks, fluids, and blocks with inventories (chests, furnaces, spawners).

## Crafting (mid/late game, before the Ender Dragon)

```
D E D      D = Diamond
E N E      E = Eye of Ender
D E D      N = Netherite Ingot
```

## Building

This zip is the SOURCE, not a mod. It will not show up in Minecraft until it is built into a .jar.

No computer set up for it? Upload this folder to a new GitHub repository: the included workflow (.github/workflows/build.yml) builds it, and the jar is under Actions -> latest run -> Artifacts.

1. Install a Java 17 JDK (the build also asks Gradle to fetch Java 21 for one tool, which it can do automatically).
2. In this folder run `./gradlew build` (Windows: `gradlew.bat build`). The mod jar ends up in `build/libs/`.
3. Copy the jar into the `mods` folder of a NeoForge 1.20.4 install.
4. To test from your IDE instead, run `./gradlew runClient`.

Config file after first launch: `config/cursormod-common.toml` (`range`).

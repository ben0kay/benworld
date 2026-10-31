# PLAYER — First-Person Player Systems

**Status:** Folder/ownership guide only. No Player scene, player scripts or FPS test room have been created yet.

`PLAYER/` is the sole owner of the reusable first-person player scene and its gameplay code.

## Intended ownership

- `PLAYER/Player.tscn` and `PLAYER/Player.cs` (planned): character controller, first-person camera and player lifecycle.
- `Movement/` (planned): walking, sprinting, jumping, crouching/leaning as later authorized.
- `Weapons/` (planned): equipping, firing, recoil, weapon visuals and hit interactions.
- `Interaction/` (planned): interaction queries, pickup/use prompts and related player interfaces.
- Other folders (inventory, health, stamina, audio) should be added **only when implemented**, with coherent ownership.

## Isolation and integration

The planned `Scenes/Tests/FPS_Test.tscn` should instance Player into a simple graybox room for independent mechanics testing. **Player must not depend on `WORLD/World.tscn`, marching cubes, terrain-specific node paths or a particular map.**

Later `Scenes/Game/MainGame.tscn` can instance the same Player scene into WORLD and provide spawn placement, collision/world queries, interaction interfaces and shared signals as necessary. Borrow selected working mechanics from [War Machine](https://github.com/ben0kay/war-machine) only after reviewing dependencies and receiving authorization; this guide does not copy any code.

Read [root README](../README.md), [AGENTS](../AGENTS.md) and [CodePreferences](../CodePreferences.md) before implementation.

# SCENE — Independent Test Worlds

Test environments instance reusable feature scenes and **do not own gameplay code**.

- **[Scene_Player.tscn](Scene_Player.tscn)** — graybox FPS test room with a floor, four walls, collision obstacles, a low ceiling for crouch testing and an instanced `res://PLAYER/Player.tscn`. **Authored; awaiting local Godot validation.**
- `Scene_World.tscn`, `Scene_Buildings.tscn`, `Scene_AI.tscn`, and `Scene_Game.tscn` — **planned**, not yet created.

Build the C# project, open `Scene_Player.tscn` and press **F6** (Run Current Scene). To use F5 instead, set the main scene to `res://SCENE/Scene_Player.tscn` in your local Godot Project Settings. Input handling lives in `PLAYER/Input/PlayerInput.cs`, not in SCENE scripts.

**Note:** `project.godot` was created on the owner's PC but has not yet been pushed to GitHub; do not replace the local file blindly.

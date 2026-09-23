# Camera Movement in Xogot (Xogot 3D Tutorial)

This project contains the example scenes and assets used in the
**Xogot 3D Modular Series - Camera Movement** tutorial by **Erin Uptegrove**.

It demonstrates how to build a more flexible third-person camera in **Xogot** - the iPad and
iPhone port of the Godot Engine - by separating the camera from the player and controlling its
movement with a reusable camera controller scene.

The project includes smooth position and rotation tracking, a SpringArm3D for collision-aware
camera placement, and mouse-look controls with adjustable sensitivity and tilt limits.

---

## Features

* Create a reusable camera controller scene with Node3D
* Use a Pivot node to keep camera look rotation predictable
* Add a SpringArm3D to prevent the camera from clipping through level geometry
* Tune spring length and camera height for third-person framing
* Smoothly follow the player's position with `lerp()`
* Smoothly follow the player's rotation with `lerp_angle()`
* Adjust position and rotation tracking speeds in the Inspector
* Add mouse-look controls with `InputEventMouseMotion`
* Configure mouse sensitivity with an exported range
* Clamp vertical camera tilt to a configurable angle

---

## Notes

This project focuses on **introductory third-person camera movement** in Xogot, not a complete
camera framework.

Key ideas demonstrated include:

* A camera can follow more naturally when it is controlled independently from the player
* Position and rotation tracking speeds create a smooth, slightly delayed follow effect
* SpringArm3D helps the camera react to nearby level geometry instead of clipping through it
* A dedicated pivot keeps horizontal and vertical look rotation easy to reason about
* Exported variables make camera feel easy to tune without rewriting the script

---

## Video Tutorial

Watch the full walkthrough on the [Xogot YouTube Channel](https://youtube.com/@xogot):

**Better Camera Movement in Xogot - Game Development in Godot on iPad**
https://youtu.be/JdOshFWwXS0

---

## How to Use

1. Download or clone this repository:

   ```bash
   git clone https://github.com/xogot-projects/Xogot-Camera-Movement.git
   ```

2. Open the project in [Xogot](https://apps.apple.com/us/app/xogot-make-games-anywhere/id6469385251) on iPad or iPhone.

3. Open `Environments/Day.tscn` and preview the project.

4. Use the virtual controls to move the player and drag to adjust the camera view.

5. Select the `CamControl` node to experiment with tracking speed, mouse sensitivity, and tilt range.

---

## Project Structure

* `Assets/cam_control.tscn` - reusable third-person camera controller
* `Assets/player.tscn` - player scene used by the example
* `Environments/Day.tscn` - main tutorial scene
* `scripts/camera_look.gd` - smooth follow and mouse-look implementation
* `scripts/camera.gd` - smooth follow example without mouse-look

---

## Learn More

* [Xogot](https://xogot.com)
* [Xogot Documentation](https://docs.xogot.com/documentation/xogot/)
* [Xogot Tutorials](https://docs.xogot.com/tutorials/xogot-tutorials/)

Built with Xogot on iPad.

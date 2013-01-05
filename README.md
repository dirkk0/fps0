FPS0
====

A ThreeJS/physics experiment, with first person controls and minimal collision detection.


The goal of this project was to explore the options for a simple game with first person controls that runs completely in a browser. To achieve this I wanted to be able to

  - load a 'level', i.e. a basic 3D model (in this case with Blender)
  - create 'WASD' first person type of controls
  - apply simple physics with collision detection to walk around and
    interact with objects
  - add dynamic objects on runtime

Luckily, all of the ground work was already done by someone else. :-)

Basically this demo merges the [Blender scene loader](http://mrdoob.github.com/three.js/examples/webgl_loader_scene_blender.html) of [mrdoobs](http://mrdoob.com/) [ThreeJS library](http://mrdoob.github.com/three.js/) and the [CannonJS](https://github.com/schteppe/cannon.js) [FPS example](https://github.com/schteppe/cannon.js/blob/master/examples/threejs_fps.html) by [schteppe](https://github.com/schteppe).


I added the idea that the imported Blender geometry gets turned into a static model in the physics engine by finding the cubes and adding invisible physical collision boxes to their position.

This worked surprisingly well and gives some sort of minimal FP(S) - completely running in the browser.
The imported Blender model is turned into a static model by adding the boxes as static physic objects. This way this you can 'walk' on the objects of the Blender model (the grey objects in the screenshot).

![Screenshot](http://dirkk0.github.com/fps0/images/scene.png)

Important: to try it locally you still must run it from a web server (for example 'python -m SimpleHTTPServer') due to cross-origin security issues.
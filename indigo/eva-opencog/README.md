eva-opencog
===========

An image containing the OpenCog + Hanson Robotics Eva robot.
This is the whole kit-n-kaboodle. In development. Probably broken.

The data processing pipeline consists of:
* A ROS node that takes video input from a UVC-compatible USB webcam
  (most typical desktop/laptop cameras are compatible).
* A ROS node that does face detection: it tries to find human faces in
  the video feed.
* A ROS node that maps the face postions to a 3D coordinate system.
* A ROS node that runs the Eva blender rig itself (i.e. uses blender
  to draw/animate Eva).
* A ROS node that converts PAU (Physiological Action Units) into motor
  controls, needed for animating physical robot models.

## Building

Run the `./build.sh` file in this directory.  You need to have built
the `ros-incog-blender` image (in the `../ros-incog-blender` directory)
first.

## Testing
To verify that blender works, run the `./run.sh` shell script.
This will start blender and the half-dozen ROS nodes that control it.
You should see a living, breating Eva; however, you proably won't
due to some bug that is being worked right now.  Open a github issue
or complain on the mailing list!
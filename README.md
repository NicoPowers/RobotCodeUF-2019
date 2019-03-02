# RobotCodeUF-2019

---

## Below are the following steps to get setup with ROS

1. [Install Ubuntu Linux 16.04 image](http://releases.ubuntu.com/16.04/).
2. Create a bootable image using the image you downloaded by flashing it to a thumbdrive ([I recommend this software program to flash to a thumbdrive](https://www.balena.io/etcher/)]),
   and then stick it in to your computer and restart your computer and boot into the thumbdrive and follow the installation process.
   There are many online tutorials and YouTube videos detailing this process.
3. [Start reading this book](http://lsi.vc.ehu.es/pablogn/investig/ROS/A%20Gentle%20Introduction%20to%20ROS.pdf).
4. [Install Fustion 360 on Windows Partition](https://www.autodesk.com/products/fusion-360/overview?mktvar002=1028563&&mkwid=sGqd1YrTz%7cpcrid%7c308370108716%7cpkw%7cfusion%20360%7cpmt%7ce%7cpdv%7cc%7cslid%7c%7cpgrid%7c64140211587%7cptaid%7caud-554208419493:kwd-330308867034%7c&intent=&utm_medium=cpc&utm_source=google&utm_campaign=GGL_Fusion+360_US_BR_RMKT_SEM_EXACT&utm_term=fusion%20360&utm_content=sGqd1YrTz%7cpcrid%7c308370108716%7cpkw%7cfusion%20360%7cpmt%7ce%7cpdv%7cc%7cslid%7c%7cpgrid%7c64140211587%7cptaid%7caud-554208419493:kwd-330308867034%7c&addisttype=g&s_kwcid=AL!8131199977!3!308370108716!e!!g!!fusion%20360&gclid=CjwKCAiA8OjjBRB4EiwAMZe6yzMp-CQelZoSLza5P_g1dVg6iRk-s1qif1UiZcgR0X0l9ZPeRn6VvxoCIc4QAvD_BwE&gclsrc=aw.ds) and signup using your ufl.edu account to access it for free as a student.
5. Download the Fusion 360 course file I created [here](https://a360.co/2EsgpaQ).
6. Download the Fusion 360 robot 3D model that is used to generate the URDF file [here](https://a360.co/2TdAvzG).
7. Follow the steps [here](https://github.com/syuntoku14/fusion2urdf) to convert the robot 3D model into a .urdf file.
8. Install the [Collada Writer on Windows Partition](https://apps.autodesk.com/FUSION/en/Detail/HelpDoc?appId=934783265519220722&appLang=en&os=Win64) add-in for Fusion 360 that allows you
   to export 3D models to .dae files (used in Gazebo to display the world). You will use this to export a .dae file for the course file.
9. Follow [this video](https://www.youtube.com/watch?v=aP4sDyrRzpU) to try to get the course map opened in Gazebo (you will have to [install gazebo on Linux Partition](http://gazebosim.org/)).
10. Go [here](http://wiki.ros.org/urdf/Tutorials/Building%20a%20Visual%20Robot%20Model%20with%20URDF%20from%20Scratch) to learn more about URDF files.

I am still in the process of learning about how to integrate the Robot Model and the World File to start actually running simulations and stuff like that, so please experiement with stuff at home and let me know what you can figure out as well.

[Here is the link to the final Hardware rules](https://drive.google.com/file/d/1KRLF-HR9mwWrROvVW-r7jZPUBfodCOC-/view?usp=sharing).

If you can, try to verify that I made the course correctly in Fusion 360.

We will develop the code for the two Arduino's once we figure out the setup and configuration for ROS to start simulating different SLAM algorithms and stuff.

We will most likely be using [this tutorial](http://emanual.robotis.com/docs/en/platform/turtlebot3/slam/) to get started with SLAM, mapping, setting waypoints, and all the stuff.

---

# TODO

## Software

1. Properly import the robot 3D model into RViZ with the corrent base_links and joints orientation and position.
2. Figure out how to simultanously place the course file (.dae file) and the exported robot 3D model (.urdf file) in either RViZ or Gazebo to start running simulations.
3. Figure out how to create a virtual LiDAR sensor for the simulations.
4. Generate the course map in RViZ using the teleop key and our robot.
5. Set way points in RViZ and linearly approximate spiral motion.
6. Try to create artificial artifacts in generated map to resemble amber lights.
7. Figure out if we can set waypoints by using features on the generated map (like near corners or something)
8. Figure out how to automate the setting of waypoints and set a timer to activate each phase of the program:
   1. Exit the starting square
   2. Enter the orbital circle
   3. Complete 2 - 3 spirals to push debris outwards
   4. Hug tower and do as many orbits as possible
   5. Return to home base and raise on-board flag

## Hardware

1. Create 4 1' x 1' squares to extend 8' walls to 9' (using braces)
2. Create back side caster to prevent robot from tipping.
3. Create center tower out of 4 peices of wood.
4. Create center circle using wire or tape.
5. Get bricks to hold walls in place when assembling course.
6. Color UF Flag with blue and orange colors and fix it to servo motor.

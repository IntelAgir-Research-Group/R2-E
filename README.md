# R2-E - Research Robot (R2): Earth-class/Education

The name `R2-E` is inspired by two of the most famous robots on the screens: `R2-D2` and `WALL-E`.  In our project, the acronym has a different meaning: `R2` stands for Research Robot since it is a robot created for research; at the same time, the `E` signifies educational, while also evoking the essence of `WALL-E` as an earth-class robot.

Joining science and cinema together has great potential to make the world a better place. Movies have inspired different types of real-world robots, and a great screenplay is always funnier than a class.

Finally, our research is inspired by three pillars of `sustainability`: 1) reuse/recycling; 2) energy efficiency/green computing; and 3) educational inclusion. We transform existing devices such as Android TV SBCs and robotic vacuums into computational units and mobile robots; use them for our research on energy-efficient robotic software; and make it possible for public Brazilian schools to have access to this kind of technology through lectures about mobile robots and computer programming. Note that Brazil is a diverse and, at the same time, unbalanced country. Usually, public schools struggle to access modern technologies due to their limited budgets. 

## THE PROJECT

TBA

## ROBOT's PARTS

Here we describe the design of the physical robot.

### Robotic Base

Our robot is built on top of `Xiaomi S10 Vacuum`, which already counts on navigation sensors that will then feed [`Nav2`](https://docs.nav2.org/) and other customized `ROS` packages.


### Robotic Body

On top of the robotic vacuum, we build a 3D printed structure to fix the SBC where local ROS packages run, an optional camera, and other hardware parts, such as the necessary batteries and additional sensors.

Below, you can visualize and download the 3D model of a basic body, which can then be easily adapted for your needs:

TBA

### Robotic "Brain"

All the necessary packages run on a customized SBC, which is delivered by other project that transform Android TV Boxes into Linux terminals. 

TBA (image of the box)

The image of the Ubuntu Linux system for such a device as well an explanation of the project can be found [here](#).

We additionally provide a RaspberryPi image [here](#) for a matter of reproducibility since those devices are popular and accessible around the world.

## ROS PACKAGES

We have been developing multiple packages for this robot according to our research needs. Here, we only describe the ones necessary to bring up the robot, making it to listen to teleoperation commands and to broadcast its sensor data to preset ROS topics.

We keep the complete list of provided packages and their description in a separated file [here](#).

As a first step, please, access your SBC with a moritor and keyboard (`username`: `r2e-admin`, `password`:`admin`), set the WiFi connection and take note of its IP address (we recommend to keep it static). 

Then, it's necessary to identify which is the IP address of the robotic base. For that, download and install the Xiaomi app from [here](#).
 
Now we are ready to go. Access your SBC via SSH and type the following commands.

```bash
source /opt/ros/humble/setup.sh
ros2 launch r2e_bringup --ros-args -p base_ip:<ip of the vacuum>
```

Now, in your laptop, you can check the sensors with ROS topic commands:
```bash
ros2 topic echo aaa
```

Try to teleoperate the robot:
```bash
ros2 run teleoperation teleoperation
```

## CONTRIBUTIONS

TBA pr policy
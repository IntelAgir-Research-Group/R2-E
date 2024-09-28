# R2-E - RESEARCH ROBOT (R2): EARTH-CLASS/EDUCATION

The name `R2-E` is inspired by two of the most famous robots on the screens: `R2-D2` and `WALL-E`.  In our project, the acronym has a different meaning: `R2` stands for Research Robot since it is a robot created for research; at the same time, the `E` signifies educational, while also evoking the essence of `WALL-E` as an earth-class robot.

Joining science and cinema together has great potential to make the world a better place. Movies have inspired different types of real-world robots, and a great screenplay is always funnier than a class.

Finally, our research is inspired by three pillars of `sustainability`: 1) reuse/recycling; 2) energy efficiency/green computing; and 3) educational inclusion. We transform existing devices such as Android TV SBCs and robotic vacuums into computational units and mobile robots; use them for our research on energy-efficient robotic software; and make it possible for public Brazilian schools to have access to this kind of technology through lectures about mobile robots and computer programming. Note that Brazil is a diverse and, at the same time, unbalanced country. Usually, public schools struggle to access modern technologies due to their limited budgets. 

---

TBA - Description of the project.

### INSPIRATIONAL PROJECTS

This project is inspired in other attempts, which have been systematically mined from GitHub:

- TBA

### EDUCATIONAL / RESEARCH PROJECTS

Here you can find most relevant `research` and `educational` projects based on and related to `R2-E` robot.

- TBA

## ROBOT PARTS

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
export ROS_BASE_IP="<our vacuum IP>"
ros2 launch r2e_bringup minimal_bringup
```

Now, in your laptop (with your ROS environment sourced), you can check the sensors with ROS topic commands:
```bash
ros2 topic echo /scan
```

You can also make it move `forward` and `backward`:
```bash
python3 fwd_bkw.py
```

Finally, try to teleoperate the robot by using your keyboard:
```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

## CONTRIBUTIONS

We are more than welcome to help us with **R2-E** project and are excited that you're interested in improving it! Please follow this protocol to ensure that your contributions align with the project’s goals and standards.

### 1. Code of Conduct

All contributors are expected to be respectful, inclusive, and mindful of others in the community. Always have in mind that sustainability is our main goal.

### 2. How to Contribute

#### a. Reporting Issues
- If you find a bug or have a feature request, open an issue in the [GitHub Issues](link-to-issues).
- Provide as much detail as possible, including steps to reproduce the bug, the expected behavior, and screenshots if applicable.
  
#### b. Suggesting Features
- Open an issue labeled **Feature Request**. All the tickets for new features will be maintained there. We also keep a Kanban with some kind of sprint. Please, [request](mailto:michelalbonico@utfpr.edu.br) to be added to it.
- Clearly describe the problem your feature addresses and the benefits it will bring to the project.
- We advise to create a branch starting with `feat-` for each new feature.

#### c. Submitting Code
1. **Fork** the repository.
2. Make your changes. 
3. Proceed with a **pull-request** (`PR`) only when you have stable code running.

#### d. Reviewing Process
- Once your `PR` is submitted, a maintainer will review it and provide feedback.
- Be prepared to make revisions if requested.
- After approval, your `PR` will be merged into the main branch.

### 3. Direct communication with the Team

Feel free to reach us out through our [`Discord`](#) channel.
# ROS Tutorial for Starters: As Intuitive As It Gets!

Welcome to the **ROS (Robot Operating System) Tutorial for Starters** — designed to guide you step-by-step from installation to advanced multi-machine setups. This repository compiles essential resources, code examples, and visual aids to make your ROS learning journey intuitive and practical.

---

## 📖 Table of Contents

Set it up
1. [Introduction](#introduction)
2. [🌐 ROS Environment Setup](#ros-environment-setup)
3. [🗂 ROS Filesystem & Package Management](#ros-filesystem--package-management)

What you actually need ⬇️
4. [🧠 Core ROS Concepts: Nodes, Topics, and Communication](#core-ros-concepts-nodes-topics-and-communication)

Bluh Bluh Bluh if you need them they are here. 
6. [🔄 ROS Services, Parameters, and Data Management](#ros-services-parameters-and-data-management)
7. [🔧 ROS Tools for Debugging and Monitoring](#ros-tools-for-debugging-and-monitoring)
8. [🎥 Data Recording, Playback, and Analysis](#data-recording-playback-and-analysis)

Ok nerd...
9. [🌍 Advanced Concepts: Multi-Machine ROS](#advanced-concepts-multi-machine-ros)
10. [Visual Roadmap](#visual-roadmap)

---

## 🧠 Introduction
ROS is a flexible framework for writing robot software. It provides tools, libraries, and conventions to simplify creating complex and robust robot behavior across a wide variety of robotic platforms.

This tutorial aims to break down the learning process into digestible sections for absolute beginners.

---

## 🌐 1. ROS Environment Setup
Setting up your development environment properly is the foundation for working with ROS.

### 1.1 Installing and Configuring ROS
📌 **Tutorial:** [Installing and Configuring Your ROS Environment](https://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment)

**Description:** 
Install ROS on your machine whatever it is
-set up environment variables
-configure your workspace

So your system is ready to develop and run ROS. 

---

## 🗂 2. ROS Filesystem & Package Management
Understand how ROS organizes files and packages—crucial for project structure and navigation.

ROS Packages: Self-contained and reusable modules
Including: Source code (Python/C++ nodes), Configuration files,Launch files, Custom messages and services, Dependencies (other ROS packages)


### 2.1 Navigating the ROS Filesystem
📌 **Tutorial:** [Navigating the ROS Filesystem](https://wiki.ros.org/ROS/Tutorials/NavigatingTheFilesystem)

**Description:** Explore ROS's file and package structure. Learn commands like `roscd`, `rosls`, and `rospack` to navigate efficiently.

### 2.2 Creating a ROS Package
📌 **Tutorial:** [Creating a ROS Package](https://wiki.ros.org/ROS/Tutorials/CreatingPackage)

**Description:** Understand the anatomy of a ROS package. Create your own package with dependencies, setting the stage for scalable projects.

### 2.3 Building a ROS Package
📌 **Tutorial:** [Building a ROS Package](https://wiki.ros.org/ROS/Tutorials/BuildingPackages)

**Description:** Learn the build system (CMake/Catkin), compile your package, and resolve dependencies for smooth development.

---

## 🧠 3. Core ROS Concepts: Nodes, Topics, and Communication
Master the core communication models in ROS for inter-node messaging.

### 3.1 Understanding ROS Nodes
📌 **Tutorial:** [Understanding ROS Nodes](https://wiki.ros.org/ROS/Tutorials/UnderstandingNodes)

**Description:** Understanding **nodes** as individual executables that handle tasks and communicate via topics and services.
Aka. A single executable that performs one task in the robot's brain.

A ROS Node is kinda like a function, but instead of living inside your program, it’s a whole mini-program that runs next to other mini-programs (nodes) — and they all talk to each other.

| **Function (Python/C++)**          | **ROS Node**                                |
|------------------------------------|---------------------------------------------|
| Runs when called                   | Runs **all the time** in the background     |
| Returns a value                    | Sends/receives messages (like broadcasting) |
| Lives inside a program             | **IS** the program                         |
| No idea what other functions are doing | Can talk to other nodes anytime       |

### 3.2 Understanding ROS Topics
📌 **Tutorial:** [Understanding ROS Topics](https://wiki.ros.org/ROS/Tutorials/UnderstandingTopics)

**Description:** Learn about the publish-subscribe messaging model. Topics allow data streams between nodes.

Aka. Publish - Subscribe


Okay, imagine your robot is a bunch of people in a room.

One person yells “THE TEMPERATURE IS 30°C!” 📢

Whoever cares about the temperature just listens.

If you don’t care, you ignore it.

That’s it.

That’s publish-subscribe.


Publisher = the person yelling

Subscriber = the people listening

Topic = the subject they’re yelling about (like “temperature” or “camera pictures”)


Nobody talks directly to anyone. They just yell on their topic and anyone listening picks it up.


Example:
The camera node yells: “Here’s a picture!”
The image processor listens and goes: “Cool, let me work on that.”
The motor? Doesn’t care. Keeps driving.


Super chill. No one needs to know who’s talking or listening.
Easy to add/remove listeners anytime.

### 3.3 Writing a Publisher and Subscriber
📌 **Python:** [Publisher/Subscriber in Python](https://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28python%29)  
📌 **C++:** [Publisher/Subscriber in C++](https://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28c%2B%2B%29)

**Description:** Hands-on coding to create nodes that send (publish) and receive (subscribe) data over topics.

Aka. How you actually do it. 

---

## 🔄 4. ROS Services, Parameters, and Data Management
Learn synchronous communication and parameterization in ROS.

### 4.1 Understanding Services and Parameters
📌 **Tutorial:** [Services and Parameters](https://wiki.ros.org/ROS/Tutorials/UnderstandingServicesParams)

**Description:** Services provide request-response communication. Parameters store runtime configurations—powerful tools for system control.

### 4.2 Creating Custom Message and Service Types
📌 **Tutorial:** [Creating Custom Msg and Srv](https://wiki.ros.org/ROS/Tutorials/CreatingMsgAndSrv)

**Description:** Design your own data structures and services to better fit your project’s requirements.

---

## 🔧 5. ROS Tools for Debugging and Monitoring
Utilize ROS tools to manage, launch, and debug your robot system.

### 5.1 Using rqt_console and roslaunch
📌 **Tutorial:** [rqt_console and roslaunch](https://wiki.ros.org/ROS/Tutorials/UsingRqtconsoleRoslaunch)

**Description:** Learn how to monitor logs with `rqt_console`, and start multiple nodes and parameters with `roslaunch`.

---

## 🎥 6. Data Recording, Playback, and Analysis
Record and replay data for testing, debugging, and offline analysis.

### 6.1 Recording and Playing Back Data
📌 **Tutorial:** [rosbag Data Recording and Playback](https://wiki.ros.org/ROS/Tutorials/Recordingandplayingbackdata)

**Description:** Use `rosbag` to record topic data and replay it for repeated testing or analysis without re-running the robot.

---

## 🌍 7. Advanced Concepts: Multi-Machine ROS
Scale your system by running ROS across multiple machines in a network.

### 7.1 Running ROS Across Multiple Machines
📌 **Tutorial:** [Multiple Machines Setup](https://wiki.ros.org/ROS/Tutorials/MultipleMachines)

**Description:** Learn network configurations that allow ROS nodes to communicate across different computers—a necessity for distributed robotic systems.

---

## 🗺 Visual Roadmap
![ROS Learning Roadmap](flowchart.png)  
*The visual roadmap for this tutorial is available inside the repository.*

---

## Contributing
Pull requests are welcome! If you find something missing or have an intuitive example to add, feel free to contribute.

---

## Star this repo if you find it helpful!
Let's make robotics learning simple and accessible for everyone.

---

**Author:** Gavin Marios Yang

*Happy Coding & Keep Building!* 🤖

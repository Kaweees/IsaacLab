<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->
<div align="left">

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]

</div>

<a href="https://github.com/Kaweees/isaacsim">
   <img alt="NVIDIA Dark Mode Logo" src="assets/img/nvidia-dark.png" align="right" width="150" media="(prefers-color-scheme: dark)">
</a>

<div align="left">
  <h1><em><a href="https://github.com/Kaweees/isaacsim">~isaacsim</a></em></h1>
</div>

<!-- ABOUT THE PROJECT -->

A template for developing production-ready robotics applications on [NVIDIA Isaac Sim](https://developer.nvidia.com/isaac/sim).

### Built With

[![Isaac Sim][Isaac-Sim-shield]][Isaac-Sim-url]
[![ROS2][ROS2-shield]][ROS2-url]
[![C++][C++-shield]][C++-url]
[![Python][Python-shield]][Python-url]

<!-- GETTING STARTED -->

## Getting Started

### Prerequisites

Before attempting to build this project, make sure you have [Docker](https://www.docker.com/products/docker-desktop/) installed on your machine.

### Installation

To get a local copy of the project up and running on your machine, follow these simple steps:

1. Clone the project repository

   ```sh
   git clone https://github.com/Kaweees/isaacsim.git
   cd isaacsim/
   ```

2. Install the environment

   ```sh
   make
   ```

3. Create a new ROS2 workspace

   ```sh
   mkdir -p ros2_ws/src
   cd ros2_ws
   ```

4. Create a new ROS2 package

   ```sh
   ros2 pkg create <package_name> --build-type ament_cmake --dependencies rclcpp rclpy std_msgs # C++
   ros2 pkg create <package_name> --build-type ament_python # Python
   ```

5. Build the package

   ```sh
   colcon build --packages-select <package_name>
   ```

6. Source the project

   ```sh
   source install/setup.bash   # if using bash
   # OR
   source install/setup.zsh    # if using zsh
   ```

7. Run the package node

   ```sh
   ros2 run <package_name> <node_name>
   ```

<!-- PROJECT FILE STRUCTURE -->

## Project Structure

```sh
isaacsim/
├── include/                       - project header files
├── src/                           - project source files
│   └── main.c                     - Entry point, main function
├── CMakeLists.txt                 - CMake build script
├── LICENSE                        - project license
└── README.md                      - you are here
```

## License

The source code for this project is distributed under the terms of the GNU General Public License v3.0, as I firmly believe that collaborating on free and open-source software fosters innovations that mutually and equitably beneficial to both collaborators and users alike. See [`LICENSE`](./LICENSE) for details and more information.

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/Kaweees/isaacsim.svg?style=for-the-badge
[contributors-url]: https://github.com/Kaweees/isaacsim/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/Kaweees/isaacsim.svg?style=for-the-badge
[forks-url]: https://github.com/Kaweees/isaacsim/network/members
[stars-shield]: https://img.shields.io/github/stars/Kaweees/isaacsim.svg?style=for-the-badge
[stars-url]: https://github.com/Kaweees/isaacsim/stargazers

<!-- MARKDOWN SHIELD BAGDES & LINKS -->
<!-- https://github.com/Ileriayo/markdown-badges -->
[Isaac-Sim-shield]: https://img.shields.io/badge/NVIDIA%20Isaac%20Sim-%23008080.svg?style=for-the-badge&logo=nvidia&logoColor=76B900&labelColor=222222&color=76B900
[Isaac-Sim-url]: https://developer.nvidia.com/isaac/sim
[ROS2-shield]: https://img.shields.io/badge/ROS2-%23008080.svg?style=for-the-badge&logo=ros&logoColor=22314E&labelColor=222222&color=22314E
[ROS2-url]: https://www.ros.org/
[C++-shield]: https://img.shields.io/badge/C++-%23008080.svg?style=for-the-badge&logo=c%2B%2B&logoColor=004482&labelColor=222222&color=004482
[C++-url]: https://isocpp.org/
[Python-shield]: https://img.shields.io/badge/Python-%23008080.svg?style=for-the-badge&logo=python&logoColor=FFDD54&labelColor=222222&color=306998
[Python-url]: https://www.python.org/

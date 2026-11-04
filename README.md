<p align="center">
  <img src="Images/dif_gif.gif" alt="The differential robot wrist turning" width="280">
</p>

<h1 align="center">Differential robot wrist</h1>

<p align="center">
  <b>Open-source 3D-printed differential mechanism for a robot wrist.</b><br>
  Two gimbal motors on Spectral Micro BLDC drivers turn its printed bevel gears through timing belts.
</p>

<p align="center">
  <a href="BOM/"><b>BOM</b></a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="STLS/"><b>Print files</b></a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="Images/"><b>Assembly pictures</b></a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://docs.source-robotics.com/Spectral-BLDC-docs/"><b>Driver documentation</b></a>&nbsp;&nbsp;·&nbsp;&nbsp;
  <a href="https://discord.com/invite/prjUvjmGpZ"><b>Discord</b></a>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-143952?style=flat-square" alt="Licence"></a>
  <a href="https://discord.com/invite/prjUvjmGpZ"><img src="https://img.shields.io/discord/1072498136284667955?style=flat-square&logo=discord&logoColor=white&label=discord&color=292B37" alt="Discord"></a>
</p>

<div align="center">

| **2 motors** | **2 drivers** | **11 parts** | **2 belts** |
|:-:|:-:|:-:|:-:|
| GBM5208-75 gimbal motors | Spectral Micro BLDC, on one CAN bus | to print, some of them twice | HTD 3M, 342 mm |

</div>

## Project overview

Due to the high demand to build this differential mechanism, we decided to open source it even at this early stage.

> [!NOTE]
> This is a test fixture that we designed to test the mechanism for our future robots. The project is based on our
> motor driver, the [Spectral Micro BLDC driver](https://source-robotics.com/products/spectral-micro-bldc-controller).

## Start here

| I want to | Go to |
|---|---|
| **1. Get the parts** | [BOM](BOM/) · [Spectral Micro drivers](https://source-robotics.com/products/spectral-micro-bldc-controller) · [CANvas USB to CAN adapter](https://source-robotics.com/products/canvas-usb-to-can-adapter) · [magnets](https://source-robotics.com/products/6x2-5mm-diametrical-neodymium-magnet) · cables: [power](https://source-robotics.com/products/spectral-micro-power-cable), [CAN](https://source-robotics.com/products/spectral-micro-can-cable), [UART](https://source-robotics.com/products/uart-cable) |
| **2. Print the parts** | [print files](STLS/); some parts are printed twice |
| **3. Assemble it** | the [assembly pictures](Images/), in order (the assembly manual is still to do); the screws are in the [BOM](BOM/) |
| **4. Calibrate the drivers** | [calibration](https://docs.source-robotics.com/Spectral-BLDC-docs/latest/05-setup/calibration/), over the UART cable, before you attach the belts |
| **5. Program and test it** | [example code](Example%20codes/) · [Python library](https://github.com/Source-Robotics/Spectral-BLDC-Python) ([guide](https://docs.source-robotics.com/Spectral-BLDC-docs/latest/06-operation/python/)) |

> [!IMPORTANT]
> Before you attach the belts, calibrate the motors: calibration spins each motor in both directions, with
> nothing on its shaft.

## In this repository

| Folder | What is in it |
|---|---|
| [`BOM`](BOM/) | the bill of materials: the screws, the two motors, the bearings, the belts and the electronics, with shop links |
| [`STLS`](STLS/) | the 11 printed parts: the bevel gears with their backplates and shaft, the pulley, the gear hub, the motor holder, the outer shell, the magnet shaft and a spacer |
| [`Images`](Images/) | the assembly pictures, `img1` to `img15`, and the animation at the top of this page |
| [`Example codes`](Example%20codes/) | `diferential_test.py`, which turns the two motors in opposite directions over CAN and prints their speed, current and position |

## Community

Ask in [Discussions](https://github.com/orgs/Source-Robotics/discussions), chat on
[Discord](https://discord.com/invite/prjUvjmGpZ), report a bug in
[Issues](https://github.com/Source-Robotics/Differential-robot-wrist/issues), and follow Source Robotics:

[![Discord](https://img.shields.io/discord/1072498136284667955?style=flat-square&logo=discord&logoColor=white&label=discord&color=143952)](https://discord.com/invite/prjUvjmGpZ)
[![Discussions](https://img.shields.io/badge/discussions-ask_a_question-143952?style=flat-square&logo=github&logoColor=white)](https://github.com/orgs/Source-Robotics/discussions)
[![YouTube](https://img.shields.io/badge/youtube-%40source--robotics-143952?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@source-robotics)
[![Instagram](https://img.shields.io/badge/instagram-%40source__robotics-143952?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/source_robotics/)
[![X](https://img.shields.io/badge/x-%40SourceRobotics-143952?style=flat-square&logo=x&logoColor=white)](https://x.com/SourceRobotics)
[![LinkedIn](https://img.shields.io/badge/linkedin-Source_Robotics-143952?style=flat-square&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUyaC0zLjU1NHYtNS41NjljMC0xLjMyOC0uMDI3LTMuMDM3LTEuODUyLTMuMDM3LTEuODUzIDAtMi4xMzYgMS40NDUtMi4xMzYgMi45Mzl2NS42NjdIOS4zNTFWOWgzLjQxNHYxLjU2MWguMDQ2Yy40NzctLjkgMS42MzctMS44NSAzLjM3LTEuODUgMy42MDEgMCA0LjI2NyAyLjM3IDQuMjY3IDUuNDU1djYuMjg2ek01LjMzNyA3LjQzM2MtMS4xNDQgMC0yLjA2My0uOTI2LTIuMDYzLTIuMDY1IDAtMS4xMzguOTItMi4wNjMgMi4wNjMtMi4wNjMgMS4xNCAwIDIuMDY0LjkyNSAyLjA2NCAyLjA2MyAwIDEuMTM5LS45MjUgMi4wNjUtMi4wNjQgMi4wNjV6bTEuNzgyIDEzLjAxOUgzLjU1NVY5aDMuNTY0djExLjQ1MnpNMjIuMjI1IDBIMS43NzFDLjc5MiAwIDAgLjc3NCAwIDEuNzI5djIwLjU0MkMwIDIzLjIyNy43OTIgMjQgMS43NzEgMjRoMjAuNDUxQzIzLjIgMjQgMjQgMjMuMjI3IDI0IDIyLjI3MVYxLjcyOUMyNCAuNzc0IDIzLjIgMCAyMi4yMjIgMGguMDAzeiIvPjwvc3ZnPg%3D%3D)](https://www.linkedin.com/company/source-robotics/)
[![Blog](https://img.shields.io/badge/blog-source--robotics.com-143952?style=flat-square&logo=rss&logoColor=white)](https://source-robotics.com/blogs/blog)

## Safety, liability and disclaimer

1. The software and hardware are still in development and may contain bugs, errors, or incomplete features.
2. Users are encouraged to use this software and hardware responsibly and at their own risk.

## Licensing

Project is under the [MIT License](LICENSE).

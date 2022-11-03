Back: [Project-Overview](./../README.md)

# Hack Challenge "Let’s Play OpenStreepMap and CARLA"

## What is CARLA?

[CARLA](https://github.com/carla-simulator/carla) is an open-source simulator for autonomous driving research. CARLA has been developed from the ground up to support development, training, and validation of autonomous driving systems. In addition to open-source code and protocols, CARLA provides open digital assets (urban layouts, buildings, vehicles) that were created for this purpose and can be used freely. The simulation platform supports flexible specification of sensor suites and environmental conditions.

## How to get it ?
Possible options:
 - Got to release page of [CARLA-Releases](https://github.com/carla-simulator/carla/releases) and download it for your operating system.
   Native packages are available for
    - Windows
    - Ubuntu
 - Also Docker-Images are available. Follow the [instructions](https://carla.readthedocs.io/en/latest/build_docker/).
 - **Best option**: In addition for the hackathon a compressed package with two simulators has been created (Windows only).

### Content of the simulator package (provided)

| Simulator                                                                                               | Example Projects |
| ------------------------------------------------------------------------------------------------------- | ---------------- |
| [AirSim with CityEnvironment (v1.8.1)](https://github.com/microsoft/AirSim/releases/tag/v1.8.1-windows) | Hello, Driving   |
| [CARLA (v0.9.13)](https://github.com/carla-simulator/carla/releases/tag/0.9.13)                         | Hello, Driving   |

* Portable Python 3.7
* Portable Visual Studio Code
* Scripts and helper tooling with task application

### Unpack the package

Get it from [here](https://github.com/Eclipse-SDV-Hackathon-BCX/hackchallenge-lets-play-osm-and-carla/releases/tag/v1.0.0-pre). 
The package is quite huge. All compressed parts together 6.3 GB and uncompressed **19.5GB**. Make sure that you have enough free diskspace for downloading an uncompressing the archive. The archive format is 7z. A installer is provided on the release page or can be downloaded and installed from [official website](https://www.7-zip.org/download.html).

* right-click on ```*.7z.001``` file and choose ```7-Zip --> Extract files...```

![dialog_7zip](https://user-images.githubusercontent.com/116635980/199595819-4fbb6905-500c-4e3a-94ac-280a0e83bdad.png)

### Directory and file structure

```sh
.
├─ .vscode/extensions.json                   # Recommended list of plugins for visual studio code
├─ getting_started/                          #
│  ├─ airsim/projects/                       # Contains example projects for AirSim simulator
│  │  ├─ 1-example-hello-airsim/*            # Project example hello-airsim for AirSim simulator
│  │  └─ 2-example-driving-airsim/*          # Project example driving-airsim for AirSim simulator
│  └─ carla/projects/                        # Contains example projects for CARLA simulator
│     ├─ 1-example-hello-carla/*             # Project example hello-carla for CARLA simulator
│     └─ 2-example-driving-carla/*           # Project example driving-carla for CARLA simulator
├─ python/3_7_3/*                            # Portable version of python 3.7.3
├─ scripts/                                  #
│  ├─ Airsim.dist.yaml                       # Contains helper tasks using the AirSim simulator and python package dependencies
│  ├─ Carla.dist.yaml                        # Contains helper tasks using the CARLA simulator and python package dependencies
│  └─ run_simulator.py                       # Basic python script helping with calling the simulators binaries
├─ simulation/                               #
│  ├─ airsim/*                               # AirSim simulator application
│  └─ carla/*                                # CARLA simulator application 
├─ task/*                                    # Task application
├─ vscode/*                                  # Portable Visual Studio Code application
├─ OpenConsoleHere.bat                       # Opens a new console window
├─ OpenVsCode.bat                            # Opens the portable visual studio code
├─ README.md                                 # Information about the package
└─ Taskfile.yaml                             # Root-task file including sub-task files
```

## How to run task

Open a new terminal (console) window in the root directory.
Run one of the following  ```task <task_name>``` like ```task carla:test:driving```


```sh
task: Available tasks for this project:
* airsim:install:example_driving:       Install deps 2-example-driving-airsim.
* airsim:install:example_helloworld:    Install deps 1-example-hello-airsim.
* airsim:run:example_driving:           Runs 2-example-driving-airsim.
* airsim:run:example_helloworld:        Runs 1-example-hello-airsim.
* airsim:sim:run:                       Starts a new airsim simulation instance.
* airsim:sim:stop:                      Stops any running airsim simulation instance.
* airsim:test:driving:                  Test-Run project 2-example-driving-airsim with Simulator.
* airsim:test:helloworld:               Test-Run project 1-example-hello-airsim with Simulator.
* carla:install:example_driving:        Install deps 2-example-driving-carla.
* carla:install:example_helloworld:     Install deps 1-example-hello-carla.
* carla:run:example_driving:            Runs 2-example-driving-carla.
* carla:run:example_helloworld:         Runs 1-example-hello-carla.
* carla:sim:run:                        Starts a new carla simulation instance.
* carla:sim:stop:                       Stops any running carla simulation instance.
* carla:test:driving:                   Test-Run project 2-example-driving-carla with Simulator.
* carla:test:helloworld:                Test-Run project 1-example-hello-carla with Simulator.
* default:                              Lists all possible tasks.
* vscode:open:                          Open Visual Studio Code.
```

## How install the demos

```sh
task: Available tasks for this project:
* airsim:install:example_driving:       Install deps 2-example-driving-airsim.
* airsim:install:example_helloworld:    Install deps 1-example-hello-airsim.
* carla:install:example_driving:        Install deps 2-example-driving-carla.
* carla:install:example_helloworld:     Install deps 1-example-hello-carla.
```

## How to run or stop the simulators

```sh
task: Available tasks for this project:
* airsim:sim:run:                       Starts a new airsim simulation instance.
* airsim:sim:stop:                      Stops any running airsim simulation instance.
* carla:sim:run:                        Starts a new carla simulation instance.
* carla:sim:stop:                       Stops any running carla simulation instance.
```

## How to run (test) the demos in the simulator

```sh
task: Available tasks for this project:
* airsim:test:driving:                  Test-Run project 2-example-driving-airsim with Simulator.
* airsim:test:helloworld:               Test-Run project 1-example-hello-airsim with Simulator.
* carla:test:driving:                   Test-Run project 2-example-driving-carla with Simulator.
* carla:test:helloworld:                Test-Run project 1-example-hello-carla with Simulator.
```

## How to create a new project

t.b.d.

## Setting up development environment for python and vscode

### Install recommended visual studio code plugins

### How to debug in vscode?

## Helpful information

- Links to carla repo
  - Link to Python API
  - Link to Settings
  - Link to tutorials

## Hints, pointers and common pitfalls (we discovered)

## Using MacOS, Using Docker, Using Unix

Next: [Step 2: Investigate data export from OpenStreetMap and import in CARLA](./step-2-oh-my-osm.md)

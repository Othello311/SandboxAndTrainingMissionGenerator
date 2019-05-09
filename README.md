<p align="center">
<a href="https://github.com/7Cav/SandboxAndTrainingMissionGenerator/releases/latest"><img src="https://img.shields.io/github/release/7Cav/SandboxAndTrainingMissionGenerator.svg?style=for-the-badge&label=Release%20Build" alt="Release Build Version"></a>
<a href="https://github.com/7Cav/SandboxAndTrainingMissionGenerator/releases/latest"><img src="https://img.shields.io/github/downloads/7cav/SandboxAndTrainingMissionGenerator/total.svg?style=for-the-badge&label=Downloads" alt="Downloads"></a>
<a href="https://travis-ci.org/7Cav/SandboxAndTrainingMissionGenerator"><img src="https://img.shields.io/travis/7Cav/SandboxAndTrainingMissionGenerator.svg?style=for-the-badge&logo=Travis-CI" alt="Build"></a>
</p>

This is a mission generator script built to quickly and reliable build sandbox and training missions for the 7th Cavalry Gaming.

# Requirements
* Python3

## Install
- **Windows:** 
  [Download and install](https://www.python.org) or `choco install python3`
- **Linux:** `sudo apt-get install python3`

# How to run
- (Soon) Modfify the `properties.ini` if needed.
- Modify the script Globals in ``build.py`` if needed.
- Modify the Templates if needed. (See below for requirements.) 
- Run the script<br />
  Windows: `py build.py -b sandbox` or ` py build.py -b training`<br />
  Linux: `python3 build.py -b sandbox` or ` python3 build.py -b training`

# Setting up a sandbox template
- Mission file most be unbinirized.
- Script will primarily use the Generic template.<br />
  A custom template can be used to create one the folowing name is required:<br />
  `Template_Altis.Altis` or `Template_MyIsland.MyIsland`<br />
  The island need to be placed in the `./Template/sandbox/` directory.
- To allow the script to set the Respawn use the following coordinates:<br />
  `position[]={20.200001,25.200001,20.200001};` 
- Unit placement is recommended to be set in the lower left corner on short grid `00 00`.

# Setting up a training mission (WIP)
- Training missions name need to be in the following format `[My_Training_Mission]_DEVBUILD.[Island_Name]`
- Training missions need to placed in `./template/training/`.
- Additional training mission scripts need to be placed in the mission `./scripts/` folder.
- Adjustments to `init.sqf` is required to be inside `init.sqf`. Only add mission essensials. (It will be merged i to the `init.sqf`) 
- Adjustments to `description.ext` is require to be inside `description.ext`. Only add mission essensials. (It will be merged i to the `description.ext`) 

# AMR-IF-UI: GUI
<!-- TOC -->

- [UI Elements and Functions](#ui-elements-and-functions)
    - [*Sidenav*](#sidenav)
- [*Viewer*](#viewer)
- [*Controller*](#controller)
- [*Command kind*](#command-kind)

<!-- /TOC -->
## UI Elements and Functions

### *Sidenav*

<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0z" fill="none"/><path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/></svg>

Sidenav is located on the left side of AMR-IF-UI and has five icons on a
gray background.

| name | description |
|:---|:---|
| <span class="material-icons">home</span> Home icon | Return to home view(Sidenav, Viewer, and Contoroller). |
| Robot Setting icon | Set robot's name, color, namespace, IP address and port number for each robot. |
| Pose Setting icon | Set Pose's name, color, position and orientation for each pose. <br>This pose setting is used only for displaying in Viewer. |
| CmdList Setting icon | Set CmdList's id, cmd, params, OK_nextid, NG_nextid for each command. <br>Cmd is required. <br>Id, OK_nextid and NG_nextid is optional. <br>Some cmds need params. |
| Viewer Setting icon | Set resolution, fontSize, poseMarkerSize and rotation. <br>Resolution, fontSize and poseMarkerSize change the viewer looks. <br> Rotation can be selected 0 to 3 and rotates the viewer 90 degrees each. |

Press "Export" at the top right of the screen to save each setting to a file. Press "Import" to load the settings from a file. Press “Clear” to delete the settings.


## *Viewer*

Viewer is located in the center of AMR-IF-UI and displays the map, pose, robot's current position, and planned path.


## *Controller*

Controller is on the right side of AMR-IF-UI, and the robot name, icons, and buttons are displayed with the background color of the selected robot's setting color. If there are NO robot settings, controller will NOT be displayed. You can use the button on the controller to send command to the selected robot.

| name | description |
|:---|:---|
| Robot name | Display the name of selected robot. |
| Robot icon | Change the operating robot. Select a robot from the dialog. |
| Connection icon | Display connection status. <br>If connected, display connect icon. <br>If disconnected, display disconnect icon.  |
| CmdList Execution button | Run cmdlist. Select a cmdlist and starting index from the dialog. |
| Command Execution button | Run command. Select a command and options if necessary from the dialog. |
| run_nav command button | Run "run_nav". Select a mapfile name from the dialog.  |
| kill_nav command button | Run "kill_nav". |
| set_pose command button | Run "set_pose". Select a mapfile name and pose name at robot current pose name from the dialog. |
| goto command button | Run "goto". Select a mapfile name and goal pose name from the dialog. |
| cancel command button | Run "cancel". |
| CmdList 0 Shortcut button | Run id0 cmdlist from the beginning. |
| CmdList 1 Shortcut button | Run id1 cmdlist from the beginning. |
| CmdList 2 Shortcut button | Run id2 cmdlist from the beginning. |


# Viewer Key Control

| Key | function |
|:---|:---|
| Arrow Right | right move |
| Arrow Left | left move |
| Arrow Up | up move |
| Arrow Down | down move |
| Page Up | zoom in|
| Page Down | zoom out |
| Home | default position |
| End | default position |

Fine adjustment possible while holding down the Shift key.


# Command

AMR-IF-UI supports some commands. These commands are defined in "src / assets / configs / config.json".


## *Command kind*

AMR-IF-UI supports five single commands and one mixed command. Single commands are "run_nav", "kill_nav", "set_pose", "goto" and "cancel". Mixed command is "cmdlist".

* Single commands

| cmd | parameter | description |
|:---|:---|:---|
| run_nav | mapfile_name | The robot starts the autonomous movement function. Execute only once before starting autonomous movement. |
| kill_nav | - | The robot ends the autonomous movement function. Run run_nav to resume autonomous movement. |
| set_pose | mapfile_name, <br>pose_name | Notify the current position to the robot at the start of autonomous movement. |
| goto | mapfile_name, <br>goal_name | Instruct the robot to move. |
| cancel | - | Stop moving. |

* Mixed command

| cmd | parameter | description |
|:---|:---|:---|
| cmdlist | start_index | A series of commands. Commands are executed in order. When the command completes, execute the following command. If OK_nextid is specified, execute the command of OK_nextid. If an error occurs in the command, the CmdList ends. But NG_nextid is specified, execute the command of NG_nextid. |

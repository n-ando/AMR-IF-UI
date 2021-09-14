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
| <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0z" fill="none"/><path d="M10 20v-6h4v6h5v-8h3L12 3 2 12h3v8z"/></svg> Home icon | Return to home view(Sidenav, Viewer, and Contoroller). |
| 
<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0z" fill="none"/><path d="M17 5H3c-1.1 0-2 .89-2 2v9h2c0 1.65 1.34 3 3 3s3-1.35 3-3h5.5c0 1.65 1.34 3 3 3s3-1.35 3-3H23v-5l-6-6zM3 11V7h4v4H3zm3 6.5c-.83 0-1.5-.67-1.5-1.5s.67-1.5 1.5-1.5 1.5.67 1.5 1.5-.67 1.5-1.5 1.5zm7-6.5H9V7h4v4zm4.5 6.5c-.83 0-1.5-.67-1.5-1.5s.67-1.5 1.5-1.5 1.5.67 1.5 1.5-.67 1.5-1.5 1.5zM15 11V7h1l4 4h-5z"/></svg> Robot Setting icon | Set robot's name, color, namespace, IP address and port number for each robot. |
| 
<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg> Pose Setting icon | Set Pose's name, color, position and orientation for each pose. <br>This pose setting is used only for displaying in Viewer. |
| 
<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0z" fill="none"/><path d="M3 13h2v-2H3v2zm0 4h2v-2H3v2zm0-8h2V7H3v2zm4 4h14v-2H7v2zm0 4h14v-2H7v2zM7 7v2h14V7H7z"/></svg> CmdList Setting icon | Set CmdList's id, cmd, params, OK_nextid, NG_nextid for each command. <br>Cmd is required. <br>Id, OK_nextid and NG_nextid is optional. <br>Some cmds need params. |
| 
<svg xmlns="http://www.w3.org/2000/svg" enable-background="new 0 0 24 24" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><g><path d="M0,0h24v24H0V0z" fill="none"/><path d="M19.14,12.94c0.04-0.3,0.06-0.61,0.06-0.94c0-0.32-0.02-0.64-0.07-0.94l2.03-1.58c0.18-0.14,0.23-0.41,0.12-0.61 l-1.92-3.32c-0.12-0.22-0.37-0.29-0.59-0.22l-2.39,0.96c-0.5-0.38-1.03-0.7-1.62-0.94L14.4,2.81c-0.04-0.24-0.24-0.41-0.48-0.41 h-3.84c-0.24,0-0.43,0.17-0.47,0.41L9.25,5.35C8.66,5.59,8.12,5.92,7.63,6.29L5.24,5.33c-0.22-0.08-0.47,0-0.59,0.22L2.74,8.87 C2.62,9.08,2.66,9.34,2.86,9.48l2.03,1.58C4.84,11.36,4.8,11.69,4.8,12s0.02,0.64,0.07,0.94l-2.03,1.58 c-0.18,0.14-0.23,0.41-0.12,0.61l1.92,3.32c0.12,0.22,0.37,0.29,0.59,0.22l2.39-0.96c0.5,0.38,1.03,0.7,1.62,0.94l0.36,2.54 c0.05,0.24,0.24,0.41,0.48,0.41h3.84c0.24,0,0.44-0.17,0.47-0.41l0.36-2.54c0.59-0.24,1.13-0.56,1.62-0.94l2.39,0.96 c0.22,0.08,0.47,0,0.59-0.22l1.92-3.32c0.12-0.22,0.07-0.47-0.12-0.61L19.14,12.94z M12,15.6c-1.98,0-3.6-1.62-3.6-3.6 s1.62-3.6,3.6-3.6s3.6,1.62,3.6,3.6S13.98,15.6,12,15.6z"/></g></svg> Viewer Setting icon | Set resolution, fontSize, poseMarkerSize and rotation. <br>Resolution, fontSize and poseMarkerSize change the viewer looks. <br> Rotation can be selected 0 to 3 and rotates the viewer 90 degrees each. |

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

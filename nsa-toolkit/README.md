## NSA Toolkit
Docker Image with PlayOnLinux, Python and leaked NSA Tools

### Requirements
To see the display, first run 
_ xhost +local:root _

### Usage:
docker run -it --privileged -e DISPLAY=$DISPLAY \
--device /dev/dri/card0:/dev/dri/card0 \
-v /tmp/.X11-unix:/tmp/.X11-unix:rw \
-v $HOME/payloads:/home/pol/.PlayOnLinux/wineprefix/nsa/drive_c/exploits:rw \
--name nsa-toolkit evait/nsa-toolkit

To start the toolkit, follow these steps:
1. start the machine
2. go to "Configure"
3. Select "nsa" at the left side and choose the tab "Wine"
4. Click on "Command prombt"
5. type "C:", press enter
6. start NSA Fuzzbunch with "python C:/nsa/windows/fb.py"

##### Notice:
Payloads are loaded from the "C:/exploits" folder.
The corresponding folder is given in the last "-v" parameter

I have a small USB powered HDMI screen attached to my 3D printer enclosure (specifically an [Elecrow 7 Inch HDMI Monitor](https://www.amazon.co.uk/Elecrow-Monitor-Display-1024X600-Raspberry/dp/B076J8ZWFF/ref=sr_1_5?keywords=elecrow&qid=1557441569&s=gateway&sr=8-5)), this is how I set it up to automatically turn on when the Printer connects to Octoprint and turn off when it's disconnected, I use uhubctl to turn off the USB ports on the Raspberry Pi that the screen is connected to.

First you must install uhubctl by mvp, which can be found [here.](https://github.com/mvp/uhubctl) Follow the installation instructions that are contained in that repo. In short, install the required libraries, git clone the repo onto your octoprint installation, then run the make file. 

I have then included the code snippets in the 'config.yaml' file that you should include in your config.yaml file which can be found in /home/pi/.octoprint/ This uses the built in Octoprint events function to trigger the commands when the printer is connected/disconnected from Octoprint. You may need to modify the command depending on where you install uhubctl.

![GUI image](/images/GUIbuttons.png)

It can also be added to the GUI in the System Command Editor plugin, this will allow you to have buttons on the 'system' drop down box to turn on and off the screen. If you do this you will need to copy the file 'octoprint-screencontrol' into the /etc/sudoers.d directory. This will allow the command to be run from the GUI. An example command can be seen below.

![Edit command box](/images/editcommand.png)

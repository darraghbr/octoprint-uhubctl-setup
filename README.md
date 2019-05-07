I have a small USB powered HDMI screen attached to my 3D printer enclosure, this is how I set it up to automatically turn on when the Printer connects to Octoprint and turn off when it's disconnected, I use a TP-Link smart plug to power the printer itself. 

First you must install uhubctl by mvp, which can be found [here.](https://github.com/mvp/uhubctl) Follow the installation instructions that are contained in that repo.

I have then included the code snippets in the 'config.yaml' file that you should include in your config.yaml file which can be found in /home/pi/.octoprint/ This uses the built in Octoprint events function to trigger the commands when the printer is connected/disconnected from Octoprint. You may need to modify the command depending on where you install uhubctl. 

It can also be added to the GUI in the System Command Editor plugin, this will allow you to have buttons on the drop down box to turn on and off the screen. If you do this you will need to copy the file 'octoprint-screencontrol' into the /etc/sudoers.d directory. This will allow the command to be run from the GUI. 

![GUI image](/images/GUIbuttons.png)
![Edit command box](/images/editcommand.png)

I have a small USB powered HDMI screen attached to my 3D printer enclosure, this is how I set it up to automatically turn on when the Printer connects to Octoprint and turn off when it's disconnected, I use a TP-Link smart plug to power the printer itself. 

First you must install uhubctl by mvp, which can be found [here.](https://github.com/mvp/uhubctl) follow the installation instructions that are contained in that repo.

I have then included the code snippets in the 'config.yaml' file that you should include in your config.yaml file which can be found in /home/pi/.octoprint/ This uses the built in Octoprint events function to trigger the commands when the printer is connected/disconnected from Octoprint.

It can also be added to the GUI in the System Command Editor plugin, this will allow you to have buttons on the drop down box to turn on and off the screen. If you do this you will need to add uhubctl to the sudoers file with the NOPASSWD option so that the GUI will be able to execute the command. 

![GUI image](/images/GUIbuttons.png)

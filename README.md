# i3-config
Configuration files for the i3 window manager

## i3 Configuration File
The configuration file can be found under the following path. Open it with a text editor like nano or vim:
```
~/.config/i3/config
```

It might be a good idea to change the keys to change focus as well as the keys to move a focused window to match the standard vim navigation keys (`h`,`j`,`k`,`l` instead of `j`,`k`,`l`,`;`). In this case you need to comment the *split in horizontal orientation* command out to avoid a conflict of the same command being used for two functions. 

You can add commands to be executed by putting `exec` in front of them. 
* An automatic screen rotation can for example be realised by adding the line `exec xrandr --output HDMI-1 --rotate left` to the config file. Just choose the appropriate output and rotation direction for your case. 
* Another example is an automatic change of the keyboard map to the German layout by adding `exec setxkbmap de`. 

## i3 Status Bar Configuration File
There are several locations that are checked for a configuration file. 
* `~/.config/i3status/i3status.conf` (for the current user, checked first)
* `/etc/i3status.conf` (for all users, checked second)

After a fresh installation of the i3 window manager, only the configuration file for all users exists. Therefore, we have to create the directory in the home directory of the current user and then copy the general configuration file into the new folder before customising it for the current user. 
```
mkdir ~/.config/i3status
cp /etc/i3status.conf ~/.config/i3status/config
```

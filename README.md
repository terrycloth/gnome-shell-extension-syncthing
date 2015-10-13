# Syncthing Gnome Shell extension

This is a simple shell extension for Gnome 3.
It features a small symbolic Syncthing icon that opens a menu with
- an on/off switch for starting/stopping Syncthing
- a button for opening the Web user interface (http://localhost:8384 or some other configurable URI)
- a list of folders that are managed by Syncthing

## Requirements
This extension uses the **user service** management facilities of systemd. The
[Syncthing documentation](http://docs.syncthing.net/users/autostart.html#how-to-use-the-user-instance)
has information about how to set this up. Please make sure that you have the
user units installed correctly, otherwise the on/off switch will not work.

## Installation

The install script will make sure all the necessary files are copied to the
correct place for you.
```sh
./install.sh
```

After that, all you have to do is enable Syncthing Icon in your list of shell
extensions. Gnome Shell comes with a simple GUI application that lists all the
extensions that you have currently installed, but for some reason it does not
normally show up when you search the application menu. You have to launch it
from the terminal, or from the Run Commands dialog (`Alt-F2`). Enter this:
```sh
gnome-shell-extension-prefs &
```

Or, if you have the Gnome Tweak Tool installed, you can launch that and go to
the Extensions tab.

Once you see the list of extensions, look for "Syncthing icon," and click to
set the switch to ON.

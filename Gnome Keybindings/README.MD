Back Up: 
dconf dump /org/gnome/desktop/wm/keybindings/ > ~/Documents/wm-keybindings.dconf.bak
dconf dump /org/gnome/settings-daemon/plugins/media-keys/ > ~/Documents/media-keys-keybindings.dconf.bak

Restore:
dconf load /org/gnome/desktop/wm/keybindings/ < ~/Documents/wm-keybindings.dconf.bak
dconf load /org/gnome/settings-daemon/plugins/media-keys/ < ~/Documents/media-keys-keybindings.dconf.bak

#############################################################################################
1. Check paths to where keybindings are stored in GNOME:
dconf dump / | grep keybinding

All of my custom keybindings were in the following to paths:
/org/gnome/desktop/wm/keybindings
/org/gnome/settings-daemon/plugins/media-keys/

2. Exporting (or making a backup):
To export as .bak files saved in, say ~/Documents, use

dconf dump /org/gnome/desktop/wm/keybindings/ > ~/Documents/wm-keybindings.dconf.bak


dconf dump /org/gnome/settings-daemon/plugins/media-keys/ > ~/Documents/media-keys-keybindings.dconf.bak

3. Importing keybindings after a fresh install:

Say, the .bak file is under ~/Docouments

dconf load /org/gnome/desktop/wm/keybindings/ < ~/Documents/wm-keybindings.dconf.bak


dconf load /org/gnome/settings-daemon/plugins/media-keys/ < ~/Documents/media-keys-keybindings.dconf.bak

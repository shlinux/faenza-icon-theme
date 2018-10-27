Installation
============
Run the `./INSTALL` script to choose the distribution logo (Ubuntu, by default) and the Gnome menu icon. If run as root, the script will copy the iconsets to `/usr/share/icons` to made them available to all users. Some default icons used by Rhythmbox may be also replaced.
Run `./UNINSTALL` as root to restore defaults icons.

Launchpad PPA
=============
Faenza icon theme is available to install for Ubuntu users via a PPA repository. Open a terminal and run:

	sudo add-apt-repository ppa:tiheum/equinox

	sudo apt-get update && sudo apt-get install faenza-icon-theme

You can also install the `faenza-icons-mono` package. It replace the 22x22 squared icons for Deluge, Exaile, Fusion Icon, iBus and Kupfer by their monochromatic counterpart.

Tips
====
* Ubuntu 10.10: the Unity panel has a strange behavior with some icons compared with the previous version (and Gnome 2 panels of course), especially with user menu and battery state icons. You might use one of the to new themes instead of the classic ones: Faenza-Ambiance is suitable with dark panel and toolbars (inherits Faenza-Darkest theme), Faenza-Radiance with light panel and controls (inherits Faenza theme).
* Some applications are configured to always use the same icon regardless of the selected theme. To display the Faenza icon, edit as root the `/usr/share/applications/application_name.desktop` file and locate the line beginning with `Icon=`. Replace the fullpath icon name by the one of the Faenza icon (usually, the name of the application itself) without the extension. Don't forget to make a backup before changing one of those files. E.g. Vim desktop file is `/usr/share/applications/gvim.desktop`. Some desktop files can be located in `/usr/local/share/applications` or in your `~/.local/share/applications` folder (e.g. Steam desktop file is somewhere in `~/.local/share/applications/wine`). Here is a partial list: emacs23, desura, gcolor2, bluefish, hardinfo, setroubleshoot, gufw, pithos, vim, rssowl, netbeans, gazpacho, guake, all commercial games, etc
* If you want to use the new Gnome contact application, edit its desktop file (`/usr/share/applications/gnome-contacts.desktop`) to use the specific (and beautiful) icon named gnome-contacts ;)

Known issues
============
* Java applications like jDownloader or Frostwire doesn't support themes even if you edit the corresponding `.desktop` files.
* A lots of applications does not currently support support monochromatic tray icon (deluge, gnome-do, skype, spotify, goldendict) without changing the application icon itself. Please report issue to the developers.


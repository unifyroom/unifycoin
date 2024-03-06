
Debian
====================
This directory contains files used to package unfyd/unfy-qt
for Debian-based Linux systems. If you compile unfyd/unfy-qt yourself, there are some useful files here.

## unfy: URI support ##


unfy-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install unfy-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your unfy-qt binary to `/usr/bin`
and the `../../share/pixmaps/unfy128.png` to `/usr/share/pixmaps`

unfy-qt.protocol (KDE)


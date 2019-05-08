
Debian
====================
This directory contains files used to package CBSLd/CBSL-qt
for Debian-based Linux systems. If you compile CBSLd/CBSL-qt yourself, there are some useful files here.

## CBSL: URI support ##


CBSL-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install CBSL-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your CBSLqt binary to `/usr/bin`
and the `../../share/pixmaps/CBSL128.png` to `/usr/share/pixmaps`

CBSL-qt.protocol (KDE)


witchres
=========

X Windows/Windows Mame Emulator Resolution Switcher


See output of "switchres -h" for best information on command line settings.

Basic config file example is in examples/switchres.conf

==========================
Simple Modeline generation:
==========================

switchres --calc pacman
switchres 384 288 60.61 --monitor d9800


=====================
Running games in MAME:
=====================

switchres pacman --monitor cga
switchres frogger --ff --redraw --nodoublescan --monitor d9200 

# ArcadeVGA files in Windows 
switchres tron --resfile extra/ArcadeVGA.txt --resfile ~/modes.txt

# Soft15Khz in Windows reading registry modelines
switchres tron --soft15khz

=================================
Running games for other emulators:
=================================

switchres a2600 --emulator mess --rom /path/to/ROM\ File.bin --args -verbose -sdlvideofps

Anything after --args is passed to the emulator, in this case 'mess'.

The game rom becomes the game system, even for other emulators, mess is still used to get the games
correct resolution.

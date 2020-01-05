ALTTP Room Autosplits
=====================

This repo contains a Livesplit USB2SNES Auto Splitter config file
and a Livesplit split definition for room by room splits for ALTTP
NMG Any%.

Usage
-----

Download and setup Livesplit, QUsb2Snes, and the USB2SNES Auto
Splitter according to the instructions on each of their pages (see
links at bottom).

In Livesplit, right click, go to Open Splits > From File... and open
`alttp-splits.lss` from this repo. Now add the USB2SNES Auto Splitter
component to your layout (see Troubleshooting section below), and
edit its settings. For the config file, open
`alttp-room-autosplit-config.json` from this repo. Make sure the
component is connected to QUsb2Snes by clicking Autodetect and the
name of your device should appear in the textbox next to the button.

You'll also want to make sure your layout is using the Subsplits
component instead of the Splits component so that the subsplits
display properly.

Note that the autosplitter component should add a red/yellow/green
line showing the status of its connection to QUsb2Snes.

Everything should be good to go at this point! Start a new save in
game and the splits should start automatically as soon as you select
the save.

Troubleshooting
---------------

* The Auto Splitter component spams modal dialogs as soon as I add
it, saying that an empty config file name is not allowed.

    * You'll have to fight the Auto Splitter component to get the config
    file specified. Keep spamming the actions you need to do, hitting OK
    to dismiss the dialog every time it appears.  Holding down Enter
    briefly may also help.

Technical Details
-----------------

These splits watch the values of a few different memory addresses:

* 0xA0 - current underworld room
* 0xA9 and 0xAA - current quadrant of underworld room (needed for
multi-room supertiles)
* 0x0100 - Link's current sprite (useful for post-boss cutscenes)
* 0x040A - current overworld area
* 0x0AA4 - sprite graphics index (used to detect overworld vs.
underworld)


Links
-----

* [LiveSplit](https://livesplit.org)
* [QUsb2Snes](https://skarsnik.github.io/QUsb2snes/)
* [USB2SNES Auto Splitter](https://github.com/Skarsnik/LiveSplit.USB2SNESSplitter/releases)


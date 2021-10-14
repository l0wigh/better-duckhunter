Better Duck Hunter
==========

Converts a USB Rubber ducky script into a Kali Nethunter friendly format for the HID attack

Original code and concept by @binkybear

Quack

This is the updated version

The original code was ported to python 3 by the nethunter team

This patch made it work completely.


### Running Duck Hunter
```
duckhunter.py -l us input.txt output.sh
```
Supports multiple languages: us, fr, de, es, sv, it, uk, ru, dk, no, pt, be

Output file can be run as a regular shell file on Nethunter devices.

You'll need to run the output with the android terminal (not kali).

The easiest way is by moving the output to /data/local/nhsystem/kali-arm64/ (/ in kali).

Give execution rights with chmod.

Run the script with android terminal.

Obviously you need to change the settings in USB Arsenal for HID before launching the script.

### Keyboard Commands

Here is a list of commands that will work with your Duck Hunter input file for conversion:
```
DELAY 1000
```
In miliseconds, 1000 is equal to 1 second
```
COMMAND SPACE
```
Apple command key with space will load spotlight
```
GUI r
```
Windows + R key for run
```
WIN7CMD
```
Load an elevated command line in Windows 7
```
WIN8CMD
```
Load an elevated command line in Windows 8
```
STRING echo "I love ducks"
```
We pass text we want to type with the STRING command. STRING will by default press enter at the end of line.
```
TEXT echo "I love ducky"
```
TEXT is similar to STRING command but instead of pressing ENTER after text is type, we leave text where it is.  Useful if you want to type something then combine with other commands.

Other useful commands:

```
ALT
CONTROL
CTRL
DELETE
DEL
SHIFT
MENU
APP
ESCAPE
ESC
END
SPACE
TAB
PRINTSCREEN
ENTER
UP
DOWN
LEFT
RIGHT
F1-F10
CAPSLOCK
```

Keys can also be combined into: CTRL ALT DEL

### Mouse Commands
```
MOUSE LEFTCLICK
MOUSE RIGHTCLICK
```
Left click and right click.
```
MOUSE 100 0
```
Will move 100 pixels to right.
```
MOUSE 0 -50
```
Will move 50 pixels up.

TODO
==========
- [ ] Make it easier to run on Nethunter

# TERES-KBD-RELEASE

How to compile the keyboard and touchpad firmware for TERES-I:

1. Make sure that you are performing these steps on the TERES-I itself.

2. Create a directoty for the sources:
```bash
mkdir avrspace
```

3. Go to the directory and download our code inside:
```bash
cd avrspace

git clone https://github.com/d3v1c3nv11/TERES-KBD-RELEASE.git

cd TERES-KBD-RELEASE/
```
4. Download Dean Camera's LUFA USB stack from http://www.fourwalledcubicle.com/ 
   Extract the archive inside "avrspace/TERES-KBD-RELEASE/" to directory lufa-LUFA-170418
```bash
unzip lufa-LUFA-170418.zip
```
5. The Olimex keyboard + touchpad code is located in "avrspace/TERES-KBD-RELEASE/TERES-HID/", navigate there to edit the build depndencies:
```bash
cd TERES-HID/
```
6. Edit the makefile inside avrspace/TERES-KBD-RELEASE/TERES-HID/
```bash
nano makefile
```
search for LUFA_PATH and make sure it point to LUFA library:
```bash
LUFA_PATH    = ../lufa-LUFA-170418/LUFA
```
save file and exit nano

7. Compile
```bash
make
```
8. Update the firmware of the TERES-I's keyboard and touchpad firmware:
```bash
./update
```
You will be prompted to press "fn+Tux+ESC" (function + penguin + escape) keys simultanously at some point. Make sure to do so!

9. Voila! Updade successful.

Note 1: If you wish to play with the behavior yourself edit the sources in avrspace/TERES-KBD-RELEASE/TERES-HID/
Note 2: If you have problems with the touchpad and it seems dead, make sure that you haven't disabled it with fn+F3

The code is based on Dean Camera's LUFA USB stack. More info at:
http://www.fourwalledcubicle.com/
The LUFA library is currently released under the MIT license, included below.
Copyright (C) Dean Camera, 2016 dean [at] fourwalledcubicle [dot] com
www.lufa-lib.org
Permission to use, copy, modify, and distribute this software and its documentation for any purpose
is hereby granted without fee, provided that the above copyright notice appear in all copies and that
both that the copyright notice and this permission notice and warranty disclaimer appear in
supporting documentation, and that the name of the author not be used in advertising or publicity
pertaining to distribution of the software without specific, written prior permission.
The author disclaims all warranties with regard to this software, including all implied warranties of
merchantability and fitness. In no event shall the author be liable for any special, indirect or
consequential damages or any damages whatsoever resulting from loss of use, data or profits,
whether in an action of contract, negligence or other tortuous action, arising out of or in connection
with the use or performance of this software.
# TERES-KBD-RELEASE

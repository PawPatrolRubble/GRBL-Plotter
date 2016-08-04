# GRBL-Plotter
A GCode sender for GRBL under windows, using DotNET 4.5 (should also work with Windows XP)
Written in C# VisualStudio 2015 

###Soon:
Controlling a 2nd Arduino with GRBL for tool change or 4th (5th, 6th) axis control (GRBL-Plotter is waiting for 'IDLE' on one GRBL before controlling the other). Commands for 2nd GRBL will be introduced via special formatted remarks in GCode e.g.: (^2 G90 X2) to move 2nd GRBL to position X2.

### Program is free and you can use it at your own risk, as you understand there is no warranty of any kind
Just unzip in new folder and run the GRBL-Plotter.exe
[GRBL-Plotter](GRBL-Plotter.zip)

### Requirements for compiling
* VisualStudio 2015 
* DotNET 4.5

### Features:
* User defined Buttons - GCode from text-field or file
* Joystick like control
* Automatic reconnect on program start
* Recent File List (Files and URLs)
* 2-dimensional preview
* Import/creation and conversion into GCode 
  - from SVG Graphics
  - from Text (into Hershey Font)
  - conversion of the Z-Dimension into Z-axis (router) or Spindle on/off (laser) or Spindle-Speed (RC-Servo PWM) 
* GCode can be edited and saved
* Drag & Drop of GCode (*.nc) and SVG (*.svg) files
* Drag & Drop (or Copy & Paste) of Browserlinks to SVG-files (works only with Chrome) for example from https://openclipart.org/
* Transformation of GCodes (scale, rotation, mirror, zero-Offset)
* Optional usage of a WebCam with graphics overlay of the current GCode, set zero point, measure angle, zoom
* Internal variable to support probing, e.g.:
  - G38.3 Z-50		(probe toward tool length sensor, stop on contact - because of decelaration stop-pos. is not trigger-pos.)
  - G43.1 Z@PRBZ	(Offset Tool with value stored on trigger of sensor switch)
  - examine SerialForm.cs for implementation

### ToDo
* Import of pictures
* Wizzard to generate simple forms in GCode
* Setup of the Joystick parameters (speed depending on step-size)

### My test bed
On my german homepage:
[my XYZ platform](http://svenhb.bplaced.net/?CNC___Plotter)

### Screenshots
Main GUI
![GRBL-Plotter GUI](GRBLPlotter_GUI.png?raw=true "Main GUI")

Seperate serial COM window

![GRBL-Plotter COM interface](GRBLPlotter_COM.png?raw=true "Serial connection")

Setup import / GCode conversion
![GRBL-Plotter Setup1](GRBLPlotter_Setup1.png?raw=true "Setup1")

Setup user defined buttons
![GRBL-Plotter Setup2](GRBLPlotter_Setup2.png?raw=true "Setup2")

Setup colors

![GRBL-Plotter Setup3](GRBLPlotter_Setup3.png?raw=true "Setup3")

Text import

![GRBL-Plotter Text](GRBLPlotter_Text.png?raw=true "Text conversion")

Different scaling options

![GRBL-Plotter Scaling](GRBLPlotter_scaling.png?raw=true "GCode scaling")
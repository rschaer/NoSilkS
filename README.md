# NoSilkS
### KiCAD 8.0 default footprints with all graphical silk screen elements removed 

#### The Problem
Graphical silkscreen elements can throw DRC errors and interfere with exporting production files if they intersect with other elements or are outside the edgecut boundaries. Most of the time, the grapical silk screen elements (lines, circles) are completely unneeded. I.E. if the polarisation or pin 1 of a component needs to be marked, this can easily be done by modifying one of the pads to look different, for example using rounded square vs. regular square pads vs. circular pads.

#### My Solution
A Windows PowerShell script that reads every *.kicad_mod file and removes all blocks and lines of code that create a graphical line or circle (fp_line, fp_circle) for a silkscreen layer (layer "F.SilkS") and (layer "B.SilkS").


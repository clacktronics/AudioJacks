# Design Rules

I am not very strict with design rules because with connectors there are so many exceptions you may neeed to make.

The following are the general rules I follow to create some kind of uniformity.

## 3D Models

* Body colour if black #646464 because actual black does not look good rendered. 
* Colour if silver metal FreeCAD standard

## Footprints

* Folllow the manufacturer hole dimensions as close as possible
* Holes are slots if the pins are wide and flat
* At least two opposite pins have a 2mm annular ring for strong mechanical support
* minimum annular pad size is 1.5mm
* If the connector is board edge, the edge is defined in `Dwgs.User` with the text "Board edge"
* A board edge connector should have a drawing in `Dwgs.User` showing how it protrudes from the edge of the board, e.g the threaded bush of a jack
* F.CrtYrd is a box 1mm larger than the size of the body
* Silkscreen outline of the jack body with 0.2mm lines so the inside of the lines is the theoretical jack size e.g if jack body is 10x10mm the lines are at 10.2 x 10.2
* Use footprint naming conventions of KiCAD 
* Drawing origin should be at the centre of the jack connector, this allows easy placement for panel design
* If jack is horizontal x axis 0 should be at board edge
* Use KiCAD pad names for jack pins T, TN, R, RN, S, SN

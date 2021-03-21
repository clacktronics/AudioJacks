# WARNING NOT YET COMPLETE, DO NOT USE, PLEASE CHECK AGAIN OR FOLLOW FOR FINAL RELASE
https://github.com/clacktronics/AudioJacks

# AudioJacks
KiCAD footprint library and 3D models for commonly used connectors used in synths and other audio equipment.

# Directory structure
* AudioJacks.3dshapes  - The .step files used by KiCAD for the PCB rendering
* AudioJacks.pretty - the KiCAD footprint library
* Demo_board - Example board of all the jacks
* FreeCAD_Drawings - The modifiable FreeCAD used to generate the 3dmodels
* Assets - Images and other items used for this documentation


# Installation and use (KiCAD 5.1)

### Symbols
There are no symbols for the jacks as it is intended for use with the KiCAD standard symbols. The pads are named with the matching designators that KiCAD uses for jacks they are as below

* T = Tip the end of the jack
* R = The ring of the jack, when stereo this is the middle band
* S = The sleeve of the jack, usually referenced to ground and connected to the conductive sleeve of the cable
* TN = Tip Normalized, this is connected to tip when the jack is not present but disconnected on insertion
* RN = Ring Normalized, this is connected to ring when the jack is not present but disconnected on insertion
* SN = Sleeve Normalized, this is connected to sleeve when the jack is not present but disconnected on insertion

For information on which jack symbol to use with which connector read `DATA.md` that contains more detailed information about this library that is not possible to fit into the KiCAD files.


### Footprints via footprint editor
* Copy to chosen location for your custom KiCAD libraries, this could be the default one or anywhere on your disk.
* Open the footprint editor and choose `File > Add Library` pick the `AudioJacks.pretty` folder and click open
* Choose `Global` as the file table to add it to 

### Footprints via PCBnew
* Select `Preferences > Manage footprint libraries`
* Under `Global Libraries` tap, choose the folder icon `Add existing library to table`
* Find `AudioJacks.pretty` and press open

### Using the 3D models
This is a little tricky, the way KiCAD 5.1 manages 3D models is still a little bit basic. Fundamentally the 3D files just need to be dumped into the `packages3d` directory but they will not be shared as the files are not stored in the project folder unlike symbols and footprints which are backed up into the local project folder. The best way is to copy the 3d shapes part of this library into the official KiCAD directory. 

* Open up Kicad and go to `Preferences > Configure paths` find the directory of your `KISYS3DMOD` files
* Copy over `AudioJacks.3dshapes` to that directory (you might find it is Read only, use Admin)
* they should now work

If you wish to do it another way you have to manually edit each footprint either at PCBnew level or in the footprint editor to point to the new location of the 3d file for that footprint. It will likely end up being the absolute location on your computer.

# FAQ
* _Can you add xxx jack to the library?_ - Yes add a feature request to issues on Github
* _My footprint did not fit after I got PCB from the manufacturer!_ - I try to test the files the best I can, but I can not guaruntee it, it is up to you to take responsibility for the design as manufacturer quality varies. If you have a problem with a footprint please open an issue on Github and I will see what I can do.
* _Can I contribute my files to this library?_ - Yes, read `CONTRIBUTE.md` to check a few simple design rules I follow. I can not guaruntee my response speed.
* _Your descriptions are wrong for the parts!_ - Please let me know if you see any errors, the descriptions try and hint what audio/Eurorack kits they are used in to help finding the right ones, they may not be complete.
* _Why dont you contribute the files to KiCAD main library?_ Yes that is the plan, I will attempt to contribut the footprints and 3D models to the KiCAD main library (probably "Connectors audio") but this seperate repository lets you grab what you need now and lets me provide a bit more information.

# Licence

I have attached an MIT licence, it is free to use and modify for any use. I don't beleive in licences as they are only useful for the super wealthy who can afford gambling on litigation and in the end the only people that really win are the lawyers. Hopefully it will help if you need the proof that I won't come after you, all work here is original, no files are derivative of other copyrighted work such as manufacturer 3D models for example.

# Donate

If you have found this project useful or are using it in a commercial product please consider donating a one off via Ko-fi or sponsoring me monthly on Github. It will help me a lot and is appreciated!

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/M4M340M71)

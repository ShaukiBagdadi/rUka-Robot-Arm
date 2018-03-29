# rUka-Robot-Arm
Compared to other hobby robot arms this robot arm:
Has no axles, no bearings, no belts, no pulleys - per joint only needed one geared stepper, one printed arm and two bolts: M3 for the head and M5 for the tail.

With lesser components there is lesser play and flex in the joints, shorter BoM and shorter time to assemble.

The arms of rUka are printed with strands in the direction giving most strength.

The most simple RepRap controller can operate the rUka without expensive drivers for heavy steppers.

The higher resolution of rUka is provided by the planetary gears.
For example slewing one degree with 16 microstepping and gear ratio 50.89 requires (16.*50.89/1.8) 452.35 microsteps per degree. At an extend of 250 mm from the slewing axis the effector shall have a resolution of 0.01 mm (250*math.pi/452.35/180).

Divide (MAX_STEP_FREQUENCY 40000) by 452.35 and you get a rotation speed of 88.42 deg/sec.
The linear speed of the effector at an extend of 250 mm is 385.8 mm/sec (250*math.pi*88.42/180).

On those pictures you see the R3 first version that shall be used to develop the blender script for arm GCode generator. Later shall upgrade to R4 where the hot end rotates to maintain vertical orientation and this increases the effective build volume.

So average of 300 mm/sec and resolution of 0.01 mm are suitable values for normal FDM 3D printing.

The album that shall be updated: https://photos.app.goo.gl/Rk5VHIa0J8tnbySf1
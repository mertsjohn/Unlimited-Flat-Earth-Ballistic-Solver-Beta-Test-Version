# Unlimited-Flat-Earth-Ballistic-Solver-Beta-Test-Version
External Ballistic Solver for G7 BC type Projectiles
This windows 11 based executable will produce a GUI which will allow the user to explore external ballisitcs on a local computer.
The user will need a bullet diameter, a muzzle velocity, a G7 BC, and may specify a downrange printout containing ballistic information
such as scope adjustments needed to perform extreme long range shots. A vacuum validation run can be selected to display computational errors
relative to the closed form solution for the Vacuum trajectory. For atmospheric shots, air density and gravity are modeled epoch by epoch
according to in-flight drived altitude. The program is written in modern fortran and makes use of parallel processing. The source code is
just over 6000 fortran lines of code. It uses an 8th order Dormand Prince variable step integrator with range as the independent integration
variable.  The G7 drag function is embedded in the source code and contains 501 samples obtained using Pchip interpolation within Matlab over
the velocity range: 0 to mach 5. The program is one file and can run with or without an output file being produced. If the write-to-file option
is selected, the input initial conditions as well as the computed ballistic results will be written to the text file named output.dat.
Subsequent runs will read the saved initial inputs contained in the output.dat file which may be overwritten by subsequent runs. The data runs
are fast with a typical execution elapsed time of 4 ms for a 1000 yd trajectory with outputs written every 100 yards. This is an initial
release for Beta testing. Comments are appreciated and needed in order to round-out the current state of the code and continue development.
I will attempt to answer questions.  jhm 19Oct26

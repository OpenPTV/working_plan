Working plan of the OpenPTV consortium
============

Working plan of the OpenPTV consortium is the result of the kick-off meeting during the OpenPTV workshop in Tel Aviv, 
April 29 - May 3, 2013


## Whiteboard snapshot

![Snapshot](http://goo.gl/FyaeW)


## Explanation

For the background of the meeting and the ideas behind it, please see the introductory lecture prepared by the organizers
[Slideshow](http://goo.gl/h98kA)


### Original Zurich version

Original Zurich version is the historical name of the code developed at ETH Zurich from 1980's. This code is present in 
the OpenPTV repository under the name `C-Tcl/Tk`. One of the major decisions of the meeting is that this version
is obsolete and would be depreceated in the future. Please **DO NOT** develop your new algorithms in `C-Tcl/Tk` framework. 

### liboptv

`liboptv` is the abbreviation of OpenPTV library. The OpenPTV community will actively develop the library that will 
contain all the major algorithms for three dimensional particle tracking velocimetry, such as particle identification 
(or segmentation), calibration, correspondence (or stereo-matching), tracking and post-processing routines. 

The library will be developed by moving functionality from the `C-Tcl/Tk` source code base, written in ANSI-C into the 
library. The first examples exist in `OpenPTV/openptv` repository. This is our central, community approved code base.


### PyPTV or OpenPTV-Python

This is the new GUI frontend, written in Python 2.7 and using NumPy, SciPy, Matplotlib, Cython from the Scientific Python stack 
and Enthought Tools Suite (TraitsUI, Chaco, Enable) from Enthought Inc. for quick GUI development. This version is developed
by the Turbulence Structure Laboratory at Tel Aviv University. 

The OpenPTV kick-off meeting decided to choose this framework (with possible change of the GUI to PyQt for example) as 
the central direction course. This is mainly because PyPTV already uses the `liboptv` approach:

Python GUI -> Python -> Cython -> C 




## C-Tcl/Tk version

The question is whethere we  discard C-Tcl/Tk version or incorporate the new developments of TU/e and RTWH
in the existing code?

Alex: `@alexlib` on Github. I vote for option 1: stop developing C-Tcl/Tk and instead put all the effort on learning how to move
the new development into the `liboptv`. I also suggest to add to the to-do list here our decision on the committees:  
1. Code manager  
2. Documentation manager  
3. Website manager  
4. Public relations manager - new users, new collaborators, Facebook, LinkedIn, etc.  

the managers are not doing all the work themselves but ask for help from the group and coordinate it. 

We also have to decide about the voting procedure, i.e. predefine democracy. 

(note if you want to get new line break, leave TWO SPACES `  ` at the end of the line, `Enter` is not enough :))








## How to work with this file? 

Alex created this file and open it for the discussion. This file should be edited in the following way: 

1. create Github account
2. Fork this repository with the Readme.md file
3. Update the file in the way you want, commit it and push to your repository (only to your, not to OpenPTV)
4. Send us your pull request and we'll accept it if your file can be merged with the other editions and whether it does not contain mistakes and typos.

We recommend to try first http://try.github.io and also see the lectures on the site Software Carpentry, e.g. http://software-carpentry.org/4_0/vc/index.html and http://software-carpentry.org/blog/2012/06/git-tutorial-links.html


Marc
Beat was here

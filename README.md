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

`liboptv` is the abbreviation of OpenPTV library. The OpenPTV community had decided to actively **develop the library** that will 
contain all the major algorithms for three dimensional particle tracking velocimetry, such as particle identification 
(or segmentation), calibration, correspondence (or stereo-matching), tracking and post-processing routines. 

The library will be developed by moving functionality from the `C-Tcl/Tk` source code base, written in ANSI-C into the 
library. The first examples exist in `OpenPTV/openptv` repository. This is our central, community approved code base.


### PyPTV or OpenPTV-Python

This is the new GUI frontend, written in Python 2.7 and using NumPy, SciPy, Matplotlib, Cython from the Scientific Python stack 
and Enthought Tools Suite (TraitsUI, Chaco, Enable) from Enthought Inc. for quick GUI development. This version is developed
by the Turbulence Structure Laboratory at Tel Aviv University. 

The OpenPTV kick-off meeting decided to **choose openptv-python framework** as a central framework (with possible change of the GUI to PyQt for example) as 
the central direction course. 

This is mainly because PyPTV already uses the `liboptv` approach: `Python GUI -> Python -> Cython -> liboptv` and it is 
easily extendable thanks to Python.


### The workplan as it appears on the whiteboard

1. move all the code from `C-Tcl/Tk` to `liboptv`
2. add all the new developments by different groups to `liboptv`
3. stop using `C-Tcl/Tk`
4. write documentation, tentatively Doxygen was chosen as a unified framework for C and Python code
5. validate your code, learn Unit testing, write tests, create validation cases using DNS or another true cases
6. make it clear how to cite this work, create a list of references
7. create simple installations for the users, create simple instructions for the developers
8. look into some option to run the code online, from the browser
9. change all the parameter files from undocumented ASCII format to INF (or XML) format. 
10. data files remain in ASCII until we have a better idea and `liboptv` will be ready with a single function that deals with I/O
11. License has not been chosen, we need to choose and the two suggestions of LGPL vs MIT/BSD-like shall be decided after some learning process
12. Use Software Carpentry or other tutorial sites to learn about Git, Github and unit testing
13. think of investing your time, time of your students, collect donations, apply for proposals, propose GSOC




----------

## How to work with this file? 

Alex created this file and open it for the discussion. This file should be edited in the following way: 

1. create Github account
2. Fork this repository with the Readme.md file
3. Update the file in the way you want, commit it and push to your repository (only to your, not to OpenPTV)
4. Send us your pull request and we'll accept it if your file can be merged with the other editions and whether it does not contain mistakes and typos.

We recommend to try first http://try.github.io and also see the lectures on the site Software Carpentry, e.g. http://software-carpentry.org/4_0/vc/index.html and http://software-carpentry.org/blog/2012/06/git-tutorial-links.html


Marc
Beat was here

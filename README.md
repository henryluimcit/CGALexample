# CGALexample

This project is an example of CGAL with XCode.

## XCode Setup for CGAL

Assuming you have install CGAL and its dependencies, in order to get CGAL to work with XCode, you will have to configure the Build Settings:

1.  Search Paths > Header Search Paths: add /usr/local/include
2.  Search Paths > Library Search Paths: add /user/local/lib

Under Build Phases, you will need to add additional libraries:

Use the '+' button under 'Link Binary With Libraries' and then select 'Add Other... > Add Files...'.  Type command+shift+g to go to the folder '/usr/local/lib' to add the following libraries:

1.  libboost_system.dylib or libboost_system-mt.dylib
2.  libboost_thread.dylib or libboost_thread-mt.dylib
3.  libCGAL_Core.dylib
4.  libCGAL.dylib
5.  libgmp.dylib
6.  libmpfr.dylib

Note: if you cannot find libCGAL.dylib, you can add the CGAL folder under '/usr/local/Cellar/cgal/5.0.2/include' (assuming CGAL version 5.0.2) and the version folder under '/usr/local/Cellar/cgal'.

To work with files, you'll need to:

Go to Product > Scheme > Edit Scheme... and under Run, within Options, select 'Use custom working directory' and navigate to the project directory.  For me, this was '/Users/.../CGALnaive/CGALnaive'

## Current Issues

1.  There are several build errors after running.
2.  This project does not utilize qt5, which may require additional dependencies.

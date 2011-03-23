## Get BamTools
The easiest way to get BamTools is to clone the git repository straight from GitHub:

$ git clone git@github.com:pezmaster31/bamtools.git

Developers who would like to modify (and we hope, contribute to) BamTools directly, may fork the project using the 'Fork' button at the top of the BamTools homepage, then pull down their own version of BamTools.

## Get CMake
BamTools has been migrated to a CMake-based build system.  We believe that this 
should simplify the build process across all platforms, especially as the 
BamTools API moves into a shared library (that you link to instead of compiling 
lots of source files directly into your application). CMake is available on all 
major platforms, and indeed comes *out-of-the-box* with many Linux distributions.

To see if you have CMake (and if so, which version) try this command:

$ cmake --version

BamTools requires CMake (version >= 2.6.4). If you are missing CMake or have an 
older version, check your OS package manager (for Linux users) or download it here:
http://www.cmake.org/cmake/resources/software.html .

## Build BamTools
Ok, now that you have CMake ready to go, let's build BamTools.  A good
practice in building applications is to do an out-of-source build, meaning
that we're going to set up an isolated place to hold all the intermediate 
installation steps.

In the top-level directory of BamTools, type the following commands:

  $ mkdir build

  $ cd build

  $ cmake ..

Microsoft Visual Studio users:
This step creates a VS solution file (.sln), which can then be built to create 
the toolkit executable and API DLL's.

Everybody else:
After running cmake, just run:

  $ make

Then go back up to the BamTools root directory.

  $ cd ..

Assuming the build process finished correctly, you should be able to find the 
toolkit executable here:

  ./bin/

The BamTools API and Utils libraries will be found here:

  ./lib/

The BamTools API headers will be found here:
 
  ./include/*
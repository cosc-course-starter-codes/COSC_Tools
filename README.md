# COSC Tools
For now, this repo just contains a (hopefully) working version of the MinGW compiler for Windozzze. You can find the most up to date version at https://www.msys2.org/ but this is here for your convenience. Either grab the above version (https://github.com/cosc-course-starter-codes/COSC_Tools/raw/refs/heads/main/msys2-x86_64-current.exe) or the latest one from https://www.msys2.org/.
Once downloaded you can follow these instructions to get everything installed:
### <u>Windows Installation Specifics</u>
#### Install MinGW ( https://github.com/cosc-course-starter-codes/COSC_Tools/ )

You can find a longer, illustrated version of these instructions at: ( https://code.visualstudio.com/docs/cpp/config-mingw#_installing-the-mingww64-toolchain )
1.  Download and run the latest (current) version of the installer (`msys2-x86_64-current.exe`) with the default options (in the default location--`C:\msys64\`).
2.	The installer will do a few things and then ask to run MSYS2 when it is done. Make sure it is selected and run MSYS2. (You can also now find “MSYS2 MSYS” in the start menu).
3.	This brings you to a command prompt. From here just type (or copy/paste!) the line below. This runs the package manager (not what you were thinking?) to download the current MinGW version. Then hit enter a few times to install the mingw packages.
    ```
    pacman -S --needed base-devel mingw-w64-x86_64-gcc
    ```
4.	When it is done, you will be brought back to the command prompt. Exit this by typing `exit` or just closing the window.

#### Set your Path
1. Click the Windozzze start button and type `advanced system settings` to bring up the system properties window.
1. Click on `Environment Variables` button.
1. In the `System variables` box at the bottom, select `Path` and press the `Edit` button (at the bottom!).
1. Click the `New` button and type
   ```
   C:\msys64\mingw64\bin
   ```
1. Close all windows and make sure to reboot when done.

#### Optional: Install OpenGL and GLUT ( http://www.transmissionzero.co.uk/software/freeglut-devel/ )
1. Grab the latest version of FreeGLUT for MinGW from the link above and extract the files to your computer. Make sure to get the version for MinGW!
1. Go to the subdirectories of that archive and find three folders: `bin`, `include`, and `lib`. Each of these contains files that need to be copied to the correct location for your program to compile and run. Just use the 64-bit versions (ignore any files not in the x64 subfolders).
1. Copy the x64 file `freeglut.dll` from bin to the `mingw64\bin` directory (by default, this should be something like `C:\msys64\mingw64\bin`).
1. Copy the four files in the folder `GL` under include to the `mingw64/include/GL` directory (by default, this should be `C:\msys64\mingw64\include\GL`).
1. Copy the two x64 `a` (`libfreeglut.a` and `libfreeglut_static.a`) files from lib to the `mingw64/lib` directory (by default, this should be `C:\msys64\mingw64\lib`).

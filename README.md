# Installation of OpenCV 3.4.0 on Windows with Visual Studio 2015 or 2017

Step 1: Get the chocolatey package manager. Find the instructions at https://chocolatey.org/

Step 2: Install openCV with "choco install -y opencv". At the time of writing, chocolatey has version `3.4.0`

Alternatively, install OpenCV from `https://sourceforge.net/projects/opencvlibrary/files/opencv-win/3.4.0/opencv-3.4.0-vc14_vc15.exe/download`

Step 3: Install Visual Studio  2015 or 2017. Ensure you have "Desktop Development with C++" support enabled.

Step 4: Open a command prompt as an administrator and run the following command to set your environment variables. 

This is assuming OpenCV is installed to `C:\tools`. If you installed OpenCV to a different directory, replace `C:\tools` in the commands below.

		VS 2015: setx -m OPENCV_DIR C:\tools\opencv\build\x64\vc14
		VS 2017: setx -m OPENCV_DIR C:\tools\opencv\build\x64\vc15

With the previous command window, set your PATH with the following command:

		setx -m PATH "%PATH%;%OPENCV_DIR%\bin"

Step 5: Probably a good idea to restart your computer at this point

## Project Creation


### Easy Method
If you have Visual Studio 2017, the project file in this repository is set up already. Make a copy of it. You can build for "Debug" or "Release". 64-bit mode is the only one supported




## Sources
https://docs.opencv.org/2.4/doc/tutorials/introduction/windows_install/windows_install.html
https://docs.opencv.org/2.4/doc/tutorials/introduction/windows_visual_studio_Opencv/windows_visual_studio_Opencv.html#windows-visual-studio-how-to
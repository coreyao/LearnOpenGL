# learnopengl.com code repository
Contains code samples for all tutorials of [http://learnopengl.com](http://learnopengl.com). 

The CMakeLists.txt is not yet tested/finished for OS X; for more info see http://learnopengl.com/#!Code-repository

## Windows building
All relevant libraries are found in /libs and all DLLs found in /dlls (pre-)compiled for Windows. 
The CMake script knows where to find the libraries so just run CMake script and generate project of choice.
Note that you still have to manually copy the required .DLL files from the /dlls folder to your binary folder for the binaries to run.

## Linux building
First make sure you have CMake, Git, and GCC by typing as root (sudo) `apt-get install g++ cmake git` and then get the required packages:
Using root (sudo) and type `apt-get install libsoil-dev libglm-dev libassimp-dev libglew-dev libglfw3-dev` . Next, run CMake (preferably CMake-gui). The source directory is LearnOpenGL and specify the build directory as LearnOpenGL/build. Creating the build directory within LearnOpenGL is important for linking to the resource files (it also will be ignored by Git). Hit configure and specify your compiler files (Unix Makefiles are recommended), resolve any missing directories or libraries, and then hit generate. Navigate to the build directory (`cd LearnOpenGL/build`) and type `make` in the terminal. This should generate the executables in the respective chapter folders. Note that using CodeBlocks or an IDE may have issues running the programs due to problems finding the shader and resource files, however it should still be able to generate the exectuables.

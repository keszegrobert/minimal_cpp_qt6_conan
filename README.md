# Minimal qt6 example with conan

If you are thinking that making a C++ project with qt6 is hard, I have a bad news for you: You are wrong

## Prerequisities

1. installed python
2. installed conan
3. installed cmake
4. installed ninja or make or Visual Studio
5. Follow the steps here: https://old-account.qt.io/conan 

## Working with this repository

Here are the 7 steps you must follow:

1. clone this repository and cd into it
2. make a build directory which will hold the temporary build files
3. using the conanfile.txt build the requirements and put them into conan's cache. 
The path provided to the conan command should contain a conanfile.txt or conanfile.py
4. activate the virtual environment created by the previous step. The paths will be set to contain everything needed for the development
5. generate the build files using the contents of the CMakeLists.txt file. The path provided to the cmake command should contain the CMakeLists.txt file
6. Build the generated solution
7. Run the console application

## The same steps in the terminal

```git clone https://github.com/keszegrobert/minimal_cpp_qt6_conan.git```

```cd minimal_cpp_qt6_conan```

```mkdir build```

```cd build```

```conan install ../ -r qt --generator=virtualenv --build=missing```

On *nix systems use: ```source activate.sh```

On Windows* systems use: ```activate.bat```

```cmake ..```

```cmake --build .```

```./helloworld```

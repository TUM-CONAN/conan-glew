
[Conan.io](https://conan.io) package for [glew](https://github.com/nigels-com/glew) project

## For Users: Use this package

### Basic setup

    $ conan install glew/2.1.0@camposs/stable

### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    glew/2.1.0@camposs/stable

    [generators]
    cmake

Complete the installation of requirements for your project running:

    $ mkdir build && cd build && conan install ..

Note: It is recommended that you run conan install from a build directory and not the root of the project directory.  This is because conan generates *conanbuildinfo* files specific to a single build configuration which by default comes from an autodetected default profile located in ~/.conan/profiles/default .  If you pass different build configuration options to conan install, it will generate different *conanbuildinfo* files.  Thus, they should not be added to the root of the project, nor committed to git.

## For Packagers: Publish this Package

The example below shows the commands used to publish to bincrafters conan repository. To publish to your own conan respository (for example, after forking this git repository), you will need to change the commands below accordingly.

## Build and package

The following command both runs all the steps of the conan file, and publishes the package to the local system cache.  This includes downloading dependencies from "build_requires" and "requires" , and then running the build() method.

    $ conan create camposs/stable

## Add Remote

    $ conan remote add camp "https://conan.campar.in.tum.de"

## Upload

    $ conan upload glew/2.1.0@camposs/stable --all -r camp

## License
[License](https://github.com/nigels-com/glew/blob/master/LICENSE.txt)

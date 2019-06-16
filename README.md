## Tensorflow 2.0alpha for Godot

<Wikipedia\> TensorFlow is a free and open-source software library for dataflow and differentiable programming across a range of tasks. It is a symbolic math library, and is also used for machine learning applications such as neural networks. 

This is Tensorflow for Godot Engine. The demo classifies an image into labels. This is a base for more interesting ideas like image upscaling, ai bots, chat bots, animations and others.

![Screen](https://github.com/godot-extended-libraries/godot-tensorflow-workspace/blob/master/Screen%20Shot%202019-05-13%20at%209.21.18%20PM.png)

## See also

https://github.com/godot-extended-libraries/godot-tensorflow

https://github.com/godot-extended-libraries/godot-tensorflow-demo

https://github.com/godot-extended-libraries/tensorflow

## Setup Instructions

* Get depot tools.
* Fetch the client
* Compile godot
* Open the example project
* Run the game
* See classification of the image

## Windows

*MUST HAVE PYTHON2*

Download the depot_tools bundle and extract it somewhere.

https://storage.googleapis.com/chrome-infra/depot_tools.zip

Add depot_tools to the start of your PATH (must be ahead of any installs of Python). Assuming you unzipped the bundle to C:\workspace\depot_tools:

With Administrator access:
Control Panel → System and Security → System → Advanced system settings

Modify the PATH system variable to include C:\workspace\depot_tools.

Without Administrator access:
Control Panel → User Accounts → User Accounts → Change my environment variables

Add a PATH user variable: C:\workspace\depot_tools;%PATH%.

Go to godot-tensorflow-workspace and run `gclient sync`.

Go to `src/thirdparty/godot` and compile using `scons p=windows tools=yes -j8`.

Use https://docs.godotengine.org/en/3.1/development/compiling/compiling_for_windows.html as reference.

Execute the binary in `src/thirdparty/godot/bin` and open the project.

## Linux

```
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
git clone https://github.com/godot-extended-libraries/godot-tensorflow-workspace
cd godot-tensorflow-workspace
PATH=$PATH:../depot_tools gclient sync
```

## OSX


```
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
cd godot-tensorflow-workspace
PATH=$PATH:../depot_tools gclient sync
```

## Build System

For the build system:

```
sudo apt install git-lfs python
git clone https://chromium.googlesource.com/chromium/tools/depot_tools.git
cd godot-tensorflow-workspace
PATH=$PATH:../depot_tools gclient sync
``` 

Reference:

https://commondatastorage.googleapis.com/chrome-infra-docs/flat/depot_tools/docs/html/depot_tools_tutorial.html#_setting_up

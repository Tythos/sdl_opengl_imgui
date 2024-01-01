# sdl_opengl_imgui

Finished sandbox of SDL+OpenGL+ImGui build with cmake/submodules in C++ 

## Quick Start

After initial clone, get the submodules:

```sh
$ git submodule update --init --recursive
```

Then, do the usual two-step CMake build:

```sh
$ cmake -S . -B build
$ cmake --build build
```

Finally, before running, copy any dynamic libaries from the SDL build into the run folder:

```sh
$ copy build/sdl/Debug/*.dll build/Debug/
```

Now you're ready to run the executable:

```sh
$ build/Debug/sdl_opengl_imgui.exe
```

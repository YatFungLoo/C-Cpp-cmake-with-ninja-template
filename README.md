# C-Cpp-cmake-with-ninja-template
Simple C/C++ cmake with ninja project template to reuse for new project

```
mkdir build && cd build
```

```
cmake .. --preset=debug
```

or 

```
cmake .. --preset=release
```

```
ninja clean && ninja
```

and executable will exist in the `build/` directory.

to generate compile_commands.json file for clangd LSP, use

```
cmake -DCMAKE_EXPORT_COMPILE_COMMANDS=1 .. --preset=${PRESET_NAME}

cd ${ROOT_DIRECTORY}

ln -s build/compile_commands.json
```

## Dynamic Menu
Dynamic menu used in almost all my projects.

The project template is from [Cpp Project](https://github.com/bsamseth/cpp-project) and the idea for this menu is from @DarKreter.

## Project structure
Menu
```
 Dynamic-Menu
 ┣ app
 ┃ ┣ advancedExample.cpp
 ┃ ┗ beginerExample.cpp
 ┣ build
 ┣ cmake
 ┃ ┣ CodeCoverage.cmake
 ┃ ┣ Colors.cmake
 ┃ ┣ ConfigSafeGuards.cmake
 ┃ ┣ Doctest.cmake
 ┃ ┣ Documentation.cmake
 ┃ ┣ LTO.cmake
 ┃ ┣ Misc.cmake
 ┃ ┗ Warnings.cmake
 ┣ inc
 ┃ ┣ Menu.hpp
 ┃ ┣ config.hpp
 ┃ ┗ config.hpp.in
 ┣ lib
 ┃ ┣ doctest
 ┣ src
 ┃ ┗ Menu.cpp
 ┣ tests
 ┃ ┣ CMakeLists.txt
 ┃ ┣ main.cpp
 ┃ ┗ menu.ut.cpp
 ┣ .gitmodules
 ┣ .travis.yml
 ┣ CMakeLists.txt
 ┗ Doxyfile.in
```

## Build

```bash
git clone https://github.com/delipl/Dynamic-Menu/ # Cloning repository
cd Dynamic-Menu

git submodule init lib/doctest
git submodule update

mkdir build && cd build
cmake ..           # options: -DCMAKE_BUILD_TYPE=[Debug | Coverage | Release], Debug is default
make fulltest      # Makes and runs the tests.
make coverage      # Generate a coverage report.
make doc           # Generate html documentation.

make app           # Runs main loop
```

## Examples
Examples are in app

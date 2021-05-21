## Dynamic Menu
Dynamic menu used in almost all my projects.

The project template is from [Cpp Project](https://github.com/bsamseth/cpp-project) and the idea for this menu is from @DarKreter.

## Project structure
.
|
+-- app
|   +-- beginerExample.cpp    # Example of using
|   +-- advancedExample.cpp   
+-- build         # Built binaries
+-- cmake         # Cmake applications config like doctest, doxygen
+-- inc           # Header files
|   +-- Menu.hpp
+-- lib           # Libraries for project
|   +-- doctest
+-- src           # Source files
|   +-- Menu.cpp
+-- tests         # Doctests


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

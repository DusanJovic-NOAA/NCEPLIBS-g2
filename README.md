### NCEPLIBS G2 Library

Utilities for coding/decoding GRIB2 messages. This library
contains Fortran 90 decoder/encoder routines for GRIB edition 2,
as well as indexing/searching utility routines. 
For more detailed documentation see (grib2.doc).

Code Manager : Boi Vuong

#### Prerequisites

Compilers: GNU | Intel | Clang | AppleClang 

#### Installing
```
Download G2 Code from GitHub.com
git clone -b g2_v3.2.0 --recursive https://github.com/NOAA-EMC/NCEPLIBS-g2.git
cd NCEPLIBS-g2
```
#### Create a directory where to build G2 library
```
mkdir build
cd build
```
#### Load the following modules 
```
module load intel/18.0.5.274
module load impi/2018.0.4
module load cmake/3.16.3
module load jasper/1.900.1
module load libpng/1.2.44
module load zlib/1.2.11

export CC=icc
export CXX=icpc
export FC=ifort

If the chosen compiler is not the default compiler on the system,
set the environment variables: export CC=..., export CXX=..., 
export FC=..., before invoking cmake.

Note: Windows systems is not supported at this time.

```
#### Run cmake
```
cmake .. -DCMAKE_INSTALL_PREFIX=path_to_install -DCMAKE_PREFIX_PATH="${JASPER_LIBDIR}/.."

If -DCMAKE_INSTALL_PREFIX= is omitted, the libraries will be installed in directory 
install underneath the build directory.

make
make install

```
#### Version
3.2.0

#### Authors
* **[NCEP/EMC](mailto:NCEP.List.EMC.nceplibs.Developers@noaa.gov)**

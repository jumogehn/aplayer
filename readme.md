
How to use cmake environment
----------------------------

This project uses cmake so wide range of OSes are supported. For ubuntu, you can
compile as shown below

**Compile**
::
 mkdir build
 cd build/
 cmake ../src/
 (cmake ../src/ -DCMAKE_INSTALL_PREFIX=/usr/local)
 make

**Install**
::
 (sudo) make install

**Use**
::
 ./driver/aplayer
 (aplayer)

**Creating binary distributing**
::
 cpack -C CPackConfig.cmake

**Creating source distributing**
::
 cpack -C CPackSourceConfig.cmake


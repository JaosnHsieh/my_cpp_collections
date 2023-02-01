## cmake_opencv_test

Use 3rd library `opencv` via cmake.


## Setup on MacOS

1. install `opencv`

```bash
git clone https://github.com/opencv/opencv.git


mkdir build && cd build

cmake ../opencv/ .


## remove arch -arm64 for x64 MacOS on the following commands

arch -arm64 cmake ../opencv/ -DWITH_QT=OFF -DWITH_OPENGL=OFF -DFORCE_VTK=OFF -DWITH_TBB=OFF -DWITH_GDAL=OFF -DWITH_XINE=OFF -DBUILD_EXAMPLES=OFF -DBUILD_ZLIB=OFF -DBUILD_TESTS=OFF .

arch -arm64 sudo make -j 4

arch -arm64 sudo make install
```


2. build by cmake

```bash
mkdir build && cd build

cmake ..

make -j4
```

3. run

`cd build && ./opencv_test`

it would display `1.png` in the root directory


## References


https://gist.github.com/nucliweb/b2a234c673221af5ec24508da7d8b854

https://blog.csdn.net/zhanghm1995/article/details/105466372


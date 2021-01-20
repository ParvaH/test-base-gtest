Ref Project : https://github.com/dr-kino/BraveCoverage

Code coverage startup for C++ project using GCov and LCov

# Build Application

mkdir build && cd build

cmake ..

make

# Build Test/Coverage 

cd test && mkdir build && cd build

cmake ..

make init

make gcov

make lcov

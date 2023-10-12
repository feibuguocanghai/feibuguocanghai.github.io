---
title: fftw编译
date: 2023-10-11 17:11:33
tags:
---
fftw 3.3.10版本，目前支持cmake编译

windows编译过程如下
mkdir build 
cd build
cmake -DBUILD_SHARED_LIBS=OFF -DBUILD_TESTS=OFF -DENABLE_FLOAT=ON -DENABLE_SSE=ON -DENABLE_SSE2=ON -DENABLE_AVX=ON -DENABLE_AVX=ON -A x64  ..
1）去掉-A X64，就会编译x86架构
2) 会生成visual studio工程，然后用IDE编译或者通过命令行触发编译即可
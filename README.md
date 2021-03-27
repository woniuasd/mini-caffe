Mini-Caffe
==========


### What can Mini-Caffe do?

Mini-Caffe only depends on OpenBLAS and protobuf which means you can't train model with Mini-Caffe. It also only supports **Forward** function which means you can't apply models like neural art style transform that uses **Backward** function.



### Linux系统下编译
protobuf源码编译安装(3.15.5)  

```
$ sudo apt install libopenblas-dev 
$ ./generatepb.sh
$ mkdir build
$ cd build
$ cmake .. -DCMAKE_BUILD_TYPE=Release
$ make -j4
```

### With CUDA and CUDNN support

Install [CUDA](https://developer.nvidia.com/cuda-downloads) and [cuDNN](https://developer.nvidia.com/cudnn) in your system, then we can compile Mini-Caffe with GPU support. Run CMake command below.

```
$ cmake .. -DUSE_CUDA=ON -DUSE_CUDNN=ON
```

Currently we only test mini-caffe on CUDA8.0 with cuDNN5.1 and CUDA9.0 with cuDNN7.1.


### With Python support

checkout Python API [here](python), install package via `python setup.py install`.

# GreenOnion

GreenOnion is a tool used to hash a large number of PGP keys concurrently in order to find fingerprint matches in a large input list. This tool was used in my [MSc Dissertation](https://github.com/AidanFray/MSc_Dissertation) as a way to find near collisions.

## Installation

Dependencies
```
libssl-dev
opencl-headers
ocl-icd-libopencl1
ocl-icd-opencl-dev
```

Run
```
sudo apt install ocl-icd-opencl-dev ocl-icd-libopencl1 opencl-headers libssl-dev
make
```

## Usage

```
./GreenOnion <TARGET_KEYS_FILE_PATH> <OPENCL_DEVICE_NUMBER>
```


#### `<TARGET_KEYS_FILE_PATH>` 
The file path of your list of keys to search for. 

An example of how the key file should be formatted is below:

```
d17572da18666614
9957049a1e67f67f
d8c8a821370da0c5
3cd093ca5a9f4cc0
d3d579b54ff63214
993160138726250f
414d7f19223a9527
fa3b9cd607854225
8d82267fda303a6d
2c652ac574c3b76d
8fa6d9a8df0f555a
```

#### `<OPENCL_DEVICE_NUMBER>`
This should normally be `0`. This allows you to choose the device to use on a system with multiple GPUs. In order to run on multiple GPUs, multiple instances with different device numbers should be used.

## OpenCL/CUDA Install

###  Nvidia
https://askubuntu.com/questions/541114/how-to-make-opencl-work-on-14-10-nvidia-331-89-drivers

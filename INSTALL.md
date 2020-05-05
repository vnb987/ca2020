# 430.636 Computer Architecture (Spring 2020)

## Setup gpgpu-sim

### Overview

In this project, we will use docker to setup gpgpu-sim environment. 

1. Pull docker images.
2. Build FFT.
3. set environmental variables.

### Docker images 

The following instructions are based on the Ubuntu 18.04 LTS. 

```
$ apt-get install docker.io
$ docker pull michael604/scal2020_gpgpu_sim
$ docker run -it michael604/scal2020_gpgpu_sim /bin/bash
```

### How to Build FFT

In fft_reference directory,

```
mkdir build&&cd build
cmake .. -DCMAKE_BUILD_TYPE=Release
export LD_LIBRARY_PATH=/usr/local/cuda/lib64
make -j
```

### How to Run

You first need to set environmental variables correctly.

1. In *gpgpu-sim_distribution* directory,

```
source setup_environment debug
```

2. You need to locate *config_ARCH_islip.cnt* & *gpgpusim.config* files from *gpgpu-sim_distribute/configs/tested-cfgs*, to the directory that you are going to run the application.

```
mkdir run&&cd run
cp {gpgpu-sim_distrubute directory}/configs/tested-cfgs/{SM_NUM}/* ./
```

3. You can then start the application binary just as you do normally.

```
../fft_release
```


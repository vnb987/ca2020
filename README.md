# 430.636 Computer Architecture (Spring 2020)

## Project : Accelerating FFT in gpgpu-sim

###  Due : 11:59PM(someday), June xth

### Introduction

We will give you the simple FFT algorithm to run on gpgpu-sim simulator. The goal of this project is to understand the simulator behavior and GPU programming (especially gpgpu-sim) by accelerating the FFT algorithm. 

### Problem specification

Modify the given FFT source code to accelerate the FFT. The second step is not mandatory. you can get credits with the first. Second step is for students interested in programming the simulator.

1. Improve the FFT algorithm through software based approach. The baseline FFT algorithm is Cooley-Tukey FFT. you can change the algorithm itself, or optimize the algorithm in given simulator settings. 

2. Change the hardware architecture in gpgpu-sim to accelerate FFT algorithm.

#### 1. Improve the FFT algorithm

##### Reference code

'ExecFft()' function in src/ffthelper.cu, where the radix-2 colley tukey algorithm is implemented as a reference code. You are asked to change the function to optimize for the GPU architecture, using the gpgpu-sim simulator.

```cuda
//상표가 짠 cooley tukey code
```

>  cooley tukey 코드 설명

##### To do

- Make your **FFT** / **iFFT** code that performs better (leading to short execution time).
  You can modify every part of the code and add any other custom function. But it is necessary to explain the implementation.
- When you run the application binary with gpgpu-sim, execution time of the code will be displayed. The execution time of your optimized code and application will be evaluated using the time displayed at the end.
- If it's necessary, you are allowed to modify the CMakeLists.txt. However, do not modify any important flags, such as optimization level flags.

#### 2. Modify the hardware architecture in gpgpu-sim

##### To do

- 

### Restriction

By default, you will work on [gpgpu-sim](https://github.com/gpgpu-sim/gpgpu-sim_distribution) 4.0 version.  You can change the version of the simulator or even work on real GPU. please elaborate on what hardware setting the program executes. 

> 만약에 실제 GPU를 쓰거나 simulator 버전 등을 바꾼다거나 fork를 쓴다거나 하면 비교하는 방법을 정해서 설명해야 될 것 같습니다. Restriction 수업 때 들은 대로 적어보았는데 프로젝트 평가에 통일성이 필요하다고 생각하시면 조금 바꾸셔도 될 것 같습니다.

### Simulator resources

The source code of `gpgpu-sim` can be downloaded from [https://github.com/gpgpu-sim/gpgpu-sim_distribution](https://github.com/gpgpu-sim/gpgpu-sim_distribution) using the following command. Note that you should checkout your branch to `dev` after cloning this repository. Do not work on `master` branch.

```shell
git clone https://github.com/gpgpu-sim/gpgpu-sim_distribution
git checkout dev
```

For design and implementation of `gpgpu-sum`, please refer to the these links.

* [webpage](http://gpgpu-sim.org/)

* [manual](http://gpgpu-sim.org/manual/index.php/Main_Page)

### Setup gpgpu-sim

To Setup gpgpu-sim, please refer to the [SETUP.md][SETUP.md] file.

> 학생들이 각각 install하게 할꺼면 gpgpu-sim 리포만 알려주는 방법이 있고, gpgpu-sim에 dependency가 많기 때문에 통일하기 위해서라면 docker파일을 주는 것이 좋을 것 같습니다. 재민이가 docker 파일을 가지고 있고 dockerhub에서 저랑 공유도 해본 상태입니다. install하는 것을 학생들이 각각 하게 할꺼면 dependency를 통일하기 위해 vm 등을 실행시켜서 똑같이 download할 수 있게 문서가 하나 더 필요할 것 같습니다.(문서 길이를 고려했을 때)

### Hand in instruction

* Please remove all the debugging outputs before you submit.

* To submit your code, 

  >  github classroom 설명, 조교 화이팅!

* Make a simple report in Markdown explaining your work. Compare between the execution time of reference algorithm and yours.

### Logistics

* You will work on this project alone
* Only the upload submitted before the deadline will receive the full credit. 25% of the credit will be deducted for every single day delay.
* Any attempt to copy others' work will result in heavy penalty (for both the copier and the originator). Don't take a risk.

### Contact

If you find some errors or issues in the code, fill free to e-mail us. Our e-mails are posted in our class discription page.

Michael Jaemin Kim: [michael604@scale.snu.ac.kr](mailto:michael604@scale.snu.ac.kr)
Sangpyo Kim: [spkim@scale.snu.ac.kr](mailto:spkim@scale.snu.ac.kr)
[Class Page Link](https://scale-snu.github.io/jekyll/update/2020/03/16/aca2020-lecture-01.html)

Have fun !

EOF



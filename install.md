
# Installation


## JH Env 
Ubuntu : Ubuntu 23.10 <br>
GPU : AD104M [GeForce RTX 4080 Max-Q / Mobile] <br>
Cuda Version :  12.1 <br>
gcc / g++ Version: 11.4.0 / 11.4.0 <br>


## Dependencies
Nvidia-driver, Cuda 설치 되어 있어야 함 <br>

### System dependencies

```
$ sudo apt-get update 
$ sudo apt-get install -yqq  build-essential ninja-build \
  python3-dev python3-pip apt-utils curl git cmake unzip autoconf autogen \
  libtool mlocate zlib1g-dev python3-numpy python3-wheel wget \
  software-properties-common openjdk-8-jdk libpng-dev  \
  libxft-dev ffmpeg python3-pyqt5.qtopengl
$ sudo updatedb
```
- install plocate instead of mlocate

<br>

### Python dependencies

1. Create a new conda environment

    ```
    conda create -n lidar-bonnetal python=3.7
    conda activate lidar-bonnetal
    ```

<br>

2. Install python dependencies <br>
lidar-bonnetal root 폴더의 requirements.txt 설치


    ```
    pip install -r requirements.txt
    ```
    - 위의 방법으로 설치가 어려운 경우 아래와 같이 진행


    ```
    pip install numpy matplotlib scipy vispy Pillow PyYAML
    pip install opencv_python opencv_contrib_python
    pip install torch torchvision
    pip install tensorflow-gpu==1.15.0
    ```

# Start with NVIDIA cuDNN base image
FROM nvidia/cuda:8.0-cudnn5-devel-ubuntu16.04
MAINTAINER Vladimir Ivanov <ivvl82@gmail.com>

# Install dependencies for Torch:
RUN apt-get update
RUN apt-get install -y --no-install-recommends \
    ca-certificates gcc-4.9 g++-4.9 curl cmake libreadline-dev git-core \
    libqt4-dev libjpeg-dev libpng-dev ncurses-dev imagemagick libzmq3-dev \
    libgfortran-4.9-dev unzip gnuplot gnuplot-x11 ipython
# Install an OpenBLAS package
RUN apt-get install -y --no-install-recommends libopenblas-dev liblapack-dev

# Run Torch7 installation scripts
RUN git clone https://github.com/torch/distro.git /torch --recursive
RUN cd /torch && ./install.sh && cd ..

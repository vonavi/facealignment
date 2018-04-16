# Start with NVIDIA cuDNN base image
FROM nvidia/cuda:8.0-cudnn5-devel-ubuntu16.04
MAINTAINER Vladimir Ivanov <ivvl82@gmail.com>

# Install basic deps
RUN apt-get update && apt-get install -y \
    git sudo

# Run Torch7 installation scripts
RUN git clone https://github.com/torch/distro.git /root/torch --recursive
RUN cd /root/torch && bash install-deps && ./install.sh

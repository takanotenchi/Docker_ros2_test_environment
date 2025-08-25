FROM osrf/ros:humble-desktop-full

# Install Intel GPU driver desktop

RUN sudo apt -y update &&\
    sudo apt install -y wget

# Install Intel GPU driver desktop & camera related utils
# RUN wget -qO - https://repositories.intel.com/graphics/intel-graphics.key | sudo gpg --dearmor --output /usr/share/keyrings/intel-graphics.gpg &&\
#     echo 'deb [arch=amd64,i386 signed-by=/usr/share/keyrings/intel-graphics.gpg] https://repositories.intel.com/graphics/ubuntu jammy arc' | sudo tee  /etc/apt/sources.list.d/intel.gpu.jammy.list &&\
#     sudo apt -y update &&\
#     sudo apt -y install intel-opencl-icd intel-level-zero-gpu \
#         intel-media-va-driver-non-free libmfx1 libmfxgen1 libvpl2 \
#         libegl-mesa0 libegl1-mesa libegl1-mesa-dev libgbm1 libgl1-mesa-dev libgl1-mesa-dri \
#         libglapi-mesa libgles2-mesa-dev libglx-mesa0 libigdgmm12 libxatracker2 mesa-va-drivers \
#         mesa-vdpau-drivers mesa-vulkan-drivers va-driver-all &&\
#     sudo apt -y install libigc-dev intel-igc-cm libigdfcl-dev libigfxcmrt-dev &&\
#     mkdir ~/neo && cd ~/neo &&\
#     wget https://github.com/intel/intel-graphics-compiler/releases/download/igc-1.0.15136.4/intel-igc-core_1.0.15136.4_amd64.deb &&\
#     wget https://github.com/intel/intel-graphics-compiler/releases/download/igc-1.0.15136.4/intel-igc-opencl_1.0.15136.4_amd64.deb &&\
#     wget https://github.com/intel/compute-runtime/releases/download/23.35.27191.9/intel-level-zero-gpu_1.3.27191.9_amd64.deb &&\
#     wget https://github.com/intel/compute-runtime/releases/download/23.35.27191.9/intel-opencl-icd_23.35.27191.9_amd64.deb &&\
#     wget https://github.com/intel/compute-runtime/releases/download/23.35.27191.9/libigdgmm12_22.3.11.ci17747749_amd64.deb &&\
#     sudo dpkg -i *.deb && \
#     cd ~/ && rm -rf ~/neo

RUN sudo apt install guvcview -y && \
    sudo apt install v4l-utils -y && \
    sudo apt install terminator -y && \
    sudo apt install tmux -y &&\
    sudo apt install python3-pip -y

RUN sudo apt install -y build-essential rtklib-qt net-tools tree netcat

RUN pip install --no-cache-dir pyserial && \
    pip install --no-cache-dir sympy

# attach ros
RUN echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc
FROM ros:humble

RUN apt-get update && apt-get install -y curl ros-humble-ros2-control ros-humble-image-transport

RUN curl https://raw.githubusercontent.com/choreonoid/choreonoid/master/misc/script/install-requisites-ubuntu-22.04.sh -o install-requisites-ubuntu-22.04.sh

RUN /bin/sh install-requisites-ubuntu-22.04.sh

RUN echo "source /opt/ros/humble/setup.bash" >> /root/.bashrc

WORKDIR /root/ros2_ws
FROM osrf/ros:indigo-desktop-full


# Installing Catkin Tools
RUN sh -c 'echo "deb http://packages.ros.org/ros/ubuntu `lsb_release -sc` main" > /etc/apt/sources.list.d/ros-latest.list'
RUN apt update && apt install -y wget && \
    wget http://packages.ros.org/ros.key -O - | sudo apt-key add -

RUN apt update && apt install -y python-catkin-tools software-properties-common

# Install Python 3.5
RUN add-apt-repository -y ppa:deadsnakes/ppa && \
    apt update && apt install -y python3.5 python-pip

RUN python -m pip install install empy # Throws errors otherwise
RUN python -m pip install install numpy scikit-learn causalgraphicalmodels causality

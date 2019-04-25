FROM osrf/ros:indigo-desktop-full


# Installing Catkin Tools
RUN sh -c 'echo "deb http://packages.ros.org/ros/ubuntu `lsb_release -sc` main" > /etc/apt/sources.list.d/ros-latest.list'
RUN apt update && apt install -y wget && \
    wget http://packages.ros.org/ros.key -O - | sudo apt-key add -

RUN apt update && apt install -y python-catkin-tools software-properties-common

# Install Python 3.5
RUN add-apt-repository ppa:deadsnakes/ppa && \
    apt update && apt install python3.5 python3.5-dev

RUN pip3.5 install empy # Throws errors otherwise
RUN pip3.5 install numpy scikit-learn CausalGraphicalModels causality

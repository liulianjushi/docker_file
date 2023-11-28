FROM  ubuntu:22.04
MAINTAINER liulianjushi@126.com
ENV LANG C.UTF-8
ENV TZ Asia/Shanghai
ENV DEBIAN_FRONTEND=noninteractive

WORKDIR  /root/
RUN sed -i 's/archive.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list; \
    sed -i 's/security.ubuntu.com/mirrors.ustc.edu.cn/g' /etc/apt/sources.list; \
    apt-get update && apt-get upgrade;\
    apt-get install -y --no-install-recommends libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev libgstreamer-plugins-bad1.0-dev gstreamer1.0-plugins-base gstreamer1.0-plugins-good gstreamer1.0-plugins-bad gstreamer1.0-plugins-ugly gstreamer1.0-libav gstreamer1.0-tools gstreamer1.0-x gstreamer1.0-alsa gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-qt5 gstreamer1.0-pulseaudio;\
    apt-get install -y --no-install-recommends libgstrtspserver-1.0-dev gstreamer1.0-rtsp;\
    apt-get install -y --no-install-recommends python3-gi;\
    apt-get install -y --no-install-recommends pkg-config libcairo2-dev gcc python3-dev python3-pip libgirepository1.0-dev;\
    pip3 config set global.index-url https://mirrors.cloud.tencent.com/pypi/simple; \
    pip3 --no-cache-dir --timeout 3000 install --upgrade pip setuptools gobject PyGObject;\
    apt-get autoremove && apt-get autoclean; \
    rm -rf /var/lib/apt/lists/*	

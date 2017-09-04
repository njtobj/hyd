FROM ubuntu:trusty
MAINTAINER njtobj <cnjsnjjn@163.com> (@njtobj)

RUN rm /bin/sh && ln -s /bin/bash /bin/sh
RUN apt-get update && apt-get install -y software-properties-common
RUN add-apt-repository ppa:beineri/opt-qt59-trusty
RUN apt-get update && apt-get install -y build-essential git mesa-common-dev libglu1-mesa-dev 
RUN rm -rf /var/lib/apt/lists/*

ENV QT_BASE_DIR=/opt/qt59 
ENV QTDIR=$QT_BASE_DIR 
ENV PATH=$QT_BASE_DIR/bin:$PATH 
ENV LD_LIBRARY_PATH=$QT_BASE_DIR/lib/x86_64-linux-gnu:$QT_BASE_DIR/lib:$LD_LIBRARY_PATH 
ENV PKG_CONFIG_PATH=$QT_BASE_DIR/lib/pkgconfig:$PKG_CONFIG_PATH

RUN gcc -v
RUN g++ -v
RUN make -v
RUN qmake -v
RUN ruby -v

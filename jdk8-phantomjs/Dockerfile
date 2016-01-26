FROM dsilahcilar/centos7-jdk8
MAINTAINER Deniz Silahcilar <dsilahcilar@gmail.com>

RUN yum -y install gcc gcc-c++ make flex bison gperf ruby \
    openssl-devel freetype-devel fontconfig-devel libicu-devel sqlite-devel \
    libpng-devel libjpeg-devel git && \ 
    yum clean all
RUN git clone --recurse-submodules https://github.com/ariya/phantomjs.git /opt/phantomjs && \ 
    /opt/phantomjs/build.py && \
    mv /opt/phantomjs/bin/phantomjs /usr/local/bin && \
    rm -Rf /opt/phantomjs
ENV PHANTOMJS_BINARY /usr/local/bin


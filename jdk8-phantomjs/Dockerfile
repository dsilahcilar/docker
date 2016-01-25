FROM dsilahcilar/centos7-jdk8
MAINTAINER Deniz Silahcilar <dsilahcilar@gmail.com>

RUN yum -y install gcc gcc-c++ make flex bison gperf ruby \
      openssl-devel freetype-devel fontconfig-devel libicu-devel sqlite-devel \
      libpng-devel libjpeg-devel git
RUN git clone --recurse-submodules git://github.com/ariya/phantomjs.git /opt/phantomjs
RUN /opt/phantomjs/build.py
ENV PHANTOMJS_BINARY /opt/phantomjs/bin/phantomjs


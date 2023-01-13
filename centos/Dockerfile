FROM centos:latest
MAINTAINER Kei "1363599071@qq.com"
ENV REFRESHED_AT 2023-01-14

RUN cd /etc/yum.repos.d/
RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-*
RUN sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum -y install ruby rubygems rubygem-rake
RUN gem install --no-document rspec ci_reporter_rspec

CMD /bin/bash

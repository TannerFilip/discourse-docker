# -*- sh -*-

# forked from https://gist.github.com/jpetazzo/5494158

FROM	ubuntu:12.04
MAINTAINER	srid


# prevent apt from starting postgres right after the installation
RUN	echo "#!/bin/sh\nexit 101" > /usr/sbin/policy-rc.d; chmod +x /usr/sbin/policy-rc.d

# https://bugs.launchpad.net/ubuntu/+source/lxc/+bug/813398
RUN apt-get -qy install language-pack-en 

ENV LANGUAGE en_US.UTF-8
ENV LANG en_US.UTF-8
ENV LC_ALL en_US.UTF-8
RUN locale-gen en_US.UTF-8
RUN dpkg-reconfigure locales


RUN	DEBIAN_FRONTEND=noninteractive apt-get install -y -q postgresql-client-9.1 postgresql-client-common


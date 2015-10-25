FROM ubuntu:14.04
MAINTAINER Phusion <info@phusion.nl>
ENV DEBIAN_FRONTEND="noninteractive" HOME="/root" TERM="screen"

ADD . /bd_build

RUN /bd_build/prepare.sh && \
	/bd_build/system_services.sh && \
	/bd_build/utilities.sh && \
	/bd_build/cleanup.sh

CMD ["/sbin/my_init"]

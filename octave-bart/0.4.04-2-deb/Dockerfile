FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="octave-bart" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="octave-bart" \ 
    about.summary="Octave bindings for BART" \ 
    about.home="https://mrirecon.github.io/bart/" \ 
    software.version="0.4.04-2-deb" \ 
    upstream.version="0.4.04" \ 
    version="1" \ 
    extra.identifiers.biotools="bart" \ 
    about.copyright="2013-2018 The Regents of the University of California" \ 
    about.license="BSD-3-clause" \ 
    about.license_file="/usr/share/doc/octave-bart/copyright" \ 
    about.tags=""

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y octave-bart || apt-get install -y octave-bart) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker

# Based on https://github.com/gnu-gettext/ci-check/

FROM ubuntu:24.04

LABEL maintainer="Bruno Haible <bruno@clisp.org>"

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update \
    && apt install -y --no-install-recommends \
                   \
                   locales \
                   git \
                   \
                   automake \
                   bison \
                   gperf \
                   perl liblocale-gettext-perl \
                   groff \
                   texinfo \
                   gobjc \
                   fp-compiler fp-units-fcl \
                   gettext \
                   texlive-base texlive-latex-base \
                   \
                   libjson-c-dev libcurl4-gnutls-dev \
                   g++ \
                   gobjc \
                   python3 \
                   clisp \
                   rep \
                   guile-3.0 \
                   openjdk-11-jdk \
                   mono-mcs \
                   gm2 \
                   gdc \
                   fp-compiler fp-units-fcl \
                   ocaml opam \
                   tcl \
                   perl libintl-perl \
                   php \
                   golang-go \
                   ruby ruby-gettext \
                   lua5.4 \
                   gjs \
                   valac \
    && : "Additional packages for the oss-scanner project" \
    && apt install -y --no-install-recommends \
                   build-essential \
                   clang \
                   gdb \
                   strace \
                   ltrace \
                   valgrind \
                   lsof \
                   file \
                   xxd \
                   jq \
                   netcat-openbsd \
                   python3-venv python3-pip \
                   pkg-config \
                   cmake \
    && : "After this line, no more 'apt' commands will work." \
    && rm -rf /var/lib/apt/lists/* \
    && localedef -i ar_SA -f ISO-8859-6 ar_SA.ISO-8859-6 \
    && localedef -i de_DE -f ISO-8859-1 de_DE.ISO-8859-1 \
    && localedef -i de_DE -f UTF-8 de_DE.UTF-8 \
    && localedef -i es_ES -f UTF-8 es_ES.UTF-8 \
    && localedef -i fa_IR -f UTF-8 fa_IR \
    && localedef -i fr_FR -f ISO-8859-1 fr_FR.ISO-8859-1 \
    && localedef -i fr_FR -f UTF-8 fr_FR.UTF-8 \
    && localedef -i ja_JP -f EUC-JP ja_JP.EUC-JP \
    && localedef -i tr_TR -f UTF-8 tr_TR.UTF-8 \
    && localedef -i zh_CN -f GB18030 zh_CN.GB18030

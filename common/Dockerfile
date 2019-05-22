FROM alpine

MAINTAINER hmyh1202 <hmyh1202@163.com>
ENV LANG=en_US.UTF-8

# base app of python3, perl and R
RUN apk update && \
    apk add --no-cache make bash which gcc zlib-dev bzip2-dev xz-dev g++ python3 python3-dev perl R R-dev && \
    ln -sf /bin/bash /bin/sh && \
    pip3 install --upgrade pip && \
    mkdir -p /usr/share/doc/R/html/ /usr/lib/R/library/RColorBrewer/html/ && \
    Rscript -e 'install.packages("RColorBrewer", repos="https://cran.r-project.org/");install.packages("ggplot2", repos="https://cran.r-project.org/");install.packages("plyr", repos="https://cran.r-project.org/");install.packages("reshape2", repos="https://cran.r-project.org/");install.packages("data.table", repos="https://cran.r-project.org/");install.packages("plotrix", repos="https://cran.r-project.org/")'

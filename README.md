# useDocker

Dockerfiles for usefull tools of bioinfo

build images based on alpine

Dockerfile list:

# Dockerfile in common folder:
  contain python3, perl and R
  
  #build docker:
  sudo docker build -t usefultool:v0.0.1 .
  #run docker
  sudo run --rm -it usefultool:v0.0.1 /bin/bash
  #installed packages for soft
  python3: base
  perl: base
  R: RColorBrewer,ggplot2,plyr,reshape2,data.table,plotrix and its dependence
  

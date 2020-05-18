FROM ubuntu
ENV container docker
RUN apt update
RUN apt upgrade -y
RUN DEBIAN_FRONTEND=noninteractive apt install -y \
python3 \
git \
wget \
software-properties-common \
vim \
tar \
curl \
ca-certificates \
apt-transport-https
RUN add-apt-repository ppa:katharaframework/kathara
RUN curl -fsSL https://download.docker.com/linux/ubuntu/gpg | apt-key add -
RUN add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
RUN apt update
RUN DEBIAN_FRONTEND=noninteractive apt install -y \
kathara \
docker-ce 
RUN apt clean
WORKDIR /root

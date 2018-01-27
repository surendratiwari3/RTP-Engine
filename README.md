# Dependency for rtpengine ubuntu 16

## apt-get install debhelper 
## apt-get install iptables-dev
## apt-get install libcurl4-openssl-dev
## apt-get install libpcre3-dev libxmlrpc-core-c3-dev
## apt-get install markdown
## apt-get install libavfilter-dev libavformat-dev libavresample-dev libevent-dev libglib2.0-dev libhiredis-dev libjson-glib-dev libpcap0.8-dev  libpcap-dev libssl-dev

# Install the debhelper (>10) 
## vim /etc/apt/sources.list
## deb http://archive.ubuntu.com/ubuntu xenial-backports main restricted universe multiverse
## sudo apt update
## Check available version of both packages
## apt-cache policy debhelper dh-autoreconf
## sudo apt install dh-autoreconf=12~ubuntu16.04.1 debhelper=10.2.2ubuntu1~ubuntu16.04.1

# Download rtpengine source
## git clone https://github.com/sipwise/rtpengine.git


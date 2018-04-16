# Dependency for rtpengine ubuntu 16

## Dependencies
 - apt-get install debhelper iptables-dev libcurl4-openssl-dev libpcre3-dev libxmlrpc-core-c3-dev markdown libavfilter-dev libavformat-dev libavresample-dev libevent-dev libglib2.0-dev libhiredis-dev libjson-glib-dev libpcap0.8-dev  libpcap-dev libssl-dev dkms module-assistant nfs-common libb-hooks-op-check-perl libexporter-tidy-perl libbencode-perl libcrypt-rijndael-perl libdigest-hmac-perl libio-socket-inet6-perl libsocket6-perl 
 
* Note: if any dependency problem then apt-get -f install

## Install the debhelper (>10) 
- Edit the apt source 
  vim /etc/apt/sources.list ===> deb http://archive.ubuntu.com/ubuntu xenial-backports main restricted universe multiverse
- sudo apt update
- apt-cache policy debhelper dh-autoreconf dh-autoreconf=12~ubuntu16.04.1 debhelper=10.2.2ubuntu1~ubuntu16.04.1

## Download rtpengine source and create the debian package and install
- cd /usr/local/src
- git clone https://github.com/sipwise/rtpengine.git
- cd rtpengine
- ./debian/flavors/no_ngcp
- dpkg-buildpackage
- cd ..
- dpkg -i ngcp-rtpengine-daemon_6.1.0.0+0~mr6.1.0.0_amd64.deb
- dpkg -i ngcp-rtpengine-iptables_6.1.0.0+0~mr6.1.0.0_amd64.deb 
- dpkg -i ngcp-rtpengine-kernel-dkms_6.1.0.0+0~mr6.1.0.0_all.deb
- dpkg -i ngcp-rtpengine-kernel-source_6.1.0.0+0~mr6.1.0.0_all.deb
- dpkg -i ngcp-rtpengine-recording-daemon_6.1.0.0+0~mr6.1.0.0_amd64.deb
- dpkg -i ngcp-rtpengine-utils_6.1.0.0+0~mr6.1.0.0_all.deb
- dpkg -i ngcp-rtpengine_6.1.0.0+0~mr6.1.0.0_all.deb 

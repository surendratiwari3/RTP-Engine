
1. Install the rip-engine
	1. apt-get install dpkg-dev git
	2. cd rtpengine
	3. dpkg-buildpackage
	4. You will get error the you need to check for all unmet dependency .
	5. dpkg-checkbuilddeps
	6. Now above command will give you all unmet dependency
	7. Vim /etc/apt/source.list —> deb http://ftp.debian.org/debian jessie-backports main
	7.   apt-get -t jessie-backports install "debhelper"
	 8. apt-get install debhelper  libmysqlclient-dev iptables-dev libavcodec-dev libavfilter-dev libavformat-dev libavutil-dev libcurl4-openssl-dev  libcurl3-openssl-dev  libevent-dev libglib2.0-dev libhiredis-dev libjson-glib-dev libpcap0.8-dev libpcap-dev libpcre3-dev libssl-dev  libxmlrpc-core-c3-dev markdown zlib1g-dev unzip
        9. Install bcg729
	    VER=1.0.4
            curl   https://codeload.github.com/BelledonneCommunications/bcg729/tar.gz/$VER   >bcg729_$VER.orig.tar.gz
            tar zxf bcg729_$VER.orig.tar.gz
            cd bcg729-$VER
            git clone https://github.com/ossobv/bcg729-deb.git debian
            dpkg-buildpackage -us -uc -sa
	    dpkg -I libbcg729-0_1.0.4-0osso1+deb9_amd64.deb
	    dpkg -I libbcg729-0-dbg_1.0.4-0osso1+deb9_amd64.deb
            dpkg -I libbcg729-dev_1.0.4-0osso1+deb9_amd64.deb
       10. apt-get -t jessie-backports install "libavutil-dev"
	11. dpkg-buildpackage

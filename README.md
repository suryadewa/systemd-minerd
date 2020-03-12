# Install CPUMiner

:example Linux Ubuntu

###### install dependencies
```
sudo apt-get install build-essential libcurl4-openssl-dev libncurses5-dev pkg-config automake yasm
```

###### git location directory & install

```
cd /usr/
git clone https://github.com/pooler/cpuminer
cd cpuminer
./autogen.sh
CFLAGS="-march=native" ./configure
make
make install
```

# systemd-minerd

A systemd unit to manage minerd (cpuminer executable).

Warning: CPU mining is unprofitable!

## Installation

    cp minerd.service /etc/systemd/system/minerd.service
    cp minerdctl /usr/bin/
    
**Make sure to edit pool in minerdctl**

## Usage

Systemd:

    systemctl {enable|start|stop} minerd
    
Management script:

    /usr/bin/minerdctl {start|stop|status|log}

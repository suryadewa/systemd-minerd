# systemd-minerd

A systemd unit to manage minerd (cpuminer executable).

Warning: CPU mining is unprofitable!

## Installation

    cp minerd.service /etc/systemd/system/minerd.service
    cp minerdctl /usr/bin/
    
## Usage

Systemd:

    systemctl {enable|start|stop} minerd
    
Management script:

    /usr/bin/minerdctl {start|stop|status|log}

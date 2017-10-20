## Prerequisites

    sudo apt-get install bridge-utils vlan


## Example usage

    $ sudo ./add-vlans eth0 30 31
    Adding VIDs to interface: eth0

    Allocated VLAN 30:
    344: br-vlan30: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state DOWN mode DEFAULT group default qlen 1000
        link/ether 80:00:00:0d:45:2e brd ff:ff:ff:ff:ff:ff

    Allocated VLAN 31:
    346: br-vlan31: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state DOWN mode DEFAULT group default qlen 1000
        link/ether 80:00:00:0c:45:2e brd ff:ff:ff:ff:ff:ff

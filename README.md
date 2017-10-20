# Prerequisites

    sudo apt-get install bridge-utils vlan


## Example usage

The `cloudlet-setup` script will set up bridged VLANs suitable for attaching to
a TAP interface, address space for each VLAN in the carrier-grade NAT space,
and a `dnsmasq` server suitable for launching cloud instances on the tenant
network.

When running on an Orange Box, make sure to replace `eth0` with the interface
name for the internal network, such as `enx8cae4cdf5349`.

One or more VLAN IDs can be specified after the interface name. Switch ports
must either be trunked, or be allowed on the switch ports relevant to the
tenant.

    $ sudo bin/cloudlet-setup eth0 11 12
    Adding VIDs to interface: eth0

    Allocated VLAN 11:
    344: br-vlan11: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP mode DEFAULT group default qlen 1000
        link/ether 80:00:00:0d:45:2e brd ff:ff:ff:ff:ff:ff

    Allocated VLAN 12:
    346: br-vlan31: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc noqueue state UP mode DEFAULT group default qlen 1000
        link/ether 80:00:00:0c:45:2e brd ff:ff:ff:ff:ff:ff

    Starting dnsmasq on VLAN 11
    Starting dnsmasq on VLAN 12


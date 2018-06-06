# Selective routing over OpenVPN

## Setup

Before use this lists, you need edit OpenVPN profile (ovpn).
Add this to manual routing:
```
pull-filter ignore "redirect-gateway"
```
Optional. If you want use local DNS server (DNS leak!):
```
pull-filter ignore "dhcp-option DNS"
```
More comment this:
```
#setenv opt block-outside-dns
```
Optional. Block IPv6:
```
pull-filter ignore "ifconfig-ipv6 "
pull-filter ignore "route-ipv6 "
```
Now you can add routing lists:
```
config /PATH/TO/FILE/RKN-Jailbreak.conf
```

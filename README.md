# Selective routing over OpenVPN

## Setup

Before use this lists, you need edit OpenVPN profile (ovpn).
Add this to manual routing:
```
pull-filter ignore "redirect-gateway"
```
If you want use local DNS server (DNS leak!):
```
pull-filter ignore "dhcp-option DNS"
```
Now you can add routing lists:
```
config    /PATH/TO/FILE/example.conf
```

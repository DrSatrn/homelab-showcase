Here is a rough idea of my networking stack (early stages) along with what services are running on each host

## Gateway
Run of the mill Telstra Smart modem. Handles inbound/outbound traffic.
No option to forward syslog or setting up custom DNS servers. Major candidate for replacement

## DNS and DHCP Server
Raspberry Pi 2011 c1 running pi-hole for network level ad-block, DNS and DHCP.
DHCP enabled to force all devices to use the custom DNS configured on this box to circumvent the lack of DNS configuration on gateway

## VPN Tunnel
Tailscale service running on a Raspberry Pi 3 allowing approved devices access to LAN when not onsite

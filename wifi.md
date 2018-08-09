## Connecting wifi via terminal

To add wifi network:
> wpa_passphrase YOUR-ESSID YOUR-PASSWORD | sudo tee /etc/wpa_supplicant.conf

To connecto to wifi network (first if down):
> sudo wpa_supplicant -c /etc/wpa_supplicant.conf -i wls1

To freed IPs:
> sudo dhclient -r

To get an IP:
> sudo dhclient wls1

To raise wifi interface:
> sudo ifconfig wls1 up

To scan wifi networks:
> sudo iw wls1 scan

If wifi ping returns "connect: network is unreachable", may be we need to add the gateway:
> sudo ip route add default via 192.168.10.1

# 10:15 - 11:00 – Demo 01 - Cisco SD-WAN: 
## Deployment av ny lokasjon

![MP1](/w02-CNSDQ2/xfiles/HLD_DEMO_01.png "MP1")

## Demo 03
* På plass før demo: K5:SD-WAN-ruter med 1x VPN til Azure-ruter med en klient bak
* Baseline: show vrf på border/edge switch
* Task SDA: Orkestrering av nytt VN (IP-nett, border-handoff/BGP, linknett, etc)
* Verify: show vrf på border/edge switch
* Verify: LAN og WLAN-klient har fått IP i nytt VN (ref Interlude)
* Baseline: konstant ping fra LAN-klient og WLAN-klient mot Azure-klient (ingen ping-reply)
* Baseline: show vrf/vpn på sd-wan ruter (Ahsan?)
* SD-WAN: Orkestrering av nytt VPN (BGP, linknett, etc)
* Verify: show vrf/vpn på sd-wan ruter
* Verify: ping fra LAN-klient og WLAN-klient mot Azure-klient er a-ok
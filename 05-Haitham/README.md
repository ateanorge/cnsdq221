# 13:15 - 14:00 – Demo 03 - Cisco DNA Center og SDA: 
## Deployment av SDA-komponenter

![MP1](/w02-CNSDQ2/xfiles/HLD_DEMO_03.png "MP1")

## På plas før Demo 01
* Shared Services: DNA Center, ISE, AD, DNS, DHCP
* Site20: Fabric Border, Control Plane, Embedded WLC 
* Site20: IP-nett for INFRA_VN, LAN Automation, VN1, ... 
* C9300   Edge-switch wiped (prep4pnp), koblet til Border, console-tilgang
* C9120   Edge-AP wiped, koblet til Edge-switch, console-tilgang
* C3560CX Extended Node wiped, koblet til Edge-switch, console-tilgang
* Demo-VN1, Demo1-SGT, Demo1-AuthZ-Profile, Demo1-AuthZ-Policy
* Demo2-SGT, Demo2-AuthZ-Profile, Demo2-AuthZ-Policy
* Test-klienter (PC1-PCX) lagt til i MAB
* DHCP Scope for INFRA_VN, med DHCP Options for PnP
* DHCP Scopes for Clients
* Clear client DHCP-scopes

## Baseline før Demo 01 - LAN Auto Edge Switch
1. Vise tomt klient-DHCP-scope på DHCP-server
2. I DNAC gå igjennom VN, IP-oppsett for site, SGT/AuthZ oppsett i ISE
3. I DNAC GUI: Edge switch, Edge AP, Exended Node, PC1-PCX ikke å finne i  inventory/Client360
4. Border Switch: Show CDP nei det - ser Edge switch, men ikke noe ip/hostname
5. PC1-PC3: Demonstrere at de ikke har IP-adresse (og ikke wifi-tilkobling på PC2 som er wifi-klient) og kan ikke pinge AD-kontroller (Konstant ping)

## Demo 01: LAN Auto Edge Switch
1. Task: LAN Automation Edge-switch (kjøre console på switchen for å vise output mens den blir provisjonert)
2. Verify: Edge switch er å finne i inventory og Edge klient PC1 er å finne i Client360 og ISE RADIUS logs
3. Verify: PC1 har fått IP-adresse og kan pinge AD-kontroller
4. **Verify: ping klienter på andre sites (Azure)

## Baseline før Demo 01 - PnP Edge AP
1. Baseline: Show CDP nei det fra switch - ser AP, men ikke noe ip/hostname

## Demo 01: PnP Edge AP
1. Task: PnP Edge-AP (kjøre console på switchen for å vise output mens den blir provisjonert)
2. Verify: Edge AP er å finne i inventory og WLAN klient PC2 er å finne i Client360 og ISE RADIUS logs
3. Verify: PC2 har fått IP-adresse og kan pinge AD-kontroller
4. **Verify: ping klienter på andre sites (Azure)

## Baseline før Demo 01 - PnP Extended Node
1. Baseline: Show CDP nei det - ser AP, men ikke noe ip/hostname / Console til AP

## Demo 01: PnP Extenede Node
1. Task: PnP Extended Node (kjøre console på switchen for å vise output mens den blir provisjonert)
2. Verify: Extended Node er å finne i inventory og Extended Node klient PC3 er å finne i Client360 og ISE RADIUS logs
3. Verify: PC3 har fått IP-adresse og kan pinge AD-kontroller
4. **Verify: ping klienter på andre sites (Azure)

## Interlude: prep mellom Demo 01 og Demo 02 - TBD
* Task: endre fra Demo1 til Demo2 SGT/AuthZ for LAN eller WLAN-klient
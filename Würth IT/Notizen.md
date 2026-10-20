## USA HUB:

NA-DC ist WINA DC (usacm01) + WGS Edge DC -> Ein neues DC für komplett USA in Chicago wird aufgebaut
Vertrag läuft Ende April 27 aus -> bis dahin WINA umstellen
Hub muss temp. in NA DC stehen, daher schicken wir zwei Hubs raus für beide DCs. Bei Zeiten dann den Schwenk machen.
Chicago DC Hardware reicht evtl. noch Januar, da wir aktuell nur 4 121G da haben. Evtl. bald neue Bestellung?

Doug oder Nick kontaktieren für Versand, zu denen schicken und die können es dann einbauen (NA DC) -> laut Bernd OK
Aufpassen wegen Kosten, WINA muss Import zahlen, bei entsprechender Menge tut das weh

Delivery Address:
Tou Vang
9485 Winnetka Ave N
Brooklyn Park, MN, USA 5544

Für Chicago mal Bob fragen

Switches in NA DC sind 10G Kupfer -> SFP beachten!! -> evtl. bei FOC nachfragen, die haben wohl viele

Bestellen bei FS.com

ISND erstellt Präfix listen für BGP, Info an Saskia wenn wir die Site-Netze haben

Mit Bernd besprechen wie die Verteilung der Site Hardware läuft, könnte über Brooklyn Park/Nick laufen


### SINGAPUR HUB

Equinix Colocation, 1 Rack
Inbound Shipment -> Equinix Portal -> Saskia macht einen Zugang
Smart Hands buchen -> vollständige Einbauanleitung, idiotensicher machen!!!!!
STROMSTECKER EINPACKEN -> KALTGERÄTEKABEL FÜR PDU, LAN KABEL MIT BESCHRIFTUNG FÜR ALLES -> Achtung Länge, SFPs für alles (Hub und Switch) -> Arista SFPs

Equinix schaltet auch mal gerne eine Stromseite ab für Wartungen -> 91G MEHRERE NETZTEILE EINPACKEN, cross connection

DNS Namen für Edge Hubs definieren und an Saskia senden

wsc01.witglobal.net
wsc02...

wsch-de.witglobal.net
wsch-us…

Singapur hub wird in jedem Fall verschickt, wird über WE abgewickelt
-> wenn Hardware verschickt wird exportantrag stellen, von Bernd oder kollegen zeigen lassen
-> wina 50-60 sites, PRIO USA erster Kunde in jedem Fall 
-> Australien nochmal mit Bernd sprechen, wahrscheinlich sind wir nicht rechtzeitig fertig
-> CC Service ca. 80€ Pro Paket, Preis ist bereits einkalkuliert im WSC Preis, gleich anbieten lassen


### N167 Medientechnik
0157 86025501 -> Maximilian arnold

alles kabelgebunden

48er Switch wird komplett voll -> genug Switches???

fernwartung noch unklar, wenn keine nötig ist dann braucht die anlage an sich auch kein Internet

Einweisung/einbau kw31/32 

QoS muss zwingend eingestellt werden bzgl. Clock Signal, auch wenn switch nicht ausgelastet ist schon wichtig

NAC: Arnold schickt Geräteliste wenn vollständig

Subnetz scheinbar schon vergeben? von JC
theoretisch aber egal, also kann auch von uns vorgegeben werden
da perspektivisch auf Forti umgezogen wird macht es sinn gleich ein netz von uns zu nehmen sonst muss später wieder umkonfiguriert werden

min. 40 IPs -> /26 Netz (62 Adressen)


__________________________________

fragen an Arnold:

wirklich 48 ports?
2,5g ports ein Problem? ab port 37. Ports können kein 10mbit dann
wird alles in einem schrank ankommen, also kein Problem igmp. Alles ein VLAN
DHCP zentral vorgegeben, statische Adressen nötig warum?
warum Internet Access? wenn ja, welche ports


kein nac auf den ports, vlan 83 einstellen
ports alle auf Access einstellen, nicht hybrid oder trunk


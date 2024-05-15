# Einführung

## GNS3 Befehle

| Befehl | Funktion |
| ---- | ---- |
| /system/identity/ set name=R1 | einen Namen setzten |
| /ping IP / Eine IP Pingen |
| /ip/address/ add address=192.168.23.16/24 interface=ether1 | Eine IP einem Ethernet zuweisen |
| /ip/address/ print | IP Adresse ansehen (wie echo) |
| /ip/dhcp-client/ print | Gibt an ob ein DHCP aktiv ist |
| vim /etc/config/network | Netzwerkkonfigurationsdatei öffnen |
| /ip service/print | Überblick über die verfügbaren Services/Konfigurationsschnittstellen |
| /export | Die gesamte Konfiguration des MikroTiks |
| /ip route print | können wir feststellen, dass eine dynamische Default-Route angelegt wurde |
| /ping cloud.tbz.ch | ob ein Uplinks ins Internet besteht |
| /export file=FILENAME | Backup machen |
| /system/package/update/install | updates machen |
| /user ssh-keys import public-key-file=id_rsa.pub user=admin | SSH key hinterlegen |
| /ip/route/add dst-address 0.0.0.0/0 gateway=192.168.96.1 | Route angeben über Terminal |

## VIM commands

| Befehl | Funktion |
| ---- | ---- |
| vim /etc/config/network | Netzwerkkonfigurationsdatei öffnen |
| i | im vim klicken um etwas anzupassen |
| esc -> : -> wq | um aus dem Vim rauszukommen |
| service network reload | reboot |
| vim /etc/config/firewall | Firewall-Konfigurationsdatei öffnen |

## DNS hinzufügen

In folgendes Verzeichnis wechseln: /ip/dhcp-client 
Danach folgenden Befehl: add interface=ether2 disable=no


## Statische IP Konfigurieren

![konfigfile](image.png)

## PI Hole installieren

Folgenden befehlt auf dem DNS ausführen:

`curl -sSL https://install.pi-hole.net | bash`

-> Login Daten merken: 
aBVoxs_i
http://192.168.3.116/admin

Um auf die Website zu kommen muss man noch eine Route öffnen (cmd mit Admin ausführen):

`route add 192.168.3.0 mask 255.255.255.0 192.168.23.135`

Nun noch den DNSSEC aktivieren:
![PI-Hole](image-1.png)

## DHCP Server Konfig anpassen

![DHCP Anpassung](image-2.png)
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

## VIM commands

| Befehl | Funktion |
| ---- | ---- |
| vim /etc/config/network | Netzwerkkonfigurationsdatei öffnen |
| i | im vim klicken um etwas anzupassen |
| esc -> : -> wq | um aus dem Vim rauszukommen |
| service network reload | reboot |
| vim /etc/config/firewall | Firewall-Konfigurationsdatei öffnen |

Labor1 bei punkt 6.3 https://gitlab.com/ch-tbz-wb/Stud/NWA/-/tree/main/2_Unterrichtsressourcen/NWA1_MTCNA/01_Labor_1_DHCP_DNS
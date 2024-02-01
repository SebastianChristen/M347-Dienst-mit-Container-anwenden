# Portfolio "Dienst mit Container anwenden"

Sebastian Christen, INF2022j
![](https://oneclick-cloud.com/wp-content/uploads/2023/08/Bigstock_-139961875-Docker-Emblem.-A-Blue-Whale-With-Several-Containers.-e1574090673987-1.jpg)

2024/02/01, Version Alpha00

In diesem Portfolio kommt der Inhalt vom Modul "M347 Dienst mit Container anwenden".

## Was sind Container?
Ein Container kann man sich am besten so vorstellen, dass er wie eine vereinfachte VM (virtuelle Maschine) ist, welcher einen vom Benutzer bestimmten Prozess laufen lässt. Der Container ist dazu da, ein Docker-Image laufen zu lassen, und wärend der Laufzeit des Containers dieses Image verwendet. Ein Docker-Image, ähnlich wie bei einem VM-Abbild (Image), beinhaltet gewisse Applikationen, Skrips, etc., welche für den Prozess, den man auf Docker ausführen möchte, benötigt werden. Container eignen sich unter Anderem für Skalierbare Webapplikationen, welche je nach Auslastung mehr oder weniger Ressourcen benötigen.

## Was ist DevOps?
DevOps steht für Development und Operations, also Entwicklung und Betrieb. DevOps ist etwa im Jahr 2007 entstanden, aus dem Grund das Entwickler und IT-Experten besorgt darüber waren, wie traditionelle Softwareentwicklung und IT-Betrieb getrennt voneinander abliefen. DevOps ermöglicht es, die Zusammenarbeit zwischen Entwicklern und IT-Teams zu verbessern und Prozesse zu automatisieren. Ein DevOps-Team besteht aus Entwicklern und IT-Experten, die solange zusammenarbeiten, solange die Entwickelte Applikation verwendet wird.

## Unterschied Virtualisierung und Containerisierung
Der Unterschied zwischen Virtualisierung und Containerisierung ist, dass bei einer VM die gesammte Hardware auch virtuallisiert wird, und daher sind VM recht gross, wärend in Containern viel weniger ist, und sie sich das betriebssystem teilen. Deshalb sind Containers kleiner. Dehalb läuft Docker nur auf linux, wegen dem Hostbetriebssystem.
Zusammenfassend sind Containers viel leichter und auch schneller als VMs.

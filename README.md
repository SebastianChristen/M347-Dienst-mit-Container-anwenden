# Portfolio "Dienst mit Container anwenden"

Sebastian Christen, INF2022j
2024/02/01, Version Alpha00
![](https://oneclick-cloud.com/wp-content/uploads/2023/08/Bigstock_-139961875-Docker-Emblem.-A-Blue-Whale-With-Several-Containers.-e1574090673987-1.jpg)

## Was sind Container?

Ein Container kann man sich am besten so vorstellen, dass er wie eine vereinfachte VM (virtuelle Maschine) ist, welche einen vom Benutzer bestimmten Prozess laufen lässt. Der Container ist dazu da, ein Docker-Image laufen zu lassen, und während der Laufzeit des Containers dieses Image verwendet. Ein Docker-Image, ähnlich wie ein VM-Abbild (Image), beinhaltet gewisse Applikationen, Skripte, etc., welche für den Prozess, den man auf Docker ausführen möchte, benötigt werden. Container eignen sich unter anderem für skalierbare Webapplikationen, welche je nach Auslastung mehr oder weniger Ressourcen benötigen.

## Was ist DevOps?

DevOps steht für Development und Operations, also Entwicklung und Betrieb. DevOps ist etwa im Jahr 2007 entstanden, aus dem Grund, dass Entwickler und IT-Experten besorgt darüber waren, wie traditionelle Softwareentwicklung und IT-Betrieb getrennt voneinander abliefen. DevOps ermöglicht es, die Zusammenarbeit zwischen Entwicklern und IT-Teams zu verbessern und Prozesse zu automatisieren. Ein DevOps-Team besteht aus Entwicklern und IT-Experten, die solange zusammenarbeiten, solange die entwickelte Applikation verwendet wird.

## Unterschied Virtualisierung und Containerisierung

Der Unterschied zwischen Virtualisierung und Containerisierung ist, wie sie mit der Hardware und dem Betriebssystem umgehen. Bei VMs wird das OS virtuell nachgebildet, was dazu führt, dass VMs ziemlich groß sind. Container benutzen deutlich weniger Ressourcen, da sie sich das Betriebssystem teilen. Deshalb sind Container kleiner und effizienter. Docker läuft nur auf Linux, weil es stark vom Host-Betriebssystem abhängt. Auf Windows benötigt es Windows Subsystem für Linux. Zusammenfassend sind Container viel leichter und auch schneller als VMs.

## Unterschied Image und Container

Container sind wie lauffähige Kopien von Docker-Images. Ein Docker-Image ist wie eine Anleitung für die Software, und der Container ist wie eine aktive Ausführung dieser Anleitung. Container können flexibel und schnell gestartet, gestoppt und verschoben werden, im Gegensatz zu den statischen Docker-Images, die eher wie feste Anleitungen sind.

## Zusammenfassung der wichtigsten Befehle und ihre Funktion (Diese wird laufend ergänzt)

| Befehl                                        | Funktion                                    |
| --------------------------------------------- | ------------------------------------------- |
| `docker image tag <ersterName> <zweiterName>` | Umbenennen                                  |
| `docker login`                                | sich einloggen                              |
| `docker images -a`                            | zeigt alle Images an                        |
| `docker pull <imageName>`                     | lädt das Image imageName herunter           |
| `docker push <tag>`                           | lädt ein image hoch                         |
| `docker-compose -f docker-compose.yaml up -d` | lädt die compose datei                      |
| `docker system prune --all`                   | löscht nicht benutze container, images etc. |

## Onlyoffice

![](onlyoffice.png)

## Todo-app V1

Screenshot des Frontends für Version 1:

![](todo_task.png)

Screenshot der Images auf Git:
![](docker_images_git.png)

## Aufgabe 1 bei "Ein Image Pushen", Befehle

```bash
docker login git-registry.gibb.ch  # Einloggen
docker image tag todo-app:v1 git-registry.gibb.ch/sch140456/dockermodul/todo-app:v1  # Das Image umbenennen
docker push git-registry.gibb.ch/sch140456/dockermodul/todo-app:v1  # Das Image hochladen
```

## Todo-app V2

Screenshot des Frontends für Version 2:
![Todo-app V2](./todo-app-v2.png)

Screenshot der Images auf Git:
![](./docker-v2-git.png)

## Docker Compose

Docker Compose ist ein Tool, welches von Docker entwickelt wurde und dazu da ist, die Verwaltung von Docker-Containern zu vereinfachen. Mit Docker Compose kann man Image-Erstellung, Container-Starts und -Stops, das Beachten von Reihenfolgen, Links, Ports und Umgebungsvariablen automatisieren. Docker Compose verwendet eine YAML-Datei, in der die Konfiguration von der Container-Anwendung festgelegt wird. Mit einem einzigen Befehl kann man alle Dienste nach dieser Konfiguration erstellen und starten. Es erleichtert die Verwaltung von Docker-Anwendungen und automatisiert komplexe Abläufe.

### Vorgehen, Befehle und Compose-Datei

```bash
sudo apt update
sudo apt install docker-compose
[TODO]
```

## Portainer

Portainer Screenshot:

![](./portainer.png)

### Vorgehen Portainer

I. Portainer gestartet

II. Beim "local" Environment auf "Live Connect" gedrückt

III. Bei "Stack" auf "add stack" gedrückt

IV. Dann habe ich diesen Code hier eingefügt:

![](./portainer-screenshot.png)

V. Auf "Deploy stack" gedrückt

VI. Dann sieht man die Container: ![](./portainer-screenshot-working.png)

## Shop

I. Zuerst habe ich `sudo nano /etc/hosts` ausgeführt, um die Datei zu öffen.

II. Dann auf der untersten Zeile `127.0.0.1    host.docker.internal` hinzugefügt.

III. Schliesslich habe ich `git clone https://git.gibb.ch/thomas.staub/microservices` ausgeführt, um es herunterzuladen.

IV. In den Ordner gehen: `cd microservices/Play.Infra/docker`.

V. `docker-compose -f docker-compose.yaml up -d` ausführen und einen Moment warten, bis es fertig ist.

VI. Dann im Browser auf http://host.docker.internal:5008/ gehen.

## Eigenes Projekt

Im Ordner "uebungsprojekt" befinden sich zwei Dateien: das Dockerfile, welches verwendet wurde, um das Image zu erstellen, welches sich nun auf git-registry.gibb.ch/sch140456/dockermodul/okon-website:v1 befindet. Die andere Datei ist das docker-compose-File. Im docker-compose wird das Image gepullt, und ein Container wird erstellt.

### Wie man das Projekt installiert

Laden Sie dieses GitHub-Repo herunter mit diesen Befehlen:

```bash
git clone https://github.com/Sebastianpkmn/M347-Dienst-mit-Container-anwenden.git
cd ./M347-Dienst-mit-Container-anwenden/uebungsprojekt
docker-compose -f ./docker-compose.yaml up -d
```

Danach sollten Sie auf Docker Desktop folgendes sehen. Sie können nun auf den Link bei "ports" klicken:

![](./okon-on-docker.png)

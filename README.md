# Platformübergreifende Dienste in ein Netzwerk integrieren
``` 
*----------------------------------------------------------------------------*
| Autor: Hajar Hoseyni                          Datum: 14.03.2020            |
|----------------------------------------------------------------------------|
| Modul: 300 /LB2                               Repository: hajhos/mym300prj |
|----------------------------------------------------------------------------|
| Version: 1                                                                 |
*----------------------------------------------------------------------------*
```
## Inhalt
1. [Einleitung](#Einleitung)
2. [Vorbereitung](#Vorbereitung)
3. [Webserver](#Webserver)
4. [mmdb](#mmdb)
5. [Test](#Test)
6. [Quellen](#Quellen)
___
### Einleitung
Mit diesem Dokument wird man über untenstehende Themen erfahren.
- Ein **Webserver** mit **Vagrant** in ein Netzwerk integrieren.
- Ein **Multi Machine DB** mit Vagrant in ein Netzwerk integrieren.
- Die Dienste auf dem Github-Repository pushen. 
___
### Vorbereitung
- Auf dem **Github** ein neuen Repository erstellen.
- Der Repository auf dem lokalen Speicher clonen.
```
git clone git@github.com:hajhos/mym300prj.git
```
- Auf diesem Verzeichnis **Gitbash** starten.
___
### Webserver
Webserver-Dokumentation ist unter folgenden Link vorhanden.
https://github.com/hajhos/mym300prj/blob/master/web/README.md
___
### mmdb
Multi Machine DB-Dokumentation ist unter folgenden Link vorhanden.
https://github.com/hajhos/mym300prj/blob/master/mmdb/README.md
___
### Test
- [x] Die konfigurierte Dienste funktionieren.
- [x] Die Vagrantfiles sind erfolgreich auf dem Repository gepusht.
___
### Quellen
- https://github.com/adam-p/markdown-here/wiki/Markdown-Here-Cheatsheet
- https://github.com/mc-b/M300/tree/master/vagrant/mmdb
- M300-Lernmittels
 
 
 
 
 
 
 
 ## Ubuntu /Docker mit MySql-Server

```
*-----------------------------------------------------------------------*
| Notebook                                 Homenetz: 192.168.1.0/24     |                      
| Virtelle Umgebung: Virtualbox 6.1.2      IP-Adresse: 10.0.2.15/24     |
*-----------------------------------------------------------------------*	

*---------------------------------------*                
|Datenbank: MySql Server                |
|Container                              |
|Container-Engine: Docker               |
|Gast OS: Ubuntu 16.04                  |
|Hypervisor: VBox                       |
|Host-OS: Windows 10                    |
*---------------------------------------*	
```
##### Docker 
| Server              | Hostname            | IP-Adresse          | Netz                | Port                |
|:--------------------|:--------------------|:--------------------|:--------------------|:--------------------|
| Web-Server: apache2 | lb2web              | 192.168.2.201       | NAT: 80             | 8080                |
| DB-Server: mysql    | lb2db               | 192.168.2.200       | __                  | 3306                |

- Der mmdb-Vagranfile lokal speichern.
- Der Code nach eigene Anforderungen anpassen. 
- Beim IP-Anpassungen muss diese Änderung auf dem **db.sh** auch eingetragen werden.
- Die Server (mysql & apache2) sind im gleichen Netz (192.168.2.0).
- Die Änderungen speichern. (auf vim -> :wq)
- Vagrant up
``` 
cd c:/Users/hajar/mym300prj/mmdb 
vagrant up 
```
- **Vagrant** sucht im Internet nach aufgerufene Dienst. Nachher werden die Dateien local speichern.
- Web-Server und DB-Server laufen auf dem Virtualbox.
- Zugriff auf dem Weboberfläche für Mysql-User ist wie folgt:

<p> URL: http://localhost:8080/adminer.php <br>
 
**LOGIN-ANGABE:**  `Username: User` `Password: admin`

![](login.JPG)

![](eingelogt.JPG)

- **Vagrantfile**, **Readme.md** , **Fotos**, **.gitignore** und **db.sh** auf dem Github-Repository pushen.

`Test`
- [x] Beim Aufruf der URL wird der Adminer.php loginseite angezeigt.
- [x] **Vagrantfile**, **Readme.md**, **Fotos**, **.gitignore** und **db.sh** erfolgreich auf dem Github-Repository gepusht.

##### Zurück zur LB2Dokumentation: https://github.com/hajhos/mym300prj/blob/master/LB2Dokumentation.md

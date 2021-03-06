## Docker mit MySql Server erstellen

```
*-----------------------------------------------------------------------*
| Notebook                                 Homenetz: 192.168.1.0/24     |                      
| Virtelle Umgebung: Virtualbox 6.1.2      IP-Adresse: 10.0.2.15/24     |
*-----------------------------------------------------------------------*	

*---------------------------------------*                
|Datenbank: MySql Server 8.0.1          |
|Container                              |
|Container-Engine: Docker               |
|Gast OS: Ubuntu 16.04                  |
|Hypervisor: Virtualbox                 |
|Host-OS: Windows 10                    |
*---------------------------------------*	
```
##### Docker erstellen
- Der MySql Server Dockerfile von der Webseite https://hub.docker.com/r/mysql/mysql-server auf die VM pullen.
```
docker pull mysql/mysql-server:8.0.1
```
- Das MySql Image, welche auf dem Server gespeicher ist, laufen lassen.
```
docker run --name my-own-mysql -e MYSQL_ROOT_PASSWORD=mypass123 -d mysql:8.0.1 #--name: Imagesname, Rootpassword, -d: Docker im Hintergrund laufen lassen, mysql: Version
```
- Nun ist der Docker erstellt. Wir können das **image** und **Docker** mit untenstehenden Befehlen kontrollieren.
```
docker images #Die vorhandene Docker images werden angezeigt
docker ps     #Die laufende Dockers werden angezeigt
```
![](dockercontroll.JPG)

- Um der MySql Server grafisch darzustellen, installiere Ich PHP-Myadmin Docker. Die Installation dafür befindet sich unter dem Link 
https://github.com/hajhos/m300lb3/blob/master/PhpMyAdmin.md.

`Test`
- [x] Ist der Zugriff auf dem MySql Server möglich.
- [x] Sind die Befehle sauber dokumentiert und getestet.

##### Zurück zur Haupt-Dokumentation: https://github.com/hajhos/m300lb3

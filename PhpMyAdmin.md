## PhpMyadmin als Weboberfläche für MySql Server installieren
```
*---------------------------------------*                
|Container                              |
|Container-Engine: Docker               |
|Gast OS: Ubuntu 16.04                  |
|Hypervisor: Virtualbox                 |
|Host-OS: Windows 10                    |
*---------------------------------------*	
```
##### Übersicht
| IP-Adresse          | Port                | DB-Server           |
|:--------------------|:--------------------|:--------------------|            
| local               | 8081                | MySql               |

- Der PhpMyadmin Dockerfile von der Webseite https://hub.docker.com/r/phpmyadmin/phpmyadmin auf die VM pullen.
```
docker pull phpmyadmin/phpmyadmin:latest
```
- Das Image laufen lassen.
```
docker run --name my-own-phpmyadmin -d --link my-own-mysql:db -p 8081:80 phpmyadmin/phpmyadmin #PhpyMyadmin wird auf port 8081 aufgerufen -p: Portnummer
``` 
- Nun lauft der MySql DB auf PhpMyadmin Weboberfläche. Mit untenstehenden Link kann man die MySql DB mit der Weboberfläche aufrufen. 
<p> URL: http://localhost:8081/ <br>
 
![](web.jpg)
 
**LOGIN-ANGABE:**  `Username: Root` `Password: mypass123 #Das Root-Password vom MySql Server Docker`

![](phpdb.JPG)

`Test`
- [x] Ist der Zugriff auf dem MySql Server durch PhpMyadmin möglich.
- [x] Sind die Befehle sauber dokumentiert und getestet.

##### Zurück zur Haupt-Dokumentation: https://github.com/hajhos/m300lb3



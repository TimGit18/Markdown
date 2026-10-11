# Ubuntu

Ubuntu kann unter Windows Subsystem für Linux (WSL) nativ ausgeführt werden. 

## Installation neuer Software

Bevor die neue Software installiert werden kann, muss zunächst der Installer selbst aktualisiert werden. 
Ansonsten kann die neue Software nicht korrekt lokalisiert werden. 

`sudo apt update`

Erst dann kann das neue Paket komplett installiert werden, zum Beispiel eine Latex-Distribution: 

`sudo apt install texlive-full`

Dafür benötigt Ubuntu den Root-Account und das Passwort:

`Root: tim`  
`Root-Passwort: ******`


# Wireless Tethering Shooting mit der Canon R5/R6/R6II unter Windows 10

In meinem Homestudio nutze ich gerne „Tethering Shooting“ um das gerade gemachte Bild auf einem 
Rechner anzuzeigen, so das die Kundschaft das Bild schon direkt sehen kann. 
Hier möchte ich eine kurze Anleitung zu meinem Setup mit der R5 vorstellen:

1. Vorbereitung des Rechners
1.1 Herausfinden der IP-Adresse des Rechners
1.2 Installation des FTP-Server
1.3 Konfiguration des FTP-Server

2.   Vorbereiten der R5
2.1  WLAN-Einstellungen
2.2  Test der Verbindungen
     
3. Anzeigegeräte einrichten
3.1 IrfanView konfigurieren
3.2 Anzeigen auf mehreren Geräten
3.3 Tethershoot mit NAS-System

# 1. Vorbereitung des Rechner
1.1 Herausfinden der IP-Adresse des Rechners

Um heraus zu finden welche IP-Adresse der Rechner hat, bitte folgendes auf dem Rechner ausführen:
In der Suchleiste gibt man „CMD“ ein, gefolgt von der Returntaste.  
Es öffnet sich die Eingabeaufforderung:

![Tethershoot 1 4-2](https://github.com/user-attachments/assets/b5f833be-6c37-4864-834e-9b9d13c3de62)

Im schwarzen Fenster gibt man den Befehl: ipconfig und drückt die Returntaste.

![Tethershoot 1 4-2_2](https://github.com/user-attachments/assets/2ef604c7-fbc2-4e0a-8ba5-0d1602018eca)

Unter Ethernet-Adapter Ethernet sollte dann unter „IPv4-Adresse“ die lokale IP-Adresse des Rechners 
angezeigt werden.
Sollte der Rechner nur mit WLAN verbunden sein, muss man unter „Drahtlos-LAN-Adapter WLAN“ die 
dortige IPv4-Adresse benutzen.
Wir notieren/merken uns die IP-Adresse des Rechners. In unserem Beispiel: 192.168.2.205

1.2 Installation des FTP-Servers

Wir laden uns unter: 
https://filezilla-project.org/download.php?type=server
den Filezilla -FTP-Server herunter und installieren ihn.



![Tethershoot 1 4-3](https://github.com/user-attachments/assets/fca6ae9f-ceae-4677-8766-c242b97d6420)

![Tethershoot 1 4-4](https://github.com/user-attachments/assets/dfb9fbd1-4f6f-49fb-b0b7-3975999b41d4)

![Tethershoot 1 4-5](https://github.com/user-attachments/assets/b586b14f-0818-45be-83d5-2e4cd71c6152)

![Tethershoot 1 4-6](https://github.com/user-attachments/assets/0793849b-d4ae-4223-b6b7-cd8215c5a5c2)

![Tethershoot 1 4-7](https://github.com/user-attachments/assets/7d5130a4-8a8a-4c12-9333-152c54b46946)

Nach erfolgreicher Installation und Authentifizierung öffnet sich die Adminkonsole und wir können nun den 
FTP-Server konfigurieren.

1.3 Konfiguration des FTP-Server

Dazu oben in der linken Ecke auf „Server“ und dann auf “configure“.

![Tethershoot 1 4-8](https://github.com/user-attachments/assets/b653633c-8e72-4f59-9c09-51ca2343a144)

![Tethershoot 1 4-9](https://github.com/user-attachments/assets/aae66fb1-6768-49a2-8cdd-5ce4e2a61024)

Ich habe unter dem User „anonymous“ folgende Mountpoints angelegt:
Virtual Path: /
Native Path: D:\picftp

Der Virtual Path ist das Stammverzeichnis des FTP-Servers 
Der Native Path das Verzeichnis wo später die Bilder hin übertragen werden im Rechner (z.B D:\picftp)

Falls wer noch etwas ausführlichere Hilfe benötigt:

https://www.youtube.com/watch?v=CzFzunrAYA0&t=333s

# 2. Vorbereitung der R5












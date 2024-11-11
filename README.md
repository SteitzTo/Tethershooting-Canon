# Wireless Tethering Shooting mit der Canon R5/R6/R6II unter Windows 10

In meinem Homestudio nutze ich gerne „Tethering Shooting“ um das gerade gemachte Bild auf einem 
Rechner anzuzeigen, so das die Kundschaft das Bild schon direkt sehen kann. 
Hier möchte ich eine kurze Anleitung zu meinem Setup mit der R5 vorstellen:

1. Vorbereitung des Rechners<br>
1.1 Herausfinden der IP-Adresse des Rechners<br>
1.2 Installation des FTP-Server<br>
1.3 Konfiguration des FTP-Server<br>

2.   Vorbereiten der R5<br>
2.1  WLAN-Einstellungen<br>
2.2  Test der Verbindungen<br>
     
3. Anzeigegeräte einrichten<br>
3.1 IrfanView konfigurieren<br>
3.2 Anzeigen auf mehreren Geräten<br>
3.3 Tethershoot mit NAS-System<br>

# 1. Vorbereitung des Rechner
## 1.1 Herausfinden der IP-Adresse des Rechners

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

## 1.2 Installation des FTP-Servers

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

## 1.3 Konfiguration des FTP-Server

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

# 2. Vorbereitung der Canon R5

Menu → Reiter  „Verbindungen“<br>

![Tethershoot 1 4-10](https://github.com/user-attachments/assets/a0c16b0b-798f-4269-94f6-c29e051afb84)

Dann : WLAN/ Bluetoothverbindung
Bilder zum FTP-Server übertragen
Gerät für Verbindung hinzufügen
Offline Konfigurieren
FTP
Adressen-Einstellungen
Dort sollte nun die IP-Adresse des Rechners, wo die Bilder hin übertragen werden, eingetragen werden:
Wir tragen bei Adressen-Einstellung die IP-Adresse des Ziel-Rechners ein: 
In meinem Fall: 192.168.2.205
Portnummereinstellung bleibt auf: 00021
Danach dann auf OK gehen.
Passiver Modus: Deaktivieren
Proxyserver: Deaktivieren
Anmeldemethode: Anonym
Zielordner: Stammverzeichnis
Danach sollte man wieder im „Verbindungsmenu“ angelangt sein.

Man wählt wieder “Bilder zum FTP-Server“ übertragen.
Nun sollte es einen Eintrag mit der IP-Adresse des Zielrechners geben.
Dieser ist auszuwählen

Danach muss man noch das WLAN konfigurieren um die Kamera ins WLAN zu bringen 
(falls noch nicht geschehen)

<ins>Wenn die Meldung „Verbunden mit FTP-Server“ erscheint, ist alles richtig eingestellt.</ins>

Mit Druck auf die „Menü-Taste“ kehrt man zum „Verbindungsmenu“ zurück.

## 2.1 WLAN-Einstellungen

Man wähle denn den Menüpunkt „WLAN-Einstellungen“ und dort dann „FTP-Übertragungseinstellungen

Autom. Übertragen auf Aktiviert
Übertrag. Typ/Größe kann man selbst bestimmen was man wählt. 
                 
Zur Vorschau der Bilder auf dem Rechner reicht JPEG Größe Übertrag auf Klein.JPEG

<ins>Diese Einstellungen haben scheinbar keinen großen Einfluss auf die Bildgröße.
Es wird die Bildgröße von den normalen Größeneinstellungen der Kamera übernommen.
Dort dann also für kleines JPG die Einstellung S2 wählen.</ins>

Sollten doch auch das RAW übertragen werden, dann:
RAW+JPEG-Übertrag. Auf Nur RAW oder auch RAW+JPEG einstellen.
Der Rest der Einstellungen habe ich nicht angepasst.

## 2.2 Test der Verbindung

Um die Verbindung zu testen mach ich ein Bild mit der R5 und schaue danach in meinem 
eingestellten Verzeichnis des Rechners nach, ob sich darin ein Bild befindet.
Die Übertragungszeit dauert ein paar Sekunden also da kurz etwas Geduld aufbringen.
Mein kleines JPG benötigt etwas 4 Sekunden um im Ordner zu erscheinen. 
Das Raw ca. 35 Sekunden um vollständig übertragen zu werden.
Diese Zahlen können natürlich je nach Netzwerk stark schwanken.

# 3. Anzeigegeräte vorbereiten

## 3.1 IrfanView konfigurieren

Ich gehe in meiner Anleitung davon aus das die neuste Version von IrfanView samt PlugIns bereits
auf dem Rechner installiert ist.

Öffne IrfanView

![Tethershoot 1 4-11](https://github.com/user-attachments/assets/c9cf5cd9-2616-422f-a252-8e549623a0fb)

Wähle unter „Optionen“ → HotFolder aus.

Im folgenden Dialogfeld wählst du das Verzeichnis auf dem Anzeigegerät aus, in welches du die 
Bilder überträgst. Man kann noch einstellen wie lange die Bilder angezeigt werden sollen.
Bei mir hier 15 Sekunden, danach wird das Bild dann abgedunkelt.

![Tethershoot 1 4-12](https://github.com/user-attachments/assets/830c1b6f-777b-4596-9e1c-a5a61bdf5a93)

Bei Klick auf „Start“ verschwindet das Fenster, ist aber im Hintergrund aktiv.
Nachdem ich ein Bild gemacht habe, öffnet sich das Fenster direkt und zeigt das erste Bild an.
Möchte man das ganze im Vollbildmodus genießen, bitte an dem Punkt die Returntaste drücken.

<ins>Info: Falls man RAW+JPEG gleichzeitig überträgt, funktioniert das ganze mit IrfanView nur eingeschränkt.
Die Dateien werden übertragen, das JPG auch angezeigt, aber beim RAW erscheint einen Fehlermeldung 
(Dekodierungsfehler) welche weggeklickt werden muss. Somit stoppt der Workflow und die Fehlermeldung 
bleibt auf dem Bildschirm stehen.</ins>

## 3.2 Anzeigen auf mehreren Geräten

Es ist auch möglich das Verzeichnis das man im FTP-Server eingestellt hat 
(bei mir d:\picftp) im Netzwerk freizugeben. 

(Schreib und Lese Rechte der Freigabe, sowie des Verzeichnisses sollten auf Lesen/Schreiben stehen).

Das ermöglicht wiederum von einem anderen Windowsrechner auf dieses Verzeichnis zuzugreifen und über 
die Hot-Folderoption von Irfanview einzubinden. 
(Netzlaufwerk verbinden sowie UNC-Pfad funktionieren)
Somit hat man die Möglichkeit, das gerade gemacht Bild auf 2 Rechner gleichzeitig an zu zeigen.
Bei mir liegt die Übertragungszeit bei ca 4 Sekunden auf  2 Geräte.

## 3.3 Tethershooting mit Nas-System

Es ist auch möglich auf einem NAS-Server (in meinem Fall von Qnap) einen FTP-Server einzurichten und 
die Bilder direkt zur NAS zu senden.
Möchte man die Bilder dann gleichzeitig wieder über Irfanview anzeigen, sollte man eine SMB-
Dateifreigabe des FTP- Verzechnisses einrichten und über die Hotfolder-Option von Irfanview darauf 
zugreifen.

Hoffe ich kann jemand damit helfen.

























[Robotername]: Adeept_PiCar-B

[RobotURL]: https://github.com/adeept/adeept_picar-b

[RobotGit]: https://github.com/adeept/adeept_picar-b.git

[Offizielle Raspberry Pi-Website]: https://www.raspberrypi.org/downloads/

[Image-Datei für den Raspberry Pi Robot]: https://adeept-my.sharepoint.com/personal/tomsun_adeept_onmicrosoft_com/_layouts/15/onedrive.aspx?id=%2Fpersonal%2Ftomsun%5Fadeept%5Fonmicrosoft%5Fcom%2FDocuments%2FadeeptRaspTank&amp;originalPath=aHR0cHM6Ly9hZGVlcHQtbXkuc2hhcmVwb2ludC5jb20vOmY6L2cvcGVyc29uYWwvdG9tc3VuX2FkZWVwdF9vbm1pY3Jvc29mdF9jb20vRXZCZmhES1dJVEJLb1ZLejFJTThta01CaWc5SHRiZG9sMXdLQU83WTk5cFJWdz9ydGltZT1rUWxJeE9EMjEwZw

[Offizielle Website]: https://www.adeept.com/

[GitHub]: https://github.com/adeept/adeept_picar-b

[Dokumentation zur Strukturmontage]: https://www.adeept.com/learn/detail-33.html

## Inhalt

----
* [Erste Schritte mit Raspberry Pi Robot und Python](#Inhalt)
    * [1. Prämisse](#1-Prämisse)
       * [1.1 STEAM und Raspberry Pi](#11-STEAM-und-Raspberry-Pi)
       * [1.2 Über die Dokumentation](#12-über-die-dokumentation)
    * [2. Raspberry Pi Systeminstallation und Einrichtung der Entwicklungsumgebung](#2-Raspberry-Pi-Systeminstallation-und-Einrichtung-der-Entwicklungsumgebung)
       * [2.1 Installieren Sie ein Betriebssystem für den Raspberry Pi](#21-Installieren-Sie-ein-Betriebssystem-für-den-Raspberry-Pi)
       * [2.1.1 Methode A: 'Raspbian' von Raspberry Pi Imager auf die SD-Karte schreiben](#211-Methode-A-Raspbian-mit-Raspberry-Pi-Imager-auf-die-SD-Karte-schreiben)
       * [2.1.2 Methode B: Laden Sie die Image-Datei Raspbian herunter und schreiben Sie sie manuell auf die SD-Karte](#212-Methode-B-Laden-Sie-die-Image-Datei-Raspbian-herunter-und-schreiben-Sie-sie-manuell-auf-die-SD-Karte)
       * [2.1.3 Methode C: Manuelles Herunterladen der von uns bereitgestellten Bilddatei und Schreiben auf die SD-Karte (nicht empfohlen)](#213-Methode-C-Laden-Sie-die-von-uns-bereitgestellte-Imagedatei-manuell-herunter-und-schreiben-Sie-sie-auf-die-SD-Karte-nicht-empfohlen)
       * [2.2 SSH-Server von Raspberry Pi aktivieren](#22-SSH-Server-des-Raspberry-Pi-aktivieren)
       * [2.2.1 Methode A: SSH mit Peripheriegeräten aktivieren](#221-Methode-A-SSH-mit-Peripheriegeräten-aktivieren)
       * [2.2.2 Methode A: SSH ohne Peripheriegeräte aktivieren](#222-Methode-A-SSH-ohne-Peripheriegeräte-aktivieren)
       * [2.3 WLAN auf Raspberry Pi konfigurieren](#23-WLAN-auf-Raspberry-Pi-konfigurieren)
       * [2.3.1 Methode A: WLAN-Verbindung mit Peripheriegeräten](#231-Methode-A-WLAN-Verbindung-mit-Peripheriegeräten)
       * [2.3.2 Methode A: WLAN-Verbindung ohne Peripheriegeräte](#232-Methode-A-WLAN-Verbindung-ohne-Peripheriegeräte)
    * [3 Melden Sie sich beim Raspberry Pi an und installieren Sie die App](#3-Melden-Sie-sich-beim-Raspberry-Pi-an-und-installieren-Sie-die-App)
       * [3.1 Bei Raspberry Pi anmelden (Windows 10)](#31-Bei-Raspberry-Pi-anmelden-Windows-10)
       * [3.2 Beim Raspberry Pi anmelden (Linux oder Mac OS)](#32-Beim-Raspberry-Pi-anmelden-Linux-oder-Mac-OS)
       * [3.3 Bei Raspberry Pi anmelden (Windows 8 oder Vorgängerversion)](#33-Bei-Raspberry-Pi-anmelden-Windows-8-oder-Vorgängerversion)
       * [3.4 Download-Programm des Raspberry Pi-Roboters](#34-Download-Programm-des-Raspberry-Pi-Roboters)
       * [3.5 Entsprechende abhängige Bibliotheken installieren](#35-Entsprechende-abhängige-Bibliotheken-installieren)
       * [3.6 Führen Sie das Programm des Raspberry Pi-Roboters aus](#36-Führen-Sie-das-Programm-des-Raspberry-Pi-Roboters-aus)
    * [4 Raspberry Pi Strukturmontage und Vorsichtsmaßnahmen](#4-Raspberry-Pi-Strukturmontage-und-Vorsichtsmaßnahmen)
       * [4.1 Dokumentation zur Strukturmontage](#41-Dokumentation-zur-Strukturmontage)
       * [4.2 Tipps für den strukturellen Zusammenbau](#42-Tipps-für-den-strukturellen-Zusammenbau)
       * [4.3 Tipps zur Strombereitstellung](#43-Tipps-zur-Strombereitstellung)
    * [5 Roboter über WEB-App steuern](#5-Roboter-über-WEB-App-steuern)
    * [6 Häufige Probleme und Lösungen (Fragen und Antworten)](#6-Häufige-Probleme-und-Lösungen-Fragen-und-Antworten)
    * [7 Stellen Sie das Programm so ein, dass es automatisch startet](#7-Stellen-Sie-das-Programm-so-ein-dass-es-automatisch-startet)
       * XXXXXXXXX[7.1 Festlegen, dass das angegebene Programm beim Booten automatisch ausgeführt wird](#71-Festlegen-dass-das-angegebene-Programm-beim-Booten-automatisch-ausgeführt-wird)
       * [7.2 Ändern Sie das Programm, das automatisch startet](#72-Ändern-Sie-das-Programm-das-automatisch-startet)
XXXXXXXXX
    * [8 Remote-Bedienung von Raspberry Pi über MobaXterm](#8-Fernbedienung-von-Raspberry-Pi-über-MobaXterm)
    * [9 So steuern Sie die WS2812 RGB-LED](#9-So-steuern-Sie-die-WS2812-RGB-LED)
    * [10 So steuern Sie den Servo](#10-So-steuern-Sie-den-Servo)
       * [10.1 Steuern Sie das Lenkgetriebe, um sich in einen bestimmten Winkel zu drehen](#101-Steuern-Sie-das-Lenkgetriebe-um-sich-in-einen-bestimmten-Winkel-zu-drehen)
       * [10.2 Steuern Sie die Zeitlupe des Lenkgetriebes](#102-Steuern-Sie-die-Zeitlupe-des-Lenkgetriebes)
       * [10.3 Nicht-blockierende Kontrolle](#103-Nicht-blockierende-Kontrolle)
    * [11 So steuern Sie den Gleichstrommotor](#11-So-steuern-Sie-den-Gleichstrommotor)
    * [12 Ultraschallmodul](#12-Ultraschallmodul)
    * [13 Linienverfolgung](#13-Linienverfolgung)
    * [14 Machen Sie ein Polizeilicht oder ein atmendes Licht](#14-Machen-Sie-ein-Polizeilicht-oder-ein-atmendes-Licht)
       * [14.1 Multi-Threading-Einführung](#141-Multi-Threading-Einführung)
       * [14.2 Realisierung von Polizeilichtern / atmenden Lichtern](#142-Realisierung-von-Polizeilichtern--atmenden-Lichtern)
       * [14.3 Warnlichter oder atmende Lichter in anderen Projekten](#143-Warnlichter-oder-atmende-Lichter-in-anderen-Projekten)
    * [15 Echtzeit-Videoübertragung](#15-Echtzeit-Videoübertragung)
    * [16 Automatische Hindernisvermeidung](#16-Automatische-Hindernisvermeidung)
    * [17 OpenCV Multithreading wird zur Verarbeitung von Videoframes verwendet](#17-OpenCV-Multithreading-wird-zur-Verarbeitung-von-Videoframes-verwendet)
       * [17.1 Single-Thread-Verarbeitung von Videoframes](#171-Single-Thread-Verarbeitung-von-Videoframes)
       * [17.2 Multi-Thread-Verarbeitung von Video-Frames](#172-Multi-Thread-Verarbeitung-von-Videoframes)
    * [18 OpenCV, Lernen Sie OpenCV zu verwenden](#18-OpenCV-Lernen-Sie-OpenCV-zu-verwenden)
    * [19 Verwenden von OpenCV zum Realisieren von Farberkennung und -verfolgung](#19-Verwenden-von-OpenCV-zur-Realisierung-von-Farberkennung-und--verfolgung)
       * [19.1 Farberkennung und Farbraum](#191-Farberkennung-und-Farbraum)
       * [19.2 Prozess der Farbidentifizierung und -verfolgung](#192-Prozess-der-Farberkennung-und--verfolgung)
       * [19.3 Spezifischer Code](#193-Spezifischer-Code)
       * [19.4 HSV-Farbkomponentenbereich in OpenCV](#194-HSV-Farbkomponentenbereich-in-OpenCV)
    * [20 Maschinenlinienverfolgung basierend auf OpenCV](#20-Maschinenlinienverfolgung-basierend-auf-OpenCV)
       * [20.1 Sichtlinieninspektionsprozess](#201-Sichtlinieninspektionsprozess)
       * [20.2 Spezifischer Code](#202-Spezifischer-Code)
    * [21 Spracherkennung](#21-Spracherkennung)
       * [21.1 Spezifischer Code](#211-Spezifischer-Code)
    * [22 Radarscan](#22-Radarscan)
       * [22.1 Spezifischer Code](#221-Spezifischer-Code)
    * [23 Einen WLAN-Hotspot auf dem Raspberry Pi erstellen](#23-Einen-WLAN-Hotspot-auf-dem-Raspberry-Pi-erstellen)
    * [24 GUI-abhängiges Element unter Microsoft Windows installieren](#24-GUI-abhängiges-Element-unter-Microsoft-Windows-installieren)
       * [24.1 GUI-Abhängigkeiten installieren](#241-GUI-Abhängigkeiten-installieren)
    * [25 So wird die GUI verwendet](#25-So-wird-die-GUI-verwendet)
    * [26 Steuerung der WS2812 LED über die GUI](#26-Steuerung-der-WS2812-LED-über-die-GUI)
    * [27 Echtzeit-Videoübertragung basierend auf OpenCV](#27-Echtzeit-Videoübertragung-basierend-auf-OpenCV)
    * [28 OpenCV verwenden, um Videoframes auf dem PC zu verarbeiten](#28-OpenCV-verwenden-um-Videoframes-auf-dem-PC-zu-verarbeiten)
    * [29 UART aktivieren](#29-UART-aktivieren)
       * [29.1 Mini-UART und CPU-Kernfrequenz](#291-Mini-UART-und-CPU-Kernfrequenz)
       * [29.2 Deaktivieren der Verwendung von Konsolen-UART durch Linux](#292-Deaktivieren-der-Verwendung-von-Konsolen-UART-durch-Linux)
       * [29.3 UART-Ausgabe auf GPIO-Pins](#293-UART-Ausgabe-auf-GPIO-Pins)
       * [29.4 UARTs und Gerätebaum](#294-UARTs-und-Gerätebaum)
       * [29.5 Relevante Unterschiede zwischen PL011 und Mini-UART](#295-Relevante-Unterschiede-zwischen-PL011-und-Mini-UART)
    * [30 Steuerung Ihres PiCar-B mit einem Android-Gerät](#30-Steuerung-Ihres-PiCar-B-mit-einem-Android-Gerät)
    * [Abschluss](#Abschluss)


## 1. Prämisse


### 1.1 STEAM und Raspberry Pi

STEAM steht für Wissenschaft, Technologie, Ingenieurwesen, Kunst und Mathematik.
Es ist eine Art transdisziplinäre Bildungsidee, die auf die Praxis ausgerichtet ist.
Als Board, das für die Ausbildung in Computerprogrammierung entwickelt wurde, hat Raspberry Pi viele Vorteile gegenüber anderen Roboterentwicklungsboards.
Daher wird Raspberry Pi zur Funktionskontrolle des Roboters verwendet.


### 1.2 Über die Dokumentation

Diese Dokumentation ist eine Softwareinstallations- und Bedienungsanleitung für das Python-Roboterprodukt. Es beschreibt jedes Detail des gesamten Prozesses der Erfüllung des Roboterprojekts von Python und Raspberry Pi von Grund auf sowie einige Vorsichtsmaßnahmen. Ich hoffe, Sie können mit dem Raspberry Pi-Roboter auf Python loslegen und mit dieser Dokumentation weitere Kreationen erstellen.

Je nach den unterschiedlichen Situationen verschiedener Benutzer wird es im Prozess dieses Dokuments einige Änderungen geben. Sie können sich auf den folgenden Prozess beziehen:

![Meerjungfrau](images/mermaid.png)


## 2. Raspberry Pi Systeminstallation und Einrichtung der Entwicklungsumgebung


### 2.1 Installieren Sie ein Betriebssystem für den Raspberry Pi


#### 2.1.1 Methode A: 'Raspbian' mit 'Raspberry Pi Imager' auf die SD-Karte schreiben
"Raspberry Pi Imager" ist ein von der Raspberry Pi Organization entwickeltes Tool zum Schreiben von Bildern auf eine SD-Karte.
Es wird mit vielen Versionen geliefert, die auf verschiedenen Systemen funktionieren, und es ist ziemlich einfach zu bedienen; Sie müssen lediglich das Betriebssystem und die SD-Karte auswählen, Raspberry Pi Imager lädt die entsprechende Image-Datei für das System herunter und installiert sie auf der SD-Karte.

**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe) "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen."
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg) "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen."
	- [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb) "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen."
3. Installieren Sie den `Raspberry Pi Imager`
4. Schreiben Sie das Betriebssystem für Raspberry Pi auf die SD-Karte mit `Raspberry Pi Imager` `Raspbian Full - A Port of Debian with Desktop and Recommended Application`
5. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/), suchen Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem und laden Sie ihn herunter. oder klicken Sie auf die obigen Links für das entsprechende System, um es direkt herunterzuladen und zu installieren.

  ![imagerDownload](images/imagerDownload.png)

- Legen Sie die SD-Karte in den Kartenleser ein, verbinden Sie den Kartenleser und Ihren Computer.

- Führen Sie den `Raspberry Pi Imager` aus, wählen Sie `CHOOSE OS` -> `Raspbian(other)` -> `Raspbian Full - A Port of Debian with desktop and Recommended applications`.

- Klicken Sie auf "SD-KARTE AUSWÄHLEN", damit die SD-Karte das "Raspbian Full" schreibt. Bitte beachten Sie, dass beim Schreiben des Bildes automatisch alle Dateien auf der SD-Karte gelöscht werden, falls vorhanden.

- Klicken Sie auf `WRITE`, warten Sie auf das Schreiben. Der `Raspberry Pi Imager` muss während des Vorgangs die `Raspbian`-Image-Datei herunterladen.
Sie können die Datei nach dem Schritt in **2.1.2** herunterladen.

  ![imagerUse](images/imagerUse.png)

- Entfernen Sie nicht die angeschlossene SD-Karte, wenn der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.
Andernfalls, wenn Sie die Karte entfernen, in den Raspberry Pi einsetzen und booten, kann die WLAN-Konfiguration ohne Peripheriegeräte im folgenden Prozess fehlschlagen.


#### 2.1.2 Methode B: Laden Sie die Image-Datei `Raspbian` herunter und schreiben Sie sie manuell auf die SD-Karte
Da die Image-Datei mit dem `Raspberry Pi Imager` in **2.1.1** heruntergeladen wird, kann es aufgrund eines langsamen Netzwerks an manchen Stellen lange dauern.
Sie können dann die Image-Datei `Raspbian` manuell herunterladen und mit dem `Raspberry Pi Imager` auf die SD-Karte schreiben.

**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe) "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen."
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg) "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen."
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb) "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen."
3. Installieren Sie den `Raspberry Pi Imager`
4. Laden Sie die Bilddatei `Raspbian` . herunter
    - Torrent-Datei: [Raspbian - Raspbian Buster mit Desktop und empfohlener Software](https://downloads.raspberrypi.org/raspbian_full_latest.torrent "Link zum Download der Torrent-Datei für das Bild")
    - Zip-Datei: [Raspbian - Raspbian Buster mit Desktop und empfohlener Software](https://downloads.raspberrypi.org/raspbian_full_latest "Link zum Download der Zip-Datei für das Bild")
5. Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
6. Schreiben Sie die auf die SD-Karte heruntergeladene Bilddatei `Raspbian` mit `Raspberry Pi Imager`
7. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website], suchen und laden Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem herunter oder klicken Sie auf die obigen Links, um das entsprechende System direkt herunterzuladen und Installieren.

  ![imagerDownload](images/imagerDownload.png)

- Wählen Sie auf der Raspberry Pi-Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/ ) über `Downloads` -> `Raspbian` -> `Raspbian Buster mit Desktop und empfohlener Software` und Klicken Sie auf die Torrent- oder Zip-Datei, um sie herunterzuladen.
Entpacken Sie die Datei nach dem Download, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
Andernfalls öffnet `Raspberry Pi Imager` die `.img`-Datei möglicherweise nicht.
Es wird empfohlen, die Datei `.img` im Stammverzeichnis der Festplatte `C:\` oder `D:\` zu speichern, **aber `.img` nicht auf der SD-Karte zu speichern**.

  ![RPiDownload](images/RPiDownload.png)

- Legen Sie die SD-Karte in den Kartenleser ein, verbinden Sie den Kartenleser und Ihren Computer.

- Führen Sie den `Raspberry Pi Imager` aus, wählen Sie `CHOOSE OS` und dann `Use custom`, um die extrahierte `.img` zu finden, klicken Sie auf `Open`.

- Wählen Sie "SD-KARTE AUSWÄHLEN" für die SD-Karte, um das "Raspbian" zu schreiben. Bitte beachten Sie, dass beim Schreiben von Bildern automatisch alle Dateien auf der SD-Karte gelöscht werden, falls vorhanden.

- Klicken Sie auf `WRITE`, warten Sie auf das Schreiben.

  ![imagerUse](images/imagerUse.png)

- Entfernen Sie nicht die angeschlossene SD-Karte, wenn der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.
Andernfalls, wenn Sie die Karte entfernen, in den Raspberry Pi stecken und hochfahren, kann die WLAN-Konfiguration ohne Peripheriegeräte im folgenden Prozess fehlschlagen.


#### 2.1.3 Methode C: Laden Sie die von uns bereitgestellte Imagedatei manuell herunter und schreiben Sie sie auf die SD-Karte (nicht empfohlen)
Die in **2.1.1** und **2.1.2** heruntergeladene Raspbian-Image-Datei ist die offizielle Quelle mit vorinstallierter Software.
Um den Roboter zu bedienen, benötigen Sie möglicherweise viele abhängige Bibliotheken.
Obwohl wir das einfache Skript für die Installation bereitstellen (siehe Details später), kann es während der Installation zu Fehlern kommen, wenn die Bibliothek nicht die neueste Version ist.
Daher kann es trotz der Bereitstellung des Herunterladens der Raspbian-Image-Datei vorkommen, dass unsere Image-Datei und die abhängigen Bibliotheken nicht die aktuellsten Versionen sind.
Bitte nur verwenden, wenn Sie auf die schwierigste Situation stoßen.

**Schritt-für-Schritt-Übersicht**

1. Bereiten Sie eine SD-Karte (16 GB oder größer) und einen SD-Kartenleser vor
2. Laden Sie den `Raspberry Pi Imager` von der offiziellen Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/) herunter.
    - [Raspberry Pi Imager für Windows](https://downloads.raspberrypi.org/imager/imager.exe "Klicken Sie hier, um Raspberry Pi Imager für Windows herunterzuladen")
    - [Raspberry Pi Imager für macOS](https://downloads.raspberrypi.org/imager/imager.dmg "Klicken Sie hier, um Raspberry Pi Imager für macOS herunterzuladen")
    - [Raspberry Pi Imager für Ubuntu](https://downloads.raspberrypi.org/imager/imager_amd64.deb "Klicken Sie hier, um Raspberry Pi Imager für Ubuntu herunterzuladen")
3. Installieren Sie den `Raspberry Pi Imager`
4. Laden Sie die Bilddatei `Adeept_PiCar-B` . herunter
    - [Bilddatei für den Adeept_PiCar-B Roboter](https://www.adeept.com/learn/detail-33.html)
5. Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte `.img`-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
6. Schreiben Sie die auf die SD-Karte heruntergeladene Bilddatei `Raspbian` mit `Raspberry Pi Imager`
7. Lassen Sie die SD-Karte angeschlossen, nachdem der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.

**Detaillierte Schritte:**

- Öffnen Sie einen Webbrowser auf Ihrem Computer, gehen Sie zur Raspberry Pi-Website [Offizielle Raspberry Pi-Website] (https://www.raspberrypi.org/downloads/), suchen Sie den "Raspberry Pi Imager" für Ihr Computer-Betriebssystem und laden Sie ihn herunter. oder klicken Sie auf die obigen Links für das entsprechende System, um es direkt herunterzuladen und zu installieren.

  ![imagerDownload](images/imagerDownload.png)
- Rufen Sie unsere [offizielle Website] auf, suchen Sie die Bilddatei [Bilddatei für den Adeept_PiCar-B-Roboter] (https://www.adeept.com/learn/detail-33.html) und laden Sie sie herunter.

- Entpacken Sie die Datei, beachten Sie, dass der Pfad für die extrahierte .img-Datei in Englisch sein sollte, keine Sonderzeichen erlaubt.
Andernfalls öffnet Raspberry Pi Imager die .img-Datei möglicherweise nicht.
Es wird empfohlen, die .img-Datei im Stammverzeichnis des Datenträgers C:\ oder D:\ zu speichern, aber .img nicht auf der SD-Karte zu speichern.

- Legen Sie die SD-Karte in den Kartenleser ein, verbinden Sie den Kartenleser und Ihren Computer.

- Führen Sie den `Raspberry Pi Imager` aus, wählen Sie `CHOOSE OS` und dann `Use custom`, um die extrahierte `.img` zu finden, klicken Sie auf `Open`.

- Wählen Sie "SD-KARTE AUSWÄHLEN" für die SD-Karte, um das "Raspbian" zu schreiben. Bitte beachten Sie, dass beim Schreiben von Bildern automatisch alle Dateien auf der SD-Karte gelöscht werden, falls vorhanden.
- Klicken Sie auf `WRITE`, warten Sie auf das Schreiben.

  ![imagerUse](images/imagerUse.png)

- Entfernen Sie nicht die angeschlossene SD-Karte, wenn der Schreibvorgang abgeschlossen ist. Wir verwenden sie später zum Konfigurieren der SSH- und WLAN-Verbindung.
Andernfalls, wenn Sie die Karte entfernen, in den Raspberry Pi stecken und hochfahren, kann die WLAN-Konfiguration ohne Peripheriegeräte im folgenden Prozess fehlschlagen.


### 2.2 SSH-Server des Raspberry Pi aktivieren

- Per SSH (Secure Shell) Server können Sie die Kommandozeile des Raspberry Pi remote auf einem anderen Gerät verwenden.
Im späteren Betrieb und bei der Nutzung des Raspberry Pi müssen Sie keine Maus, Tastatur oder Monitor daran anschließen, sondern einfach an einem Computer im selben LAN steuern.
- Seit der Version vom November 2016 ist bei Raspbian der SSH-Server standardmäßig deaktiviert.
Sie müssen es manuell aktivieren.
- Die Methode zum Aktivieren von SSH in dieser Dokumentation finden Sie auf der offiziellen Raspberry Pi-Website [SSH(Secure Shell)](https://www.raspberrypi.org/documentation/remote-access/ssh/)


#### 2.2.1 Methode A: SSH mit Peripheriegeräten aktivieren

- Wenn Sie (2.1.3, um die von uns bereitgestellte Image-Datei manuell herunterzuladen und auf die SD-Karte zu schreiben) verwenden, um das Betriebssystem des Raspberry Pi auf die SD-Karte zu schreiben, müssen Sie diesen Abschnitt nicht lesen, um SSH zu öffnen , da der SSH-Dienst im Image bereits aktiviert ist.
- Wenn Sie eine Maus, Tastatur oder einen Monitor an den Raspberry Pi angeschlossen haben, führen Sie diese Schritte aus, um SSH zu aktivieren.

    1. Entfernen Sie die SD-Karte aus dem Computer, stecken Sie sie in den Raspberry Pi ein, schließen Sie eine Maus, Tastatur und einen Monitor an den Raspberry Pi an, booten Sie ihn.
	2. Gehen Sie zum Menü "Einstellungen" und wählen Sie "Raspberry Pi-Konfiguration".
    3. Gehen Sie zur Option `Schnittstellen`.
    4. Wählen Sie `Aktivieren` neben `SSH`.
    5. Klicken Sie auf `OK`.
    
    ![configSSH](images/configSSH.png)


#### 2.2.2 Methode A: SSH ohne Peripheriegeräte aktivieren

- Wenn Sie keinen Monitor an den Raspberry Pi angeschlossen haben, führen Sie diese Schritte aus, um SSH zu aktivieren.

    1. Entfernen Sie die SD-Karte nicht, nachdem `Raspberry Pi Imager` die Image-Datei geschrieben hat.

    2. Erstellen Sie eine Datei namens `ssh` in einem beliebigen Verzeichnis ohne Erweiterungsnamen.
Sie können eine `ssh.txt` erstellen und die `.txt` löschen (stellen Sie sicher, dass unter Ordneroptionen das Kontrollkästchen Erweiterungen bei bekannten Dateitypen ausblenden deaktiviert ist.
Dann haben Sie eine `ssh`-Datei ohne Erweiterungsnamen.

    3. Kopieren Sie die `ssh`-Datei und fügen Sie sie in das Stammverzeichnis der SD-Karte ein.
Der Raspberry Pi sucht beim Booten automatisch nach der `ssh`-Datei und aktiviert SSH, wenn die Datei gefunden wird.
Sie müssen nur einmal kopieren, da der Raspberry Pi dann bei jedem Booten automatisch SSH aktiviert.

    4. Entfernen Sie die SD-Karte nicht, wenn Sie WLAN konfigurieren müssen.


### 2.3 WLAN auf Raspberry Pi konfigurieren

Es gibt viele Möglichkeiten, WLAN für Raspberry Pi zu verbinden.
In dieser Dokumentation werden zwei Methoden bereitgestellt; Weitere Informationen finden Sie auf der offiziellen Raspberry Pi-Website: [Wireless-Konnektivität](https://www.raspberrypi.org/documentation/configuration/wireless/README.md).


#### 2.3.1 Methode A: WLAN-Verbindung mit Peripheriegeräten

- Wenn Sie eine Maus, Tastatur oder einen Monitor an den Raspberry Pi angeschlossen haben, führen Sie diese Schritte aus, um WLAN zu konfigurieren.

    1. Entfernen Sie die SD-Karte aus dem Computer, stecken Sie sie in den Raspberry Pi ein, schließen Sie eine Maus, Tastatur und einen Monitor an den Raspberry Pi an, booten Sie ihn.
    2. Wählen Sie das WLAN-Symbol in der oberen rechten Ecke des Monitors aus, suchen Sie das zu verbindende WLAN und wählen Sie es aus.
    3. Geben Sie das Passwort für das WLAN ein, verbinden Sie sich.
    4. Nach erfolgreicher Verbindung wird das WLAN gespeichert und der Raspberry Pi verbindet sich automatisch für den nächsten Start, sodass Sie nicht jedes Mal Peripheriegeräte anschließen müssen.


#### 2.3.2 Methode A: WLAN-Verbindung ohne Peripheriegeräte

- Wenn Sie keinen Monitor mit dem Raspberry Pi verbunden haben, gehen Sie wie folgt vor, um WLAN zu konfigurieren.
- Diese Methode basiert auf der [offiziellen Dokumentation](https://www.raspberrypi.org/documentation/configuration/wireless/headless.md)

    1. Entfernen Sie die SD-Karte nicht, nachdem `Raspberry Pi Imager` die Image-Datei geschrieben hat.
(Diese Methode funktioniert für den Fall, dass die Raspbian-Image-Datei gerade auf die SD-Karte geschrieben wurde; wenn Sie die SD-Karte bereits in den Raspberry Pi gesteckt und nach dem Schreiben der Image-Datei neu gestartet haben, kann die Konfiguration fehlschlagen. )

    2. Erstellen Sie irgendwo auf Ihrem Computer eine Datei namens `wpa_supplicant.conf`.
    
    3. Öffnen Sie die mit Textbook erstellte Datei `wpa_supplicant.conf` und geben Sie den folgenden Code ein:

    ```
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    country=Geben Sie hier den Ländercode ein
    Netzwerk={
     ssid="Name Ihres WLANs"
     psk="Passwort für Ihr WLAN"
    }
    ```

    4. Geben Sie Ihre eigenen Informationen für `Ländercode hier einfügen`, `Name Ihres WLANs` und `Passwort für Ihr WLAN` ein.
Achten Sie auf die Groß-/Kleinschreibung. Siehe folgendes Beispiel:

    ```
    ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
    update_config=1
    Land=USA
    Netzwerk={
     ssid="MeinName"
     psk="12345678"
    }
    ```

    5. Speichern und beenden. Kopieren Sie die `wpa_supplicant.conf` in das Stammverzeichnis der SD-Karte.

    6. Wenn Sie die Datei `ssh` bereits wie in **2.2** beschrieben auf die SD-Karte kopiert haben, sind sowohl die WLAN- als auch die SSH-Einstellungen ohne Peripheriegeräte durchgeführt.
Sie können die SD-Karte entfernen, in den Raspberry Pi einlegen und hochfahren.
    
    7. Weitere Informationen zur Datei `wpa_supplicant.conf` finden Sie in der offiziellen Dokumentation [WIRELESS-CLI](https://www.raspberrypi.org/documentation/configuration/wireless/wireless-cli.md)


## 3. Melden Sie sich beim Raspberry Pi an und installieren Sie die App

- Wenn Sie die Schritte in **2.2.1** und **2.3.1** für die SSH- und WiFi-Konfiguration befolgt haben, können Sie jetzt die Peripheriegeräte entfernen und später SSH verwenden, um den Raspberry Pi fernzusteuern.

- Wenn Sie die Schritte in **2.2.2** und **2.3.2** befolgt haben, können Sie nun die SD-Karte in den Raspberry Pi einlegen und diesen hochfahren.
Der Raspberry Pi bootet automatisch und verbindet sich beim Einschalten mit WLAN, ohne dass Peripheriegeräte erforderlich sind.

- Einige der unten aufgeführten Schritte basieren auf der offiziellen Raspberry Pi-Dokumentation [SSH](https://www.raspberrypi.org/documentation/remote-access/ssh/).

- Informationen zur Stromversorgung des Raspberry Pi finden Sie in der offiziellen Dokumentation [Stromversorgung](https://www.raspberrypi.org/documentation/hardware/raspberrypi/power/README.md).

- Das Robot HAT Board des Adeept Raspberry Pi Robot kann den Raspberry Pi über den GPIO-Port mit Strom versorgen.
Da die Installation der Software auf dem Raspberry Pi jedoch sehr lange dauern kann, wird von einer Lieferung mit dem Akku abgeraten
s während dieses Vorgangs.
Sie können die Installation des Robot HAT-Boards oder der Kamera während der Softwareinstallation überspringen; Sie müssen jedoch sicherstellen, dass die Treiberplatine und die Kamera für den Raspberry Pi bereit sind, die installierte Software auszuführen, da sonst ein Programmfehler auftritt.


### 3.1 Bei Raspberry Pi anmelden (Windows 10)

- Für Windows 10 ist SSH in den Versionen nach Oktober 2018 eingebaut, Sie benötigen also keine Software von Drittanbietern.

- Bei niedrigeren Versionen des Windows-Betriebssystems ist SSH nicht integriert, und Sie können sich in der offiziellen Dokumentation [SSH using Windows] (https://www.raspberrypi.org/documentation/remote-access/) beim Raspberry Pi anmelden. ssh/windows.md).

- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen.
Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.

- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse] (https://www.raspberrypi.org/documentation/remote-access/ip-address.md)

- Drücken Sie die Tasten <kbd>win</kbd>+<kbd>R</kbd>, geben Sie `cmd` ein und drücken Sie <kbd>Enter</kbd>.

- Der Standardnutzer ist "pi" und das Passwort ist "raspberry".

- Geben Sie `ssh pi@<IP>` in die Befehlszeile ein, ersetzen Sie das `<IP>` durch die IP-Adresse Ihres Raspberry Pi, wie unten gezeigt:

    >ssh pi@192.168.3.161

- Drücken Sie die Eingabetaste und es erscheint eine Eingabeaufforderung: `Sind Sie sicher, dass Sie die Verbindung fortsetzen möchten (ja/nein)?`

- Geben Sie `yes` ein, drücken Sie die Eingabetaste und es wird `pi@192.168.3.161's password:` angezeigt, geben Sie das anfängliche Passwort des Raspberry Pi ein, `raspberry` (achten Sie auf die Groß-/Kleinschreibung).
Während der Eingabe ändert sich der Bildschirm nicht, aber das bedeutet nicht, dass Sie die Informationen nicht eingeben.
Drücken Sie die <kbd>Eingabetaste</kbd>, nachdem Sie mit der Eingabe fertig sind.

- Jetzt haben Sie sich also beim Raspberry Pi angemeldet.

![winSSH](images/winSSH.png)


### 3.2 Beim Raspberry Pi anmelden (Linux oder Mac OS)

- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen.
Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.

- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse] (https://www.raspberrypi.org/documentation/remote-access/ip-address.md "IP-Adresse")

- Öffnen Sie das Terminalfenster (oder die Befehlszeile)

- Der Standardnutzer ist "pi" und das Passwort ist "raspberry".

- Geben Sie `ssh pi@<IP>` in die Befehlszeile ein, ersetzen Sie `<IP>` durch die IP-Adresse Ihres Raspberry Pi wie unten gezeigt:

    >ssh pi@192.168.3.161

- Drücken Sie die Eingabetaste und es erscheint eine Eingabeaufforderung: `Sind Sie sicher, dass Sie die Verbindung fortsetzen möchten (ja/nein)?`

- Geben Sie `yes` ein, drücken Sie die Eingabetaste und es wird `pi@192.168.3.161's password:` angezeigt, geben Sie das anfängliche Passwort des Raspberry Pi ein, `raspberry` (achten Sie auf die Groß-/Kleinschreibung).
Während der Eingabe ändert sich der Bildschirm nicht, aber das bedeutet nicht, dass Sie die Informationen nicht eingeben.
Drücken Sie die <kbd>Eingabetaste</kbd>, nachdem Sie mit der Eingabe fertig sind.

- Jetzt haben Sie sich also beim Raspberry Pi angemeldet.


### 3.3 Bei Raspberry Pi anmelden (Windows 8 oder Vorgängerversion)

- Für niedrigere Versionen des Windows-Betriebssystems ist SSH nicht integriert, und Sie können sich beim Raspberry Pi anmelden, indem Sie sich auf die offizielle Dokumentation Raspberry Pi [SSH using Windows] (https://www.raspberrypi.org/documentation/remote- access/ssh/windows.md "SSH unter Windows").
- Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen.
Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.
- Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse] (https://www.raspberrypi.org/documentation/remote-access/ip-address.md "IP-Adresse")
- Möglicherweise müssen Sie die `PuTTY`-Version für Ihr Betriebssystem herunterladen und sich mit dem Tool bei Raspberry Pi anmelden. [Klicken Sie hier, um PuTTY herunterzuladen](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html "Klicken Sie hier, um PuTTY herunterzuladen")
- Führen Sie `PuTTY` aus, geben Sie die IP-Adresse des Raspberry Pi als `Host Name` ein und klicken Sie auf <kbd>Öffnen</kbd>.
- Wenn die Meldung `Netzwerkfehler: Zeitüberschreitung der Verbindung` erscheint, haben Sie möglicherweise eine falsche IP-Adresse eingegeben.
- Wenn die Verbindung funktioniert, sehen Sie die unten angezeigte Sicherheitswarnung.
Sie können es getrost ignorieren und auf die Schaltfläche "Ja" klicken.
Sie sehen diese Warnung nur, wenn sich PuTTY zum ersten Mal mit einem Raspberry Pi verbindet, den es noch nie zuvor gesehen hat.
- Sie sehen nun die übliche Anmeldeaufforderung. Melden Sie sich mit demselben Benutzernamen und Passwort an, das Sie auf dem Pi selbst verwenden würden.
Der Standard-Login für Raspbian ist `pi` mit dem Passwort `raspberry`.
- Sie sollten jetzt die Raspberry Pi-Eingabeaufforderung haben, die identisch mit dem auf dem Raspberry Pi selbst gefundenen.

![Putty](images/putty.png)


### 3.4 Download-Programm des Raspberry Pi-Roboters

- Der Code für das Roboterprodukt wurde auf [GitHub](https://github.com/adeept/adeept_picar-b.git) hochgeladen. Möglicherweise müssen Sie ihn auf Ihren Raspberry Pi herunterladen und die entsprechenden abhängigen Bibliotheken installieren, um den Programm.

- Im vorherigen Abschnitt haben Sie sich beim Raspberry Pi angemeldet und geben hier den folgenden Befehl im Terminalfenster ein:

    >sudo git clone https://github.com/adeept/adeept_picar-b.git
	
	Oder meine Version, mit den Deutschen Dokumenten
	
    >sudo git clone https://github.com/dwhr-pi/adeept_picar-b.git

- Drücken Sie <kbd>Enter</kbd>, um das Programm des Roboters von GitHub herunterzuladen. Es kann einige Zeit dauern, bitte warten Sie, bis es fertig ist.


### 3.5 Entsprechende abhängige Bibliotheken installieren

- Befolgen Sie die nachstehenden Schritte, um die Bibliotheken zu installieren, wenn Sie die Image-Datei basierend auf **2.1.1 Schreiben Sie 'Raspbian' auf die SD-Karte mit `Raspberry Pi Imager`** und **2.1.2 Laden Sie das Image-Datei `Raspbian` und schreibe sie manuell auf die SD-Karte**.

- Sie sollten jedoch **diesen Abschnitt überspringen**, wenn Sie die Bilddatei auf Grundlage von **2.1.3 auf die SD-Karte geschrieben haben. Laden Sie die von uns bereitgestellte Bilddatei manuell herunter und schreiben Sie sie auf die SD-Karte**; siehe **2.4.5** für die Konfiguration des Autostart-Programms.

- Hier wird ein Skript bereitgestellt, um alle benötigten abhängigen Bibliotheken zu installieren und den Start der Kamera und anderer Autostart-Programme zu konfigurieren.

- Geben Sie den folgenden Code in das Terminalfenster ein, um die abhängigen Bibliotheken für das Skript `setup.py` auszuführen:

    > sudo python3 adeept_picar-b/setup.py

- Drücken Sie <kbd>Enter</kbd> und das Skript wird automatisch ausgeführt.
Dies kann je nach Netzwerkstatus Minuten oder Stunden dauern.
Bitte warten Sie, bis es fertig ist.

- Nach Abschluss der Installation werden die folgenden Eingabeaufforderungen angezeigt:

    >Das Programm im Raspberry Pi wurde installiert, getrennt und neu gestartet.
    >Sie können jetzt den Raspberry Pi ausschalten, um die Kamera und die Treiberplatine (Motor HAT) zu installieren.
Nach dem erneuten Einschalten führt der Raspberry Pi automatisch das Programm aus, um das Servo-Port-Signal zu setzen, um die Servos in die mittlere Position zu drehen, was für die mechanische Montage praktisch ist.

- Wenn die Installation abgeschlossen ist, trennt der Raspberry Pi automatisch SSH und startet neu.
Wenn Sie puTTy verwendet haben, um den Raspberry Pi zu verbinden, kann es zu einer Fehlermeldung wie `Netzwerkfehler: Software verursachte Verbindungsabbruch` kommen.
Sie können es einfach ignorieren und schließen.


### 3.6 Führen Sie das Programm des Raspberry Pi-Roboters aus

- Raspberry Pi führt bei jedem Neustart automatisch das Programm für den Roboter aus. Dies ist der Teil `[RobotName]/server/webServer.py` (ersetzen Sie `[RobotName]` durch den Namen des Ordners für das Programm Ihres Roboterprodukts).
Wenn die Raspberry Pi-Kamera oder Motor Hat jedoch nicht angeschlossen ist, kann `webServer.py` nicht richtig laufen. Dies ist sinnvoll, da das Programm des Roboters die Kamera und den Chipsatz PCA9685 benötigt. Motor Hat steuert Servo mit PCA9685; der Raspberry Pi kommuniziert mit PCA9685 über I2C; Wenn Robot HAT also nicht mit Raspberry Pi verbunden ist, tritt bei der Instanziierung abhängiger Bibliotheken für PCA9685 aufgrund eines Kommunikationsfehlers ein Programmfehler auf.

- Raspberry Pi ausschalten, Kameramodul und Motor Hat anschließen, neu starten und nun kann `webServer.py` laufen.

- Im Allgemeinen müssen Sie `webServer.py` nicht manuell ausführen, da es bei jedem Start automatisch von Raspberry Pi ausgeführt wird.

- Öffnen Sie einen Webbrowser (zum Beispiel Google Chrome), geben Sie in der Adressleiste die IP-Adresse des Raspberry Pi ein, fügen Sie wie unten gezeigt `:5000` am Ende hinzu und drücken Sie <kbd>Enter</kbd>, um umzuleiten zur Webseite des Raspberry Pi:

    >http://192.168.3.161:5000/

- Wenn die Seite nicht aufgerufen werden kann, melden Sie sich über SSH am Raspberry Pi an, geben Sie den folgenden Befehl ein, um die automatische Ausführung des Programms beim Booten zu beenden, um Ressourcen freizugeben, oder Probleme wie ein Fehler bei der Kamerainitialisierung oder belegte Ports.

    > sudo killall python3

- Geben Sie den folgenden Befehl ein, um `webServer.py` auszuführen:

    >sudo python3 adeept_picar-b/server/webServer.py  

- Überprüfen Sie, ob ein Fehler vorliegt, und beheben Sie ihn gemäß den Anweisungen im Abschnitt Fragen und Antworten unten.


## 4 Raspberry Pi Strukturmontage und Vorsichtsmaßnahmen


### 4.1 Dokumentation zur Strukturmontage

- [Dokumentation zur Strukturmontage](https://www.adeept.com/learn "Dokumentation zur Strukturmontage")
Vor dem Zusammenbau
Vor der Installation des Roboters "müssen Sie die Software installieren (siehe zweite Hälfte des Dokuments), um den Roboter auf dem Raspberry Pi zu steuern".
Denn das Servo muss während des Robotermontageprozesses in die ursprüngliche Position zurückgebracht werden, was die Unterstützung eines Raspberry Pi mit normaler Software erfordert.

`Wie man ein Servo in die ursprüngliche Position zurückkehrt`

Verbinden Sie das Servo mit dem Raspberry Pi, der eingeschaltet ist.
Wenn die Verbindung hergestellt ist, läuft das Servo sofort und kehrt in kürzester Zeit automatisch in die Ausgangsposition zurück.
Dann können Sie den Kipphebel in einem bestimmten Winkel am Servo montieren.

automatisch zurückkehren ➔ Kipphebel einbauen

![Servo](images/9.jpg)

`(Der Servotyp und der Einbauwinkel des Kipphebels dienen nur als Referenz. Bitte beziehen Sie sich auf das tatsächliche Produkt und das Montageteil.)`

Ob das Servo in die ursprüngliche Position zurückgekehrt ist

Ob das Servo in die Ausgangsposition zurückgekehrt ist, können Sie durch Ziehen am Kipphebel prüfen (nicht zu fest anstrengen, um eine Beschädigung des Servos zu vermeiden).
Das automatisch zurückgekehrte Servo kann nicht gezogen werden.


![Servo](images/10.jpg "Servo")

Wenn Ihr Servo nicht automatisch in die ursprüngliche Position zurückkehrt, können Sie die Datei server.py manuell ausführen und dann versuchen, das Servo anzuschließen.


- Vorbereitungen vor der Montage

1. Verbinden Sie die Raspberry Pi Kamera und das Band.
![Servo](images/11.jpg)

2. Verbinden Sie das Adeept Ultraschallmodul mit 4-poligen Drähten.
![Servo](images/12.jpg)

Die Anschlussdiagramme der verbleibenden Module und Drähte sind wie folgt:

![Servo](images/13.jpg)

![Servo](images/14.jpg)

![Servo](images/15.jpg)

3. Schrauben Sie die M3*3-Feststellschraube in das Kegelrad (2 Sätze).
![Servo](images/16.jpg)

4. Schrauben Sie die M4*4-Verriegelungsschraube in die S12D4-Kupplung (2 Sätze).
![Servo](images/17.jpg)


- Montage von Autolicht und Batteriehalter

1. Befestigen Sie zwei M3 * 12 Kupfer-Abstandshalter auf A01.
![Servo](images/18.jpg)

![Servo](images/19.jpg)

2. Fixieren Sie A06 auf A01.
![Servo](images/20.jpg)

![Servo](images/21.jpg)

3. Fixieren Sie M2*6 Kupferabstandshalter auf A01.
![Servo](images/22.jpg)

![Servo](images/23.jpg)

4. Befestigen Sie eine 3-CH WS2812 RGB LED-A auf M2*6 Kupferabstandshalter.

![Servo](images/24.jpg)

![Servo](images/25.jpg)

5. Befolgen Sie Schritt 3 und 4 und befestigen Sie eine weitere 3-CH WS2812 RGB LED-A an A01.

![Servo](images/26.jpg)

6. Befestigen Sie den 18650x2 Batteriehalter auf A01.

![Servo](images/27.jpg)

![Servo](images/28.jpg)

7. Befestigen Sie auf beiden Seiten des A02 jeweils eine 3-CH WS2812 RGB LED-A und eine 3-CH WS2812 RGB LED-B.

![Servo](images/29.jpg)

![Servo](images/30.jpg)

8. Fixieren Sie A02 auf A01.
![Servo](images/31.jpg)

![Servo](images/32.jpg)

![Servo](images/33.jpg)


- Hinterradmontage

1. Befestigen Sie das Kegelrad am Motor.

![Servo](images/34.jpg)

2. Motor an A06 befestigen.

![Servo](images/35.jpg)

![Servo](images/36.jpg)

3. Befestigen Sie vier M3*30 Kupferabstandshalter auf A01.

![Servo](images/37.jpg)

![Servo](images/38.jpg)

4. Befestigen Sie dann den A04 am M3*30 Copper Standoff.

![Servo](images/39.jpg)

![Servo](images/40.jpg)

5. Nehmen Sie eine S12D4-Kupplung und befestigen Sie sie an der D3.9L120-Achse.

![Servo](images/41.jpg)

6. Führen Sie dann die D3.9L120-Achse durch die A10.

![Servo](images/42.jpg)

7. Nehmen Sie eine andere S12D4-Kupplung und befestigen Sie sie an der D3.9L120-Achse.

![Servo](images/43.jpg)

![Servo](images/44.jpg)

8. Befestigen Sie den Reifen an der S12D4-Kupplung.

![Servo](images/45.jpg)

![Servo](images/46.jpg)

9. Befestigen Sie auf die gleiche Weise eine weitere S12D4-Kupplung an einem Reifen.

![Servo](images/47.jpg)

10. Befestigen Sie das Kegelrad an der Achse D3.9L120.

![Servo](images/48.jpg)


- Vorderradmontage

1. Befestigen Sie das 3-CH-Line-Tracking-Modul auf A03.

![Servo](images/49.jpg)

![Servo](images/50.jpg)

2. Befestigen Sie zwei 3 * 12 Kupfer-Abstandshalter auf A03.

![Servo](images/51.jpg)
![Servo](images/52.jpg)

3. Kalibrieren Sie die Servos.
![Servo](images/53.jpg)

Stellen Sie nun das Servo ein.
Dieser Schritt besteht darin, die Servowelle in der Mitte zu machen, damit die mit dem Servo verbundene Komponente nach Bedarf in einem bestimmten Umfang bewegt werden kann.

![Servo](images/54.jpg)

![Servo](images/55.jpg)

4. Nehmen Sie zwei Servos und fixieren Sie diese jeweils mit A09.

![Servo](images/56.jpg)

5. Befestigen Sie das zusammengebaute Servo am M3*12 Copper Standoff am A03.

![Servo](images/57.jpg)

![Servo](images/58.jpg)

6. Befestigen Sie vier M3*30 Kupfer-Abstandshalter auf A03.

![Servo](images/59.jpg)

![Servo](images/60.jpg)

7. Verbinden Sie den Kipphebel eines Servos mit A07.

![Servo](images/61.jpg)

8. Montage mit zwei Vorderrädern.

![Servo](images/62.jpg)

9. Befestigen Sie den Kipphebel des A07 am Servo des A03.

![Servo](images/63.jpg)

![Servo](images/64.jpg)

10. Befestigen Sie den M3*30 Kupferabstandshalter an A01 und A03.

![Servo](images/65.jpg)

![Servo](images/66.jpg)

11. Reparieren Sie das Adeept RGB LED-Modul auf A05.

![Servo](images/67.jpg)

![Servo](images/68.jpg)

12. Reparieren Sie das Adeept RGB LED-Modul und A05 auf A01.

![Servo](images/69.jpg)

![Servo](images/70.jpg)

![Servo](images/71.jpg)


- Frontteilmontage

1. Fixieren Sie die Raspberry Pi-Kamera auf A18.

![Servo](images/72.jpg)

2. Befestigen Sie das Adeept Ultraschallmodul am A18.

![Servo](images/73.jpg)

3. Nehmen Sie ein Servo und fixieren Sie es mit A15.

![Servo](images/74.jpg)

4. Befestigen Sie drei M3 * 30 Kupferabstandshalter an A17.

![Servo](images/75.jpg)

5. Fügen Sie A16 in A17 ein.

![Servo](images/76.jpg)

6. Fügen Sie A15 in A17 ein.

![Servo](images/77.jpg)

7. Befestigen Sie den A18 am M3*30 Kupferabstandshalter auf dem A17.

![Servo](images/78.jpg)

8. Installieren Sie einen Kipphebel am Servo.

![Servo](images/79.jpg)

9. A13 mit Servo fixieren.

![Servo](images/80.jpg)

10. Wählen Sie ein 'cross' Kipphebel und am A12 befestigen.

![Servo](images/81.jpg)

11. Befestigen Sie dann den Kipphebel am mit A09 montierten Servo.

![Servo](images/82.jpg)

12. M3*18 Schraube auf A14 befestigen.

![Servo](images/83.jpg)

13. Fügen Sie A13, A14 in A12 ein.

![Servo](images/84.jpg)

14. Dann A3*12 Schraube verwenden, um A13 und A14 an A12 zu befestigen.

![Servo](images/85.jpg)

15. Befestigen Sie die im vorherigen Schritt abgeschlossene Baugruppe am M3*12-Kupferabstandshalter am A1.

![Servo](images/86.jpg)

![Servo](images/87.jpg)

![Servo](images/88.jpg)

![Servo](images/89.jpg)

![Servo](images/90.jpg)

Drehen Sie schließlich den oberen Teil des Servos zurück in die ursprüngliche Position.

![Servo](images/91.jpg)


- Raspberry Pi-Baugruppe

1. Fixieren Sie M2,5 * 10 + 6 Kupfer-Abstandshalter und M2.5 * 14 Kupfer-Abstandshalter auf Raspberry Pi.

![Servo](images/92.jpg)

2. Verbinden Sie das andere Ende des Raspberry P1 Camera Ribbon über Adeept Motor HAT mit dem Raspberry Pi und befestigen Sie den Adeept Motor HAT am Raspberry Pi.

![Servo](images/93.jpg)

3. Fixieren Sie den Raspberry Pi auf dem A02.

![Servo](images/94.jpg)

![Servo](images/95.jpg)

4. Wenn Sie das Voice-Modul verwenden müssen, müssen Sie es in den Raspberry Pi stecken.

![Servo](images/96.jpg)

![Servo](images/97.jpg)


- Batterien einlegen und entfernen

![Servo](images/98.jpg)


- Schaltungsverbindung

Verbinden Sie die Komponenten gemäß der Abbildung.
Achten Sie darauf, dass Kabel und Port übereinstimmen und nicht umgekehrt anschließen.

![Servo](images/99.jpg)

## 4.2 Tipps für den strukturellen Zusammenbau

- Da im Produkt viele Servos verwendet werden, ist die Servoinstallation für den Roboter kritisch.
Bevor Sie den Kipphebel am Servo montieren, müssen Sie das Servo an die Stromversorgung anschließen und die Servowelle in die Mittelposition drehen.
So befindet sich der am vorgesehenen Grad montierte Kipphebel in der Mittelposition.
- Im Allgemeinen führt Raspberry Pi beim Booten automatisch `webServer.py` aus.
Wenn `webServer.py` alle mit Servos verbundenen Ports steuert, um ein Signal zum Drehen in die Mittelposition zu senden.
Beim Zusammenbau des Servos können Sie es jederzeit an einen beliebigen Servoanschluss anschließen.
Nach dem Anschließen des Servos an den Port drehen sich die Zahnräder in die Mittelposition; Montieren Sie den Kipphebel am Servo, trennen Sie das Servo vom Anschluss und setzen Sie weitere Servos ein, um die Kipphebelmontage zu wiederholen (alle Servos befinden sich in der Mittelposition).
- Wenn das Servo an die Stromversorgung angeschlossen ist, versuchen Sie, den Kipphebel zu bewegen.
Wenn es nicht bewegt werden kann, zeigt es das Programm für die Servos an; andernfalls gibt es einen Fehler für das Servoprogramm.
Führen Sie die Zeile `[RobotName]/initPosServos.py` aus (ersetzen Sie `[RobotName]` durch den Ordnernamen Ihres Roboterprogramms), um das Servo in die Mittelposition zu drehen.
- Beim Booten (es kann 30-50s dauern), dauert es eine Weile, bis der Raspberry Pi PCA9685 steuert, um das Signal aller Servoports für die Mittelpositionsdrehung zu setzen.

## 4.3 Tipps zur Strombereitstellung

- Wenn Sie die Software installieren, die Struktur zusammenbauen und das Programm debuggen, können Sie den Raspberry Pi über ein USB-Kabel mit Strom versorgen.
Wenn der Raspberry Pi mit Motor HAT installiert ist, können Sie das USB-Kabel an die USB-Schnittstelle des Motor HAT anschließen.
Motor HAT versorgt den Raspberry Pi über die GPIO-Schnittstelle mit Strom.
- Der Bedarf verschiedener Himbeer-Pi an elektrischem Strom ist unterschiedlich.
Zum Beispiel benötigt der Raspberry Pi 3B mindestens 2 A Strom zum Starten und der Raspberry Pi 4 benötigt 3 A, um normal zu starten.
Sie können die Spezifikationen Ihres Netzteils überprüfen, bevor Sie das Netzteil verwenden, um den Raspberry Pi mit Strom zu versorgen.
- Wenn der Motor HAT an eine Last angeschlossen ist (z. B. an einen Motor oder mehrere Servos), müssen Sie ein Netzteil verwenden, das Hochstrom unterstützt, um an Vin am Motor HAT anzuschließen.
Sie können zwei 18650-Batterien verwenden, die Hochstrom unterstützen, um Motor HAT zu betreiben.
Unser Produkt bietet eine duale 18650-Batteriebox mit 2-Pin-Schnittstelle, die Sie direkt an Motor HAT anschließen können.
- Wenn Sie die USB-Schnittstelle am Motor HAT zur Stromversorgung verwenden, steuert der Schalter von Motor HAT nicht, ob Strom zugeführt wird, der Schalter von Motor HAT kann nur die Stromversorgung von Vin steuern.
- Verwenden Sie die USB-Schnittstelle und Vin am Motor HAT nicht gleichzeitig zur Stromversorgung.
Wenn Sie das Programm längere Zeit debuggen müssen und den Akku nicht entfernen möchten, können Sie den Schalter am Motor HAT auf OFF stellen.
Wenn Sie also ein USB-Kabel verwenden, um Motor HAT anzuschließen, wird Motor HAT über USB mit Strom versorgt.
- Wenn Ihr Roboter nach dem Start automatisch neu startet oder der Roboter die Verbindung trennt und plötzlich neu startet, wenn er sich nach dem normalen Start zu bewegen beginnt.
Dies liegt höchstwahrscheinlich daran, dass Ihr Netzteil nicht genügend Strom ausgibt.
Wenn der Roboter startet, führt er automatisch das Programm aus, um alle Servos in die neutrale Position zu bringen.
Der durch diesen Vorgang verursachte Spannungsabfall führt zum Neustart des Himbeer-Pi.
- Wir haben getestet, dass bei Verwendung einer 7,4 V-Stromversorgung der Spitzenstrom des Roboters etwa 3,75 A beträgt. Sie müssen also eine Batterie verwenden, die eine Ausgangsleistung von 4 A unterstützt.
- Sie können auch verwendeneine Power-Lithium-Batterie, um den Motor HAT mit Strom zu versorgen.
Motor HAT unterstützt die Stromversorgung, die unter 15 V liegt.
- Sie können ein USB-Kabel verwenden, um den Motor HAT mit Strom zu versorgen, wenn Sie den Kipphebel des Servos während der strukturellen Montage installieren.
Nachdem die Robotersoftware installiert ist, steuert der Raspberry Pi den Motor HAT so, dass alle Servoanschlüsse so eingestellt werden, dass das Neutralsignal nach dem Start ausgegeben wird.
Zu diesem Zeitpunkt können Sie das Servo an einen beliebigen Servoanschluss anschließen, das Servogetriebe dreht sich in die neutrale Position und dann können Sie den Kipphebel des Servos entsprechend dem angegebenen Winkel installieren.
Nachdem der Kipphebel montiert ist, kann das Servo vom Motor HAT getrennt werden.
Wenn Sie den Kipphebel des zweiten Servos installieren müssen, müssen Sie nur das zweite Servo an einen beliebigen Servoanschluss auf der Antriebsplatine anschließen.

## 5 Roboter über WEB App steuern

- Die WEB-App wurde für normale Benutzer entwickelt, um den Roboter einfacher zu steuern.
Es ist bequem, die WEB-App zu verwenden; Sie können damit den Roboter auf jedem Gerät mit einem Webbrowser drahtlos steuern (**Google Chrome wurde zum Testen verwendet**).
- Im Allgemeinen führt Raspberry Pi beim Booten automatisch `webServer.py` aus und baut einen Webserver im LAN auf.
Sie können dann jeden anderen Computer, Handy oder Tablet im selben LAN verwenden, um die Webseite zu besuchen und den Roboter zu steuern.
- So erkennen Sie, ob der Roboter `webServer.py` ausgeführt hat oder nicht:
Wenn die WS2812-LED mit dem Atemeffekt aufleuchtet, bedeutet dies, dass der Roboter gebootet hat und das Programm automatisch ausführt.
- Wenn das Programm beim Booten des Roboters nicht ausgeführt wird, versuchen Sie, den Raspberry Pi über SSH zu verbinden, führen Sie `webServer.py` manuell mit Code aus und überprüfen Sie die Fehler.
Lesen Sie die Fragen und Antworten unten oder senden Sie uns eine E-Mail, um Hilfe zu erhalten (bevor Sie `webServer.py` manuell ausführen, müssen Sie das Programm möglicherweise automatisch im Backend ausführen, um Ressourcen freizugeben.

    ```
sudo killall python3
    sudo python3 [Robotername]/server/webServer.py
    ```

- Wenn die `webServer.py` erfolgreich automatisch ausgeführt wird, öffnen Sie einen Webbrowser (hier Google Chrome), geben Sie die IP-Adresse des Raspberry Pi ein, mit `:5000` am Ende, und gehen Sie zum nächsten Schritt, Wie nachfolgend dargestellt:

    >192.168.3.157:5000

- Wenn kein Bild angezeigt wird, versuchen Sie, `webServer.py` manuell auszuführen, wie im obigen Schritt beschrieben.
- Wenn ein Bild angezeigt wird, können Sie den Roboter jetzt so steuern, dass er sich bewegt.
Sie können die Beschreibung der Tastenkombinationen 'Anweisung' unten überprüfen und den Roboter anhand seiner allgemeinen Funktionen mit der Tastatur steuern.
- Das `Video`-Fenster zeigt das von der Roboterkamera aufgenommene Bild in Echtzeit.
- Das Fenster "Move Control" dient zur Steuerung der Grundbewegungen des Roboters.
- Das Fenster "CVFL-Steuerung" dient zur Steuerung der Sichtlinienverfolgungsfunktion des Roboters.
Hier wird nur eine Übersicht zur Funktion beschrieben; Weitere Details finden Sie im Abschnitt OpenCV:

    `START`: Aktivieren oder deaktivieren Sie die visuelle Linienverfolgungsfunktion.
    `COLOR`: Umschalten zwischen weißer und schwarzer Linienführung.
Standardmäßig folgt der Roboter weißen Linien; Klicken Sie auf die Schaltfläche, um zur schwarzen Linie zu wechseln.
- Die Zeilenfolgefunktion analysiert zwei Pixel parallel und verwendet die erkannten Informationen; die Positionen dieser beiden Pixel sind "L1" und "L2".
    `SP` ist der Schwellenwert des Abbiegebefehls basierend auf den Ergebnissen der visuellen Analyse.
Ein größerer "SP"-Wert bedeutet eine große Abweichung; obwohl ein besonders kleiner `SP`-Wert den Roboter an der Bewegung hindern kann, da er das Ziel nicht anvisieren und die Richtung finden kann.

- Wenn die visuelle Linienverfolgungsfunktion aktiviert ist, wird der Videobildschirm automatisch zu binarisierten Ergebnissen, wodurch die visuelle Analyse klarer wird.
- Das Fenster "Hardware" zeigt die CPU-Temperatur, die CPU-Auslastung und die Speichernutzung des Raspberry Pi an.
- Das Fenster "Aktionen" steuert einzigartige Funktionen des Roboters:
    - `MOTION GET`: Bewegungserkennungsfunktion basierend auf OpenCV.
Wenn sich Objekte im Blickfeld der Kamera bewegen, umkreist das Programm das Teil im 'Video'-Fenster und das LED-Licht am Roboter zeigt die entsprechenden Änderungen an.
    - `AUTO MATIC`: Hindernisvermeidungsfunktion basierend auf Ultraschall.
Wenn das Ultraschallmodul des Roboters ein Hindernis erkennt, biegt er automatisch nach links ab und macht einen Schritt zurück, bevor er sich dreht, wenn er sich zu nahe am Hindernis befindet.
    - `DISTANCE BEHALTEN`: Die Funktion des Abstandhaltens basierend auf Ultraschall.
Wenn der Ultraschall des Roboters ein Hindernis vor ihm erkennt, hält er einen Abstand von 0,35 m zum Hindernis vor ihm.
    - `TRACK LINE`: Linienverfolgungsfunktion durch Verwendung des 3-Kanal-Infrarotmoduls.
Standardmäßig verfolgt es schwarze Linien auf einer weißen Oberfläche (ein weißer Hintergrund, der Infrarot reflektiert, und 1 cm breite schwarze Linien, die kein Infrarot reflektiert).
Die Leistung der Linienverfolgung variiert von Oberflächen- und Linienmaterialien sowie der Höhe des Roboterchassis.
Möglicherweise benötigen Sie einen Kreuzschraubendreher, um das Potentiometer am Linienverfolgungsmodul einzustellen.
- `SPEECH` Die Funktion der Sprachsteuerung basiert auf dem Spracherkennungsmodul, den Sprachbefehlen zur Steuerung des Roboters.
EIN Derzeit unterstützt der Roboter nur die Befehle vorwärts, rückwärts, links abbiegen und rechts abbiegen und kann nur Englisch erkennen.
- Das Fenster `FC Control` steuert die Farbsperrfunktion des Roboters:

    `START`: Aktivieren oder deaktivieren Sie die Farbsuch- und -verfolgungsfunktion.
    `FARBE`: Wählen Sie die zu verfolgende Farbe.

    Wenn die Funktion aktiviert ist, sperrt der Roboter automatisch eine bestimmte Farbe in der Kameraansicht.
Standardmäßig verfolgt es leuchtend gelbe Objekte.
Sie können die Farbe nach Belieben ändern.
Wenn ein Objekt gesperrt ist, leuchtet die LED am Roboter orange.
Die Kamera des Roboters kann nicht nur Nickbewegungen ausführen, sondern auch Objekte einer bestimmten Farbe horizontal arretieren.
- `Radar-Scan-Steuerung`:
Die Radar-Scanfunktion basiert auf Ultraschall.
Der Roboter nimmt einen Radius von mehr als einem Meter vor sich als Radius, scannt von links nach rechts und erfasst den Abstand aller Hindernisse.
Es zeigt die Hindernisse auf einer Seite an und jedes Hindernis ist ein Punkt.
- `PWM INIT SET`: Wird verwendet, um den Anfangswinkel jedes Servoanschlusses des Roboters einzustellen.
Wenn Sie feststellen, dass der Winkel eines bestimmten Servos Ihres Roboters nicht richtig ist, können Sie diese Funktion verwenden, um ihn auf den richtigen Winkel abzustimmen.

![Web- Interface](images/100.jpg)

## 6 Häufige Probleme und Lösungen (Fragen und Antworten)

- Wo finde ich die IP-Adresse des Raspberry Pi?
Bevor Sie den Raspberry Pi per SSH verbinden, müssen Sie die IP-Adresse des Raspberry Pi kennen.
Überprüfen Sie die Verwaltungsoberfläche Ihres Routers oder laden Sie die App `Network Scanner` herunter -> suchen Sie nach einem Gerät namens `RASPBERRY` oder `Raspberry Pi Foundation`, um die IP-Adresse zu erhalten.
Weitere Methoden zum Abrufen der IP-Adresse des Raspberry Pi finden Sie in der offiziellen Dokumentation [IP-Adresse]
- Fehler treten mit der Eingabeaufforderung "Berechtigung verweigert" auf, wenn ich "server.py" oder "webServer.py" manuell ausführe.
Der Raspberry Pi benötigt die Root-Berechtigung, um die abhängigen Bibliotheken für die WS2812 LED-Lichtsteuerung auszuführen.
Sie müssen `sudo` am Anfang von `server.py` oder `webServer.py` hinzufügen, um das Programm auszuführen.

    ```
sudo python3 [PFAD]/server.py
sudo python3 [PFAD]/webServer.py
    ```

- Ich kann den Hot Pot für den Roboter nicht erstellen.
Sie müssen das Open-Source-Projekt create_ap verwenden, um den Hotspot des Roboters einzurichten.
Trennen Sie vor der Verwendung das WLAN-Netzwerk, aber schalten Sie das WLAN-Modul NICHT aus, sonst zeigt create_ap einen Fehler an, dass die Hardware blockiert ist.

- Der Servo dreht sich ungewöhnlich stark.
Vor dem Zusammenbau von Kipphebel und Servo müssen Sie die Servozahnräder in die mittlere Position ihres Drehbereichs drehen lassen.
Montieren Sie dann den Kipphebel gemäß dem in der Dokumentation angegebenen Winkel.
Aufgrund des Aufbaus des Servos (Zähnezahl 20 bei den Servozahnrädern) kann es zu einer Abweichung von weniger als 9° kommen.
Für eine bessere Leistung können Sie die Servosteuerungsdokumentation für die anfängliche Gradeinstellung nach Code lesen.

- Das Servo wackelt.
Wahrscheinlich ist das Servo-Untersetzungsgetriebe kaputt.

- Raspberry Pi kann nicht booten.
Entfernen Sie alle Teile auf der Treiberplatine.
Nur das Board an Raspberry Pi und Stromversorgung anschließen, neu starten.

- "Remote-Seite unerwartet geschlossene Netzwerkverbindung" wird in einem Popup-Fenster angezeigt.
Während der Installation kann es zu Fehlermeldungen kommen, da der Raspberry Pi nach der Installation automatisch neu gestartet wird, wodurch die Platine getrennt wird.

- Programm stürzt nach Doppelklick auf client.py oder GUI.py ab.
Führen Sie das Skript von `python client.py` oder `python GUI.py` in cmd aus und überprüfen Sie die Fehlerberichte.

- Wie initialisiere ich den Winkel des Servos?
Wenn Sie die Softwareinstallation auf dem Raspberry Pi abgeschlossen haben, booten Sie ihn einfach und das Servo wird initialisiert.

- Ich kann über SSH eine Verbindung zum Raspberry Pi-Terminal herstellen \ Raspberry Pi konnte keine WLAN-Verbindung herstellen.
Die Stromversorgungsmethoden haben keinen Einfluss auf die Steuerung durch SSH.
Prüfen Sie, ob Sie die Datei `wpa_supplicant.conf` mehrmals erstellt haben.
Wenn ja, verursacht dieses Problem SSH-Fehler.

- Kann ich den Motor HAT und Raspberry Pi über USB versorgen?
Für einen Raspberry Pi 3B wird ein 2A-Ausgang benötigt, für einen Raspberry Pi 4 werden mindestens 3A benötigt.
Sie können die USB-Stromversorgung für die Softwareinstallation und zum Testen verwenden, aber sie ist nicht für Hochleistungsmodule wie Servo- oder Motoranpassungen geeignet, da dies zu einer niedrigen Spannung führen kann.
Es wird empfohlen, hier eine Batterie zur Stromversorgung zu verwenden.

- Nach der Installation zeigt der Roboter beim Booten keine Reaktion.
Die Datei `server.py` oder `webServer.py` kann aus bestimmten Gründen nicht ausgeführt werden.
Versuchen Sie, `server.py` oder `webServer.py` manuell auszuführen und prüfen Sie, ob eine Fehlermeldung angezeigt wird.

- Das Servo kehrt beim Anschluss an die Treiberplatine nicht in die Mittelstellung zurück.
Im Allgemeinen führt der Raspberry Pi beim Booten automatisch `webServer.py` aus, und `webServer.py` wird laufen und die Servo-Ports steuern, um ein Signal zum Drehen in die Mittelposition zu senden.
Beim Zusammenbau des Servos können Sie es jederzeit an einen beliebigen Servoanschluss anschließen.
Nach dem Anschließen des Servos an den Port drehen sich die Zahnräder in die Mittelposition; Montieren Sie den Kipphebel am Servo.
Trennen Sie den Server vo aus dem Anschluss und fügen Sie weitere Servos ein, um die Kipphebelmontage zu wiederholen (alle Servos befinden sich in der Mittelposition).
Wenn das Servo eingeschaltet ist, versuchen Sie, den Kipphebel zu bewegen.
Wenn es nicht bewegt werden kann, zeigt es das Programm für die Servos an; andernfalls gibt es einen Fehler für das Servoprogramm.
Führen Sie die Zeile `[RobotName]/initPosServos.py` aus (ersetzen Sie `[RobotName]` durch den Ordnernamen Ihres Roboterprogramms), um das Servo in die Mittelposition zu drehen.
Beim Booten (es kann 30-50s dauern) dauert es eine Weile, bis der Raspberry Pi PCA9685 steuert, um das Signal aller Servoports für die Mittelpositionsdrehung einzustellen.

- kein cv2-Fehler tritt auf, wenn ich `server.py` oder `webServer.py` manuell ausführe.
OpenCV ist nicht richtig installiert.
Geben Sie den Befehl sudo pip3 install opencv-contrib-python in den Raspberry Pi ein, um OpenCV manuell zu installieren.

- Wenn ein Computer verwendet wird, um ssh und wpa_supplicant.conf auf die SD-Karte zu kopieren, wird angezeigt, dass keine SD-Karte vorhanden ist.
Ziehen Sie in diesem Fall den Kartenleser aus der Steckdose und schließen Sie ihn an den Computer an.

- SSH kann keine Verbindung herstellen, Fehler WARNUNG: REMOTE HOST IDENTIFICATION HAT GEÄNDERT!
Geben Sie Folgendes in die Befehlszeile ein und drücken Sie die Eingabetaste

    ```
ssh-keygen -R Fügen Sie die IP-Adresse des Raspberry Pi hinzu.
    ```

Zum Beispiel:

ssh-keygen -R 192.168.3.157

Dann können Sie wieder per SSH auf den Raspberry Pi zugreifen.

- Raspberry Pi startet nach dem Booten automatisch neu / startet den Roboter neu, sobald er sich zu bewegen beginnt
Wenn Ihr Roboter nach dem Einschalten automatisch neu startet oder die Verbindung trennt und neu startet, wenn der Roboter nach dem normalen Einschalten beginnt, sich zu bewegen.
Dies liegt wahrscheinlich daran, dass Ihr Netzteil nicht genügend Strom ausgibt und der Roboter das Programm beim Start automatisch ausführt.
Bringen Sie alle Servos in Neutralstellung, der durch diesen Vorgang verursachte Spannungsabfall führt zum Neustart des Raspberry Pi.
Wir haben getestet, dass bei Verwendung eines 7,4 V-Netzteils der Spitzenstrom des Roboters etwa 3,75 A beträgt. Sie müssen also eine Ausgangsbatterie mit 4 A unterstützen.

- Die Richtung der Servobewegung ist falsch.
Aufgrund der unterschiedlichen Chargen von Servos, wenn den Servos der gleiche Winkeländerungstrend gegeben wird.
Die tatsächliche Bewegungsrichtung der Servos kann entgegengesetzt sein.
Wir haben eine Schnittstelle eingerichtet, um die Richtung der Servos im Programm anzupassen.
Sie müssen RPIservo.py öffnen,
Suchen Sie das Array sc_direction in ServoCtrl.
Wenn die Richtung des Servos von Port 3 umgekehrt ist, ändern Sie die vierte 1 auf -1.
(Die Seriennummer des Arrays beginnt bei Null, also entspricht Port 3 der vierten 1).
Wenn die Servorichtung von Port 3 nicht korrekt ist: Vor der Änderung:

>self.sc_direction = [1,1,1,1, 1,1,1,1, 1,1,1,1, 1,1,1,1]

Nach der Änderung (die Seriennummer des Arrays beginnt bei Null, also entspricht Port 3 dem vierten 1):

>self.sc_direction = [1,1,1,-1, 1,1,1,1, 1,1,1,1, 1,1,1,1]

- Bewegungsrichtung des Motors ist falsch
Aufgrund der unterschiedlichen Motorenchargen kann bei gleichem Signal die Drehrichtung des Motors unterschiedlich sein.
Wir haben eine Schnittstelle zur Einstellung der Drehrichtung des Motors im Programm eingestellt.
Sie müssen move.py öffnen.
Im Programmteil sehen Sie Zu den folgenden Variablendefinitionen:

    Dir_forward = 0
    Dir_backward = 1
    left_forward = 0
    left_backward = 1
    right_forward = 0
    rechts_rückwärts = 0

Wenn alle Ihre Motoraktionen umgekehrt sind, ändern Sie einfach Dir_forward = 0 in Dir_forward = 1, Ändern Sie einfach Dir_backward = 1 in Dir_backward = 0.
Wenn Sie nur einen Motor reversiert haben, müssen Sie nur den entsprechenden Variablensatz ändern.
- Nach dem Ausführen des Servers erhalte ich eine Fehlermeldung und kann config.txt nicht finden.
Dies liegt daran, dass das Installationsskript die Datei config.txt aufgrund von Berechtigungsproblemen während der Installation nicht an den angegebenen Speicherort kopiert hat.
Die neue Version von webServer verwendet diese Datei nicht, sondern nur die alte Version des Servers.
Kopieren Sie den Serverordner des Raspberry Pi nach /etc/ des Raspberry Pi, verwenden Sie den folgenden Befehl.

    ```
    sudo cp -f //home/pi/adeept_PiCar-B/server/config.txt //etc/config.txt
    ```

    Ersetzen Sie einfach oben adeept_PiCar-B durch Ihren Produktnamen, wir nehmen hier PiCar-B als Beispiel.

- Das Ausführen von GUI.py meldet den ip.txt NotFound-Fehler.
Der korrekte Betriebsmodus besteht darin, GUI.py direkt im GUI-Verzeichnis auszuführen.
Wenn Sie GUI.py in einem anderen Verzeichnis ausführen, wird in Ihrem aktuellen Verzeichnis nach ip.txt gesucht.

## 7 Stellen Sie das Programm so ein, dass es automatisch startet

### 7.1 Festlegen, dass das angegebene Programm beim Booten automatisch ausgeführt wird
XXXXXXXXX
In diesem Abschnitt wird nur die von unseren Produkten verwendete Autostart-Methode vorgestellt.
Wenn Sie weitere Informationen über das Auto-Run-Programm von Raspberry Pi benötigen, können Sie dieses Dokument von [itechfythe](https://www.itechfy.com/) Dokument [Auto-Run](https://www.itechfy.com/tech/auto-run-python-program-on-raspberry-pi-startup/).

Wenn Sie die Arbeitsschritte **3.5** oder **3.6** verwendet haben, wurde das Skriptprogramm so konfiguriert, dass das Programm beim Start automatisch ausgeführt wird.
In diesem Kapitel haben wirerklären, wie Sie ein Programm so einstellen, dass es beim Start automatisch von Grund auf neu gestartet wird.

Zuerst verwenden wir den folgenden Code, um eine neue startup.sh zu erstellen:
    ```
	sudo touch //home/pi/startup.sh
    ```

Die startup.sh bearbeiten:  
    ```
	sudo nano startup.sh
    ```

Schreiben Sie den folgenden Inhalt in startup.sh, wobei auf python3 das Programm folgt, das automatisch ausgeführt werden soll.
Beachten Sie, dass Sie hier einen absoluten Pfad verwenden müssen.
Nehmen wir als Beispiel webServer.py.

>\#!/bin/sh  
    ```
sudo python3 [Robotername]/server/webServer.py
    ```

Nach `Strg + X` Um die Bearbeitung zu beenden. Drücken Sie Y Speichern. `Enter` Bestätigen und Bearbeiten beenden.
Geben Sie startup.sh-Berechtigungen, wobei \*\*\* der Linux-Berechtigungscode ist. Wir empfehlen die Verwendung von Berechtigungen wie 777 nicht, aber für Anfänger kann 777 viele Konto- und Berechtigungsprobleme vermeiden.
Sie können ihn natürlich auch auf 700 setzen.
Damit nur der Besitzer die startup.sh lesen, schreiben und ausführen kann.
Weitere Informationen zu Linux-Berechtigungen finden Sie in diesem Artikel von [maketecheasier](https://www.maketecheasier.com/) dem Artikellink [Understanding File Permissions](https://www.maketecheasier.com/file-permissions-what-does-chmod-777-means/).

    ```
	sudo chmod 777 //home/pi/startup.sh
    ```

- Bearbeiten Sie rc.local, um das Skript so zu konfigurieren, dass es automatisch ausgeführt wird.
    ```
sudo nano /etc/rc.local
    ```

- Folgende Inhalte unter fi im Originaldokument hinzufügen, speichern und beenden:
    ```
//home/pi/startup.sh start
    ```
- Natürlich können Sie den obigen Skriptdateipfad auch durch andere Skripte ersetzen, die automatisch ausgeführt werden sollen.


## 7.2 Ändern Sie das Programm, das automatisch startet

Nach Schritt **7.1** können Sie das Programm bereits so einstellen, dass es beim Booten automatisch ausgeführt wird.
Wenn Sie das Programm so ändern möchten, dass es beim Booten automatisch ausgeführt wird.
Bearbeiten Sie einfach startup.sh:

    ```
    sudo nano //home/pi/startup.sh
    ```

- Wenn wir beispielsweise webServer.py durch server.py ersetzen möchten, müssen wir nur Folgendes bearbeiten:
Ersetzen

    ```
sudo python3 [Robotername]/server/webServer.py
    ```

mit

    ```
sudo python3 [Robotername]/server/server.py
    ```

- Speichern und beenden Sie, damit der Roboter beim nächsten Einschalten automatisch server.py anstelle von webServer.py ausführt.
- server.py ist ein Socket-Server, der bei der Verwendung von PythonGUI verwendet wird.
Wir empfehlen es Anfängern hier nicht, da Sie viele abhängige Bibliotheken manuell auf dem Computer installieren müssen, der sie steuert, damit die GUI normal mit ihr kommunizieren kann.
Es wird empfohlen, die WEB-Anwendung zu verwenden, um den Raspberry Pi-Roboter zu steuern.

## 8 Fernbedienung von Raspberry Pi über MobaXterm

- Um die tägliche Nutzung des Raspberry Pi komfortabler zu gestalten, schließen wir in der Regel keine Peripheriegeräte wie Maus, Tastatur und Monitor an den Raspberry Pi an.
Da unser Raspberry Pi im Roboter installiert ist, oft mit Peripheriegeräten zur Steuerung des Raspberry Pi, wird die Effizienz des Programmierens und Testens ernsthaft beeinträchtigt.
Daher stellen wir eine Methode zur Programmierung im Raspberry Pi vor.
- Es gibt viele Möglichkeiten, den Raspberry Pi zu programmieren.
Sie können sich beispielsweise mit **3.x am Raspberry Pi** anmelden, ohne ein Drittanbieter-Tool zu verwenden.
Sie können auch Dateien im Raspberry Pi erstellen.
Fast alle Operationen können SSH verwenden, um sich mit dem Raspberry Pi im Terminal zu verbinden, aber für viele Leute wird es eine enttäuschende Erfahrung sein, wenn viele Codes in das Terminal geschrieben werden.
In diesem Kapitel wird eine Methode vorgestellt, die die Übertragung von Dateien auf den Raspberry Pi erleichtern kann.
Diese Methode kann Programme direkt im Raspberry Pi bearbeiten.
- Diese Methode erfordert die Drittanbietersoftware MobaXterm, [Website-Adresse](https://mobaxterm.mobatek.net/download.html "MobaXterm").
- MobaXterm ist eine Terminal-Tool-Software, mit der der Raspberry Pi ferngesteuert werden kann und die Fernsteuerung verfügbar ist, wenn SSH aktiviert ist.
Für die Methode von Raspberry Pi, SSH zu aktivieren und automatisch eine Verbindung zum WIFI herzustellen.
Siehe Schritte **2.2** und **2.3**.
- Laden Sie MobaXterm herunter und installieren Sie es.
- Um die IP-Adresse des Raspberry Pi zu erhalten.
Sie können sich auf die Methode von **3.x beziehen und sich in diesem Dokument beim Raspberry Pi** anmelden, um die IP-Adresse des Raspberry Pi zu erhalten.
- Um MobaXterm auszuführen.
Erstellen Sie zunächst eine neue Sitzung, klicken Sie oben links auf Sitzung.
Klicken Sie im Popup-Fenster auf SSH, geben Sie die IP-Adresse des Raspberry Pi hinter Remote-Host ein und klicken Sie abschließend auf OK.
Der Standardkontoname des Raspberry Pi ist pi.
Das Standardpasswort ist Himbeere.
Nur das Passwort erscheint nicht auf dem Bildschirm, wenn Sie es eingeben und die \*-Nummer hat keine Bedeutung **Enter** erfolgreich.
Drücken Sie nach dem Login, um sich beim Raspberry Pi anzumelden, MobaXterm erinnert Sie daran, das Passwort zu speichern.
Sie müssen wählen.
- Wenn Benutzername und Passwort korrekt sind.
Sie können den Benutzernamen und das Passwort entsprechend der Eingabeaufforderung im Terminal ändern, was sicherer ist.
- Nach erfolgreichem Login speichert MobaXterm automatisch die Konversation.
Wenn wieder mit dem Raspberry Pie verbundenBeim nächsten Mal muss nur noch ein Doppelklick auf die linke Seite der IP-Adresse erforderlich sein, um wieder mit dem Raspberry Pi verbunden zu werden.
Wenn kein Benutzername und kein Kennwort gespeichert sind, müssen Sie den Benutzernamen und das Kennwort eingeben.
Wenn sich die IP-Adresse des Raspberry Pi geändert hat, müssen Sie einen neuen Dialog starten.
- Nach erfolgreicher Anmeldung wird die linke Spalte durch ein Dateiübertragungssystem ersetzt.
Dadurch können Sie mit dem System im Raspberry Pi interagieren.
Wenn Sie zur Sitzungsauswahl zurückkehren möchten, klicken Sie einfach auf Sitzungen.
- Programme, die Sie auf anderen Geräten schreiben, können durch einfaches Drag & Drop auf den Raspberry Pi übertragen werden, und dann kann der Raspberry Pi im Terminal gesteuert werden, um das Programm auszuführen.
Oder die Dateien im Raspberry Pi können auf andere Geräte gezogen werden.
- Wenn Sie eine andere IDE verwenden möchten, um Dateien in Raspberry Pi zu bearbeiten.
Sie finden die Datei, die Sie bearbeiten möchten, im Dateiübertragungssystem auf der linken Seite von MobaXterm.
Klicken Sie mit der rechten Maustaste auf diese Datei und wählen Sie Ihre IDE aus, damit Sie Ihre bevorzugte IDE auf anderen Geräten verwenden können, um die Raspberry Pi-Datei zu bearbeiten. Nachdem die Bearbeitung abgeschlossen ist, **STRG+S** speichern Sie die Datei.
- Es ist jedoch zu beachten, dass wenn Sie das Dateiübertragungssystem von MobaXterm verwenden, um Dateien auf dem Raspberry Pi zu bearbeiten.
Sie müssen auf das Berechtigungsproblem achten.
Weil das Dateiübertragungssystem keine Root-Berechtigungen hat.
Wenn Sie also nach der Bearbeitung der Datei zum Speichern aufgefordert werden.
Der Fehler "Berechtigung verweigert" führt dazu, dass die Datei nach der Bearbeitung nicht gespeichert werden kann.
Sie müssen den folgenden Befehl verwenden, um der Datei, die Sie bearbeiten möchten, die Berechtigung zu erteilen, von MobaXterm bearbeitet zu werden:

    ```
sudo chmod 776 [Dateiname]
    ```

- Weitere Informationen zu Linux-Berechtigungen finden Sie im Artikel [maketecheasier](https://www.maketecheasier.com/ "maketecheasier") über den Artikellink [Understanding File Permissions](https://www.maketecheasier.com/file- permissions-what-does-chmod-777-means/ "Dateiberechtigungen verstehen").

## 9 So steuern Sie die WS2812 RGB-LED

- WS2812 LED-Licht ist ein häufig verwendetes Modul unserer Roboterprodukte.
An jedem Modul befinden sich drei WS2812-Leuchten.
Bitte achten Sie beim Anschließen darauf.
Die Signalleitung hat eine andere Richtung, die nach dem Herausführen aus dem Raspberry Pi mit dem WS2812 verbunden werden muss.
Das IN-Ende des LED-Lampenmoduls, wenn das nächste WS2812-LED-Modul angeschlossen werden muss, wird die Signalleitung aus dem OUT-Ende des vorherigen WS2812-Moduls herausgeführt und mit dem IN-Ende der nächsten WS2812-LED verbunden.
- Bei Verwendung des Raspberry Pi mit installierter Treiberplatine Motor HAT kann das WS2812 LED-Modul mit einem 3-Pin-Kabel an die WS2812-Schnittstelle des Motor HAT angeschlossen werden.
- Wir verwenden eine Drittanbieterbibliothek [rpi_ws281x](https://pypi.org/project/rpi-ws281x/ "rpi_ws281x") um das WS2812 LED-Licht zu steuern. Sie können mehr über dieses Projekt auf [GitHub](https ://github.com/richardghirst/rpi_ws281x "GitHub").
- Wenn Sie das WS2812 LED-Modul an die WS2812-Schnittstelle von Motor HAT anschließen, entspricht die Signalleitung dem Raspberry Pi Auf GPIO 12 können Informationen zur Pin-Nummer des Raspberry Pi diesem offiziellen Dokument entnommen werden [GPIO](https:// www.raspberrypi.com/documentation/computers/raspberry-pi.html "GPIO").
- Verwenden Sie den folgenden Befehl, um rpi_ws281x für den Raspberry Pi zu installieren.
Da auf dem Raspberry Pi zwei Python-Versionen eingebaut sind, wird der Python3-Code als Beispiel verwendet, sodass pip3 zur Installation der Bibliothek verwendet wird.
    ```
pip3 installieren rpi-ws281x
    ```
- Als nächstes erklären wir das Programm.
Dieses Programm wird im Raspberry Pi geschrieben und im Raspberry Pi ausgeführt.
Die genaue Methode finden Sie unter **8 Programmierung im Raspberry Pi**.
- Abhängigkeiten importieren:
```
Importzeit
aus rpi_ws281x-Import *
```

- Aufbau der LED-Steuerungsklasse:
```
Klasse LED:
def __init__(selbst):
self.LED_COUNT = 16 # Auf die Gesamtzahl der LED-Leuchten am Roboterprodukt einstellen.
# Es gibt mehr LED-Leuchten auf dem Raspberry Pi.
self.LED_PIN = 12 # Auf die Eingangspinnummer der LED-Gruppe setzen.
self.LED_FREQ_HZ = 800000
selbst.LED_DMA = 10
self.LED_BRIGHTNESS = 255
self.LED_INVERT = Falsch
self.LED_CHANNEL = 0

# Verwenden Sie das obige Konfigurationselement, um einen Streifen zu erstellen.
self.strip = Adafruit_NeoPixel(
selbst.LED_COUNT,
selbst.LED_PIN,
selbst.LED_FREQ_HZ,
selbst.LED_DMA,
self.LED_INVERT,
self.LED_BRIGHTNESS,
self.LED_CHANNEL
)
self.strip.begin()
```
- Instanziieren Sie das Objekt und führen Sie die Methodenfunktion aus.
Die Funktion colorWipe() muss drei Parameter übergeben, nämlich R, G und B, die der Helligkeit der drei Primärfarben Rot, Grün und Blau entsprechen.
Der Wertebereich ist 0-255, je größer der Wert, desto höher die Helligkeit des entsprechenden Farbkanals.
Sind die Werte der drei Farbkanäle gleich, wird weißes Licht emittiert.
Konkrete Beispiele sind wie folgt:

```
if __name__ == '__main__':
LED = LED ()
Versuchen:
während 1:
LED.colorWipe(255, 0, 0) # Alle Lichter werden rot.
Time.schlaf(1)
LED.colorWipe(0, 255, 0) # Alle Lichter werden grün.
Zeit.Schlaf(1)
LED.colorWipe(0, 0, 255) # Alle Lichter werden blau.
Zeit.Schlaf(1)
außer:
LED.colorWipe(Color(0,0,0)) # Schalten Sie alle Lichter aus.
```

- Der obige Code steuert alle WS2812-Leuchten, um durch die drei Farben zu wechseln. Drücken Sie STRG + C, um das Programm zu beenden.
- Wenn Sie die Farbe einer einzelnen Lampe steuern möchten.
Sie können den folgenden Code verwenden.
Wobei i die Seriennummer der Lampe ist.
Die Seriennummer der ersten über die Treiberplatine angeschlossenen Lampe ist 0 und die der zweiten Lampe ist 1.
Analog dazu sind R, G, B die Helligkeit der entsprechenden drei Farbkanäle:

```
LED.strip.setPixelColor(i, Farbe(R, G, B))
LED.strip.show()
```

- Hinweis: Sie müssen die Methode Color() verwenden, um die RGB-Werte zu packen und sie dann an setPixelColor() zu übergeben.

## 10 So steuern Sie den Servo

### 10.1 Steuern Sie das Lenkgetriebe, um sich in einen bestimmten Winkel zu drehen

- Da das Servo das PWM-Signal verwenden kann, um den Drehwinkel eines Mechanismus zu steuern.
Es ist ein häufiger verwendetes Modul für Roboterprodukte.
Laufroboter, Roboterarme und Gimbals werden alle vom Servo angetrieben.
In unserem Raspberry Pi verfügt die Treiberplatine Motor HAT über einen dedizierten PCA9685-Chip zur Steuerung des Servos.
Der Raspberry Pi verwendet I2C, um mit dem PCA9685 zu kommunizieren.
Sie müssen nur die Raspberry Pi-Treiberplatine Motor HAT auf dem Raspberry Pi installieren, und der Raspberry Pi wird mit dem PCA9685 verbunden.
Für den Anschluss sind keine weiteren Drähte erforderlich.
- Der Raspberry Pi verwendet Python-Code zur Steuerung des Lenkgetriebes und erfordert Bibliotheken von Drittanbietern Adafruit_PCA9685, Adafruit-PCA9685Projektadresse.
Wenn Sie das Installationsskript der Robotersoftware ausführen, müssen Sie es nicht erneut manuell installieren.
Wenn Sie nicht die Sicherheit haben, den Roboter auszuführenUm das Skript zu installieren, verwenden Sie den folgenden Befehl, um Adafruit_PCA9685 für Python3 auf dem Raspberry Pi zu installieren:

```
sudo pip3 installieren adafruit-pca9685
```

- Nach der Installation können Sie den Python3-Code im Raspberry Pi verwenden, um das Servo zu steuern:

```
import Adafruit_PCA9685 # Importiert die Bibliothek, die für die Kommunikation mit PCA9685 verwendet wird.
Importzeit

pwm = Adafruit_PCA9685.PCA9685() # Instanziieren Sie das Objekt, das zur Steuerung der PWM verwendet wird.
pwm.set_pwm_freq(50) # Setzt die Frequenz des PWM-Signals.

während 1: # Das Servo, das mit dem Servoanschluss Nr. 3 auf der Motor-HAT-Antriebsplatine verbunden ist, hin- und herbewegen.
pwm.set_pwm(3, 0, 300)
Zeit.Schlaf(1)
pwm.set_pwm(3,0, 400)
Zeit.Schlaf(1)
```

- Im obigen Code wird set_pwm_freq (50) verwendet, um die PWM-Frequenz auf 50 Hz einzustellen.
Diese Einstellung hängt vom Modell des Servos ab.
Das von unserem Roboterprodukt verwendete Servo muss durch ein 50Hz PWM-Signal gesteuert werden.
Wenn Sie andere verwenden Der Wert des Servos muss anhand der spezifischen Servodokumentation eingestellt werden.
- pwm.set_pwm (3, 0, 300) Diese Methode wird verwendet, um die Drehung eines Servos auf eine bestimmte Position zu steuern, wobei 3 die Servo-Portnummer ist.
Dies entspricht der Nummer auf der Motor HAT-Treiberplatine, aber achten Sie auf das Ruder.
Wenn die Maschine an die Antriebsplatine angeschlossen ist, stecken Sie das Erdungskabel, VCC und Signalkabel nicht in umgekehrter Richtung ein, braun zu schwarz, rot zu rot, gelb zu gelb; 0 ist die Abweichung der Steuerung der Drehung des Servos.
Unser Programm verwendet diese Funktion nicht, um die Abweichung zu korrigieren.
(Der Grund für den Fehler des Lenkgetriebes kann sich auf **4.2 Hinweis zur strukturellen Montage** beziehen); 300 ist der PWM-Tastverhältniswert, den Sie einstellen möchten.
Je nach Servo repräsentiert dieser Wert unterschiedliche Servowinkel.
Der PWM-Tastverhältnisbereich der von uns verwendeten Servos beträgt ca. 100 bis 560, was einem Drehbereich von ca. 0° bis 180° entspricht.
- Der obige Code zur Steuerung des Lenkgetriebes steuert nicht die Drehzahl des Lenkgetriebes.
Wenn wir ein bestimmtes Lenkgetriebe langsam zwischen zwei Stellungen hin- und herschwingen lassen wollen, müssen wir zur Steuerung des Lenkgetriebes eine zunehmende oder abnehmende Variable verwenden.


## 10.2 Steuern Sie die Zeitlupe des Lenkgetriebes

```
import Adafruit_PCA9685 # Importieren Sie die Bibliothek, die für die Kommunikation mit PCA9685 verwendet wird
Importzeit

pwm = Adafruit_PCA9685.PCA9685()# Instanziieren des Objekts, das zur Steuerung der PWM verwendet wird
pwm.set_pwm_freq(50) # Setzt die Frequenz des PWM-Signals

während 1:
für i im Bereich (0,100): # Bewegen Sie das Servo langsam von 300 auf 400
pwm.set_pwm(3, 0, (300+i))
time.sleep(0.05)
für i im Bereich (0,100): # Bewegen Sie das Servo langsam von 400 auf 300
pwm.set_pwm(3, 0, (400-i))
time.sleep(0.05)
```

- Der obige Code kann dazu führen, dass sich das Lenkgetriebe zwischen 300 und 400 langsam hin und her dreht, aber diese Methode zur Steuerung des Lenkgetriebes hat auch viele Nachteile.
Wenn das Programm ausgeführt wird, wird die langsame Bewegung des Lenkgetriebes blockiert.
Dies wird die Programmleistung ernsthaft beeinträchtigen.
Daher bieten wir in unserem Roboter-Produktprogramm eine Multithread-Lösung an, um dieses Problem zu lösen.


### 10.3 Nicht-blockierende Kontrolle

- Sie finden die Datei RPIservo.py im Serverordner des Roboterprodukts, kopieren Sie sie in den gleichen Ordner wie das Programm, das Sie ausführen möchten, und verwenden Sie diese Methode dann in Ihrem Programm.

```
import RPIservo # Importieren Sie eine Bibliothek, die mehrere Threads verwendet, um das Lenkgetriebe zu steuern.
Importzeit
sc = RPIservo.ServoCtrl() # Instanziieren Sie das Objekt, das das Lenkgetriebe steuert.
sc.start() # Startet diesen Thread, wenn sich das Servo nicht bewegt, wird der Thread ausgesetzt.
während 1:
sc.singleServo(3, -1, 2)
Zeit.Schlaf(1)
sc.stopWiggle()
sc.singleServo(3, 1, 2)
Zeit.Schlaf(1)
sc.stopWiggle()
```

- Der obige Code kann verwendet werden, um den Servo so zu steuern, dass er sich hin- und herbewegt, mit Ausnahme von time.sleep (), der die Ausführung des Kontextprogramms nicht blockiert.
- Rufen Sie singleServo () auf, um die Bewegung des Servos zu starten, rufen Sie stopWiggle () auf, um die Bewegung des Servos zu stoppen, wobei singleServo ()
Drei Parameter sind erforderlich, nämlich die Portnummer des zu steuernden Servos (3 dient zur Steuerung des Servos Nr. 3, das an Motor HAT angeschlossen ist), die Bewegungsrichtung des Servos (1 oder -1) und die Bewegungsgeschwindigkeit von des Servos (je größer der Wert, desto größer Je früher).

## 11 So steuern Sie den Gleichstrommotor

- Wenn die von Ihnen installierte Raspbian-Image-Version Raspbian Full ist, das von der offiziellen Website bereitgestellt wird, müssen Sie keine anderen abhängigen Bibliotheken installieren.
Wir müssen nur den GPIO-Port des Raspberry Pi für einfache hohe und niedrige Pegel und PWM steuern, um den L298N-Chip auf Motor HAT zu steuern und so die Richtung und Geschwindigkeit des Motors zu steuern.

- Wenn Sie die Motor HAT-Treiberplatine verwenden, um den Motor anzuschließen, weil der vom Motor benötigte Strom relativ groß ist, versuchen Sie, kein USB-Kabel zu verwenden, um den Raspberry Pi und die Treiberplatine mit Strom zu versorgen.
Auf der Treiberplatine befindet sich eine 2pin Vin-Schnittstelle, die genutzt werden kann.

```
Importzeit
import RPi.GPIO as GPIO # Importieren Sie die Bibliothek, die zur Steuerung von GPIO verwendet wird.

GPIO.cleanup() # Setzt die High- und Low-Pegel des GPIO-Ports zurück.
GPIO.setwarnings(False) # Ignoriere einige unbedeutende Fehler.
GPIO.setmode(GPIO.BCM) # Es gibt drei Kodierungsmethoden für den GPIO-Port des Raspberry Pi.
                            # Wir wählen die BCM-Kodierung, um den GPIO-Port zu definieren.
'''
Der folgende Code definiert den GPIO, der zur Steuerung des L298N-Chips verwendet wird.
Diese Definition ist für verschiedene Raspberry Pi-Treiberplatinen unterschiedlich.
'''
Motor_A_EN = 4
Motor_B_EN = 17
Motor_A_Pin1 = 14
Motor_A_Pin2 = 15
Motor_B_Pin1 = 27
Motor_B_Pin2 = 18

def motorStop(): # Stoppt die Motordrehung.
GPIO.Ausgang (Motor_A_Pin1,GPIO.LOW)
GPIO.output(Motor_A_Pin2,GPIO.LOW)
GPIO.Ausgang (Motor_B_Pin1,GPIO.LOW)
GPIO.output(Motor_B_Pin2,GPIO.LOW)
GPIO.Ausgang(Motor_A_EN,GPIO.LOW)
GPIO.Ausgang(Motor_B_EN,GPIO.LOW)

def setup(): # GPIO-Initialisierung, GPIO-Motor kann ohne Initialisierung nicht gesteuert werden.
global pwm_A, pwm_B GPIO.setwarnings(False)
GPIO.setmode(GPIO.BCM)
GPIO.setup(Motor_A_EN, GPIO.OUT)
GPIO.setup(Motor_B_EN, GPIO.OUT)
GPIO.setup(Motor_A_Pin1, GPIO.OUT)
GPIO.setup(Motor_A_Pin2, GPIO.OUT)
GPIO.setup(Motor_B_Pin1, GPIO.OUT)
GPIO.setup(Motor_B_Pin2, GPIO.OUT)
motorStop() # Verhindert, dass der Motor nach der Initialisierung automatisch anläuft.
try: # Try wird hier verwendet, um Fehler durch wiederholte PWM-Einstellungen zu vermeiden.
pwm_A = GPIO.PWM(Motor_A_EN, 1000)
pwm_B = GPIO.PWM(Motor_B_EN, 1000)
außer:
passieren

def motor_A(direction, speed): # Die Funktion zur Steuerung des Motors von Port A.
wenn Richtung == 1:
GPIO.output(Motor_A_Pin1,
GPIO.HIGH) GPIO.Ausgang (Motor_A_Pin2, GPIO.LOW)
pwm_A.start(100)
pwm_A.ChangeDutyCycle(Geschwindigkeit)
wenn Richtung == -1:
GPIO.output(Motor_A_Pin1, GPIO.LOW)
GPIO.Ausgang (Motor_A_Pin2, GPIO.HIGH)
pwm_A.start(100)
pwm_A.ChangeDutyCycle(Geschwindigkeit)

def motor_B(Richtung, Geschwindigkeit): # Die Funktion zur Steuerung des Motors von Port B.
wenn Richtung == 1:
GPIO.Ausgang (Motor_B_Pin1, GPIO.HIGH)
GPIO.output(Motor_B_Pin2, GPIO.LOW)
pwm_B.start(100)
pwm_B.ChangeDutyCycle(Geschwindigkeit)
wenn Richtung == -1: GPIO.output(Motor_B_Pin1, GPIO.LOW)
GPIO.Ausgang (Motor_B_Pin2, GPIO.HIGH)
pwm_B.start(100)
pwm_B.ChangeDutyCycle(Geschwindigkeit)

'''
Steuern Sie die Motoren A und B so, dass sie sich 3 Sekunden lang mit voller Geschwindigkeit drehen.
'''
motor_A(1, 100)
motor_B(1, 100)
Zeit.Schlaf(3)
'''
Steuern Sie die Motoren A und B so, dass sie sich 3 Sekunden lang mit voller Geschwindigkeit in entgegengesetzte Richtungen drehen.
'''
motor_A(-1, 100)
motor_B(-1, 100)
Zeit.Schlaf(3)
'''
Stoppen Sie die Motordrehung der Anschlüsse A und B.
'''
motorStop()
```
- Die obigen Codes können verwendet werden, um die Motorbewegung zu steuern.
Der Aufbau der beiden Funktionen motor_A und motor_B ist gleich, der Steuerservoanschluss ist jedoch unterschiedlich.
Diese Funktion erfordert zwei Parameter, einen die Richtung und den anderen die Geschwindigkeit.
1 oder -1.
Die minimale Geschwindigkeit ist 0 und der maximale Wert ist 100.
Seit derDie Geschwindigkeitsanpassung wird durch PWM angepasst, sie entspricht tatsächlich der Anpassung des Spannungswerts des Motoranschlusses.
Der Motor hat als Last einen Verzögerungsmechanismus.
Es findet keine Drehung statt, daher sollte der Geschwindigkeitswert nicht zu niedrig sein.

- Je nach der tatsächlichen Situation wird durch die Änderung des Geschwindigkeitswerts des vom Motor angetriebenen Roboters nur die Startgeschwindigkeit des Roboters verlangsamt, was sich nur geringfügig auf die Höchstgeschwindigkeit auswirkt, und wenn die angegebene Geschwindigkeit zu niedrig ist, wird der Motor verursacht zu stehen.

## 12 Ultraschallmodul

- Die von unserem Raspberry Pi-Roboter verwendete Kamera ist monokular und kann keine Tiefeninformationen erfassen.
Daher verwenden viele unserer Roboterprodukte Ultraschall-Entfernungsmodule, um Tiefeninformationen zu erhalten und zu erkennen, ob sich ein Hindernis in einer bestimmten Richtung befindet, um die Entfernung des Hindernisses zu ermitteln.

- Das Prinzip der Ultraschall-Bereichsmessung wird in der folgenden Formel dargestellt:

![formel](images/101.jpg "formel")

- S ist die Entfernung des Hindernisses, T2 ist der Zeitpunkt, zu dem das Echo empfangen wird, T1 ist der Zeitpunkt, zu dem die Schallwelle ausgesendet wird und Vs ist die Geschwindigkeit der Schallausbreitung in der Luft.
Wir können die obige Formel verwenden, um die Entfernung des Hindernisses zu bestimmen.

- Das in unseren Roboterprodukten verwendete Modell des Ultraschall-Entfernungsmoduls ist HC-SR04.
Das Modul HC-SR04 hat vier Pins, nämlich VCC, GND, Echo und Trig.
Entfernungserkennungsfunktion 2cm-400cm, Messgenauigkeit kann 3mm erreichen; Das Modul enthält Ultraschallsender, -empfänger und eine Steuerschaltung.
Das grundlegende Arbeitsprinzip ist wie folgt:
- Triggern Sie die Distanzmessung mit TRIG des IO-Ports und senden Sie automatisch 8 40-kHz-Rechteckwellen an ein High-Level-Signal.
- Modul von mindestens 10us und erkennt automatisch, ob ein Signal zurückkehrt.
- Wenn ein Signal zurückkehrt, wird ein High-Pegel über den IO-Port ECHO ausgegeben.
Die Dauer des hohen Pegels ist die Zeit vom Aussenden der Ultraschallwelle bis zur Rückkehr.

- Wenn die Motor-HAT-Treiberplatine verwendet wird, müssen Sie den HC-SR04 an die Ultraschallschnittstelle auf der Treiberplatine anschließen.
Sie dürfen es nicht an den IIC-Port anschließen, um ein Verbrennen des Ultraschallmoduls zu vermeiden.
(IIC ist eine Schnittstelle zum Anschließen von I2C-Geräten, und ihre VCC- und GND-Pinpositionen unterscheiden sich von Ultraschall.)

- Die Methode zur Verwendung von Python3 zum Erhalten von Ultraschall-Entfernungsergebnissen ist wie folgt:

```
RPi.GPIO als GPIO importieren
Importzeit

Tr = 11 # Pin-Nummer des Eingangsanschlusses des Ultraschallmoduls.
Ec = 8 # Pin-Nummer des Ausgangsanschlusses des Ultraschallmoduls.

GPIO.setmode(GPIO.BCM)
GPIO.setup(Tr, GPIO.OUT,initial=GPIO.LOW)
GPIO.setup(Ec, GPIO.IN)

def checkdist():
GPIO.output(Tr, GPIO.HIGH) # Stellen Sie das Eingangsende des Moduls auf High-Pegel und senden Sie eine anfängliche Schallwelle aus.
time.sleep(0.000015)
GPIO.Ausgabe(Tr, GPIO.LOW)

while not GPIO.input(Ec): # Wenn das Modul die anfängliche Schallwelle nicht mehr empfängt.
passieren
t1 = time.time() # Notieren Sie sich die Zeit, zu der die erste Schallwelle emittiert wird.
while GPIO.input(Ec): # Wenn das Modul die Rückschallwelle empfängt.
passieren
t2 = time.time() # Notieren Sie sich die Zeit, zu der die zurückkommende Schallwelle erfasst wird.
Rückrunde((t2-t1)*340/2,2) # Distanz berechnen
'''
Geben Sie Ultraschall-Bereichsergebnisse einmal pro Sekunde und zehnmal aus.
'''
für i im Bereich (10):
print(checkdist())
Zeit.Schlaf(1)
```

- Was das Ultraschallmodul betrifft, so ist dies ein in vielen Vorprojekten häufig verwendetes Modul, um die Komplexität des Programms zu reduzieren, obwohl dieser Code einen blockierenden Teil enthält.
Wir haben kein Multithreading verwendet, um es zu lösen.
Wenn Ihr Projekt hohe Anforderungen an die Produktleistung stellt, können Sie sich auf den Inhalt von **14** beziehen, um Multi-Thread-Ultraschall zu rekonstruieren.
- Wenn Ihr Projekt die Ultraschallfunktion verwenden muss, müssen Sie den obigen Code nicht neu schreiben.
Kopieren Sie einfach ultra.py aus dem Ordner des Roboterprogrammservers in denselben Ordner wie Ihr eigenes Projekt.
Verwenden Sie den folgenden Code, um Informationen zur Ultraschallentfernung zu erhalten:

```
ultra importieren
Abstand = ultra.checkdist()
```


## 13 Linienverfolgung

- Einige unserer Roboterprodukte sind mit einem Dreikanal-Infrarot-Linienpatrouillenmodul ausgestattet.
Das Linienpatrouillenmodul wird auf das Linienpatrouillen-Funktionsdesign des Roboters umgestellt.
Das Dreikanal-Infrarot-Linienpatrouillenmodul enthält 3 Gruppen von Sensoren, wobei jede Gruppe von Sensoren aus einer Infrarot-emittierenden LED und einem Infrarotsensor besteht, der aus einem photoelektrischen Transistor besteht.
Der Roboter bestimmt, ob eine Linie erkannt wird, indem er die Infrarotlichtintensität erkennt, die von dem Infrarotsensor-Fototransistor erkannt wird.
Es kann die weiße Linie (reflektiertes Infrarotlicht) auf schwarzem Hintergrund (nicht reflektiertes Infrarotlicht) erkennen und kann auch einen weißen Hintergrund erkennen.
Die schwarze Linie an (reflektiert Infrarotlicht) (reflektiert kein Infrarotlicht).

- Da der Raspberry Pi nur digitale Signale lesen kann, ist das Dreikanal-Infrarot-Tracking-Modul mit einem Potentiometer ausgestattet.
Mit einem Kreuzschraubendreher können Sie das Potentiometer am Infrarot einstellenTracking-Modul, um die Empfindlichkeit des Infrarotsensor-Fototransistors einzustellen.

- Unser Programm findet standardmäßig schwarze Linien auf weißem Hintergrund (reflektiert Infrarotlicht) (kein Reflektieren von Infrarotlicht).

- Bevor Sie das Dreikanal-Infrarot-Streckenpatrouillenmodul verwenden, müssen Sie es mit einem 5-poligen Kabel an die Tracking-Schnittstelle des Motor HAT anschließen.

- Das Dreiwege-Infrarot-Linienpatrouillenmodul hat ein Pfeilmuster auf der Rückseite des Sensors.
Die Pfeilrichtung ist die Richtung des Roboters.

- Die Codes des Dreikanal-Infrarot-Streckenpatrouillenmoduls lauten wie folgt:

```
RPi.GPIO als GPIO importieren
Importzeit
# Ausgangspin des Jagdmoduls.
line_pin_right = 19
line_pin_middle = 16
line_pin_left = 20
'''
Initialisieren Sie Ihren GPIO-Port bezogen auf das Line Patrol-Modul.
'''
def setup():
GPIO.setwarnings(Falsch)
GPIO.setmode(GPIO.BCM)
GPIO.setup(line_pin_right,GPIO.IN)
GPIO.setup(line_pin_middle,GPIO.IN)
GPIO.setup(line_pin_left,GPIO.IN)
def run():
'''
Lesen Sie die Werte von drei Infrarotsensor-Fototransistoren (0 ist keine Linie erkannt, 1 ist eine Linie erkannt).
Diese Routine nimmt die schwarze Linie auf weiß als Beispiel.
'''
status_right = GPIO.input(line_pin_right)
status_middle = GPIO.input(line_pin_middle)
status_left = GPIO.input(line_pin_left)

# Erkennen, ob das Leitungssuchmodul die Leitung erkennt.
if status_middle == 1:
'''
Steuern Sie den Roboter vorwärts
'''
print('vorwärts')
elif status_left == 1:
'''
Steuern Sie den Roboter, um nach links abzubiegen
'''
print('links')
elif status_right == 1:
'''
Steuern Sie den Roboter, um nach rechts abzubiegen
'''
print('richtig')
anders:
'''
Wenn die Linie nicht erkannt wird, stoppt der Roboter, Sie können den Roboter auch rückwärts fahren lassen.
'''
print('stopp')
if __name__ == '__main__':
erstellen()
während 1:
Lauf()
```
- Wenn Ihr Projekt die Linienüberwachungsfunktion verwenden muss, müssen Sie den obigen Code nicht neu schreiben.
Kopieren Sie einfach findline.py und move.py in den Ordner des Roboterprogrammservers in dasselbe wie Ihr eigenes Projekt.
Verwenden Sie dann im Ordner den folgenden Code, um die Linienpatrouillenfunktion zu verwenden:

```
Suchlinie importieren

findline.setup()

während 1:
findline.run()
```

- Der Grund, warum Sie move.py importieren müssen, ist, dass findline.py die Methode in move.py verwenden muss, um die Roboterbewegung zu steuern.
Wenn Sie andere Methoden verwenden, müssen Sie nur den entsprechenden Code in findline.py neu schreiben.


## 14 Machen Sie ein Polizeilicht oder ein atmendes Licht
xxxxx ggf. wird dies auch pulsierend genannt. 

### 14.1 Multi-Threading-Einführung
- In diesem Kapitel wird die Verwendung von Multi-Threading vorgestellt, um einige Effekte im Zusammenhang mit WS2812 LED-Leuchten zu erzielen.
Multithreading ist eine häufig verwendete Operation in Roboterprojekten.
Da Roboter hohe Anforderungen an die Echtzeitreaktion haben, versuchen Sie bei der Ausführung einer bestimmten Aufgabe, die Kommunikation des Haupt-Threads nicht zu blockieren.

- Multithreading ist vergleichbar mit der gleichzeitigen Ausführung mehrerer verschiedener Programme oder Aufgaben.
Multithreading hat folgende Vorteile:
- Durch die Verwendung von Threads können lang andauernde Aufgaben zur Verarbeitung in den Hintergrund gestellt werden.
- Um die Betriebseffizienz des Programms zu verbessern, verwenden die anschließende Echtzeit-Video- und OpenCV-Verarbeitung von Videoframes Multithreading, um die Bildrate erheblich zu erhöhen.
- Die gekapselte Multithreaded-Aufgabe ist bequemer aufzurufen, ähnlich wie die **10.3 non-blocking control method** ist die Verwendung der gekapselten Multithreaded-Steuerungsmethode.
- Wir verwenden die Threading-Bibliothek von Python, um Thread-bezogene Arbeit bereitzustellen.
Threads sind die kleinste Arbeitseinheit in einer Anwendung.
Die aktuelle Version von Python bietet keine Multi-Thread-Priorität, Thread-Gruppe und Thread können nicht gestoppt, ausgesetzt, fortgesetzt und unterbrochen werden.

### 14.2 Realisierung von Polizeilichtern / atmenden Lichtern
- Wir verwenden den folgenden Code, um eine Multithread-Steuerung von LED-Leuchten zu erreichen, und wenn sich die LED nicht ändert, halten Sie den Thread blockiert, um keine CPU-Ressourcen zu verschwenden.

- Die Methode wait() wird hier verwendet, um den Thread zu blockieren, ab der Erkenntnis, dass der Thread kontrolliert werden muss.

```
Importzeit
Importsystem
aus rpi_ws281x-Import *
Einfädeln importieren
'''
Verwenden Sie das Threading-Modul, um Threads zu erstellen, direkt von threading.Thread zu erben und
Überschreiben Sie dann die Methode __init__ und die Methode run.
'''
Klasse RobotLight(threading.Thread):
def __init__(self, *args, **kwargs):
'''
Hier initialisieren Sie einige Einstellungen zu LED-Leuchten.
'''
self.LED_COUNT = 16 # Anzahl der LED-Pixel.
self.LED_PIN = 12 # GPIO-Pin mit den Pixeln verbunden (18 verwendet PWM!).
self.LED_FREQ_HZ = 800000 # LED-Signalfrequenz in Hertz (normalerweise 800khz)
self.LED_DMA = 10 # DMA-Kanal zur Signalerzeugung (versuchen Sie 10)
self.LED_BRIGHTNESS = 255 # Auf 0 für dunkelste und 255 für hellste setzen
self.LED_INVERT = False # True, um das Signal zu invertieren (bei Verwendung von NPN-Transistor-Pegelverschiebung)
self.LED_CHANNEL = 0 # auf '1' gesetzt für GPIOs 13, 19, 41, 45 oder 53
'''
Stellen Sie die Helligkeit der drei RGB-Farbkanäle ein, hier muss nichts geändert werden, diese
Werte werdennach dem anschließenden Aufruf der Atemlichtfunktion automatisch eingestellt.
'''
self.colorBreathR = 0
self.colorBreathG = 0
self.colorBreathB = 0
self.breathSteps = 10
'''
Die Modusvariable 'none' bewirkt, dass der Thread blockiert und hängt, das Licht ändert sich nicht;
'Polizei' ist ein Polizeilichtmodus, rot und blau blinken abwechselnd;
'Atem' Atemlicht, können Sie die angegebene Farbe einstellen.
'''
self.lightMode = 'none' #'none' 'polizei' 'breath'

# Erstellen Sie ein NeoPixel-Objekt mit entsprechender Konfiguration.
self.strip = Adafruit_NeoPixel(self.LED_COUNT, self.LED_PIN, self.LED_FREQ_HZ,

self.LED_DMA, self.LED_INVERT, self.LED_BRIGHTNESS,
selbst.LED_CHANNEL)
# Bibliothek initialisieren (muss vor anderen Funktionen einmal aufgerufen werden).
self.strip.begin()
super(RobotLight, self).__init__(*args, **kwargs)
self.__flag = threading.Event()
self.__flag.clear()

# Definieren Sie Funktionen, die LEDs auf verschiedene Weise animieren.
def setColor(self, R, G, B):
'''
Stellen Sie die Farbe aller Lichter ein.
'''

Farbe = Farbe(int(R),int(G),int(B))
für i im Bereich (self.strip.numPixels()):
self.strip.setPixelColor(i, Farbe)
self.strip.show()
def setSomeColor(self, R, G, B, ID):
'''
Stellen Sie die Farbe einiger Lampen ein, die ID ist das Array der Seriennummer dieser Lampe.
'''
Farbe = Farbe (int(R),int(G),int(B))
#print(int(R),' ',int(G),' ',int(B))
für i in ID:
self.strip.setPixelColor(i, Farbe)
self.strip.show()
def Pause (selbst):
'''
Rufen Sie diese Funktion auf, setzen Sie __flag auf False, blockieren Sie den Thread.
'''
self.lightMode = 'none'
self.setColor(0,0,0)
self.__flag.clear()
def Lebenslauf(selbst):
'''
Rufen Sie diese Funktion auf, setzen Sie __flag auf True, um den Thread zu starten.
'''
self.__flag.set()
def Polizei (selbst):
'''
Rufen Sie diese Funktion auf, um den Polizeilichtmodus einzuschalten.
'''
self.lightMode = 'Polizei'
self.resume()

def polizeiVerarbeitung(selbst):
'''
Die spezifische Realisierung des Polizeilichtmodus.
'''
while self.lightMode == 'Polizei':
'''
Blau blinkt 3 mal
'''
für i im Bereich (0,3):
self.setSomeColor(0,0,255,[0,1,2,3,4,5,6,7,8,9,10,11])
time.sleep(0.05)
self.setSomeColor(0,0,0,[0,1,2,3,4,5,6,7,8,9,10,11])
time.sleep(0.05)
if self.lightMode != 'Polizei':
brechen
time.sleep(0.1)
'''
Rot blinkt 3 mal.
'''
für i im Bereich (0,3):
self.setSomeColor(255,0,0,[0,1,2,3,4,5,6,7,8,9,10,11])
time.sleep(0.05)
self.setSomeColor(0,0,0,[0,1,2,3,4,5,6,7,8,9,10,11])
time.sleep(0.05)
time.sleep(0.1)
def Atem (selbst, R_input, G_input, B_input):
'''
Rufen Sie diese Funktion auf, um den Atemlichtmodus einzuschalten, Sie müssen drei eingeben
Parameter, nämlich die Helligkeit der drei RGB-Farbkanäle, als Farbe, wenn die
Helligkeit der Atemlampe ist maximal.
'''
self.lightMode = 'Atem'
self.colorBreathR = R_input
self.colorBreathG = G_input
self.colorBreathB = B_input
self.resume()

def AtemBearbeitung(selbst):
'''
Spezifische Realisierungsmethode der Atemlampe.
'''
while self.lightMode == 'Atem':
'''
Alle Lichter werden allmählich heller.
'''
für i im Bereich (0,self.breathSteps):
if self.lightMode != 'Atem':
brechen
self.setColor(self.colorBreathR*i/self.breathSteps,
self.colorBreathG*i/self.breathSteps,
self.colorBreathB*i/self.breathSteps)
time.sleep(0.03)
'''
Alle Lichter werden dunkler.
'''
für i im Bereich (0,self.breathSteps):
if self.lightMode != 'Atem':
brechen
self.setColor(self.colorBreathR-(self.colorBreathR*i/self.breathSteps),
self.colorBreathG-(self.colorBreathG*i/self.breathSteps),
self.colorBreathB-(self.colorBreathB*i/self.breathSteps))
time.sleep(0.03)

def lightChange (selbst):
'''
Diese Funktion wird verwendet, um die auszuführende Aufgabe auszuwählen.
'''
if self.lightMode == 'none':
selbst.pause()
elif self.lightMode == 'Polizei':
self.policeProcessing()
elif self.lightMode == 'Atem':
self.breathProcessing()
def run(selbst):
'''
Funktionen für Multithreading-Aufgaben
'''
während 1:
self.__flag.wait()
self.lightChange()
passieren

if __name__ == '__main__':
RL=RobotLight() # Instanziieren Sie das Objekt, das das LED-Licht steuert.
RL.start() # Thread starten.
'''
Starten Sie den Atemlichtmodus und stoppen Sie ihn nach 15 Sekunden.
'''
RL.Atem(70,70,255)
time.sleep(15)
RL.pause()

'''
2 Sekunden pausieren.
'''
Zeit.Schlaf(2)
'''
Starten Sie den Polizeilichtmodus und stoppen Sie nach 15 Sekunden.
'''
RL.Polizei()
time.sleep(15)
RL.pause()
```

### 14.3 Warnlichter oder atmende Lichter in anderen Projekten

- Wenn Ihr Projekt LED-Lichter für Warnlichter oder Atemlichter verwenden muss, müssen Sie den obigen Code nicht neu schreiben, kopieren Sie einfach robotLight.py in den Ordner des Roboterprogrammservers.
Im Ordner verwenden Sie dann den folgenden Code to Warnlicht oder Atemlicht verwenden:

```
robotLight importieren
RL=robotLight.RobotLight() # Instanziieren des Objekts, das das LED-Licht steuert
RL.start() # Thread starten

'''
Atemlichtmodus starten und nach 15 Sekunden stoppen
'''
RL.Atem(70,70,255)
time.sleep(15)
RL.pause()

'''
2 Sekunden pausieren
'''
Zeit.Schlaf(2)
'''
Starten Sie den Polizeilichtmodus und stoppen Sie nach 15 Sekunden
'''
RL.Polizei()
time.sleep(15)
RL.pause()
```

## 15 Echtzeit-Videoübertragung

- Echtzeit-Video und OpenCV-Funktion sind die Vorteile des Raspberry Pi-Roboters.
Dieses Kapitel stellt die Methode des Echtzeit-Videos vor.
Tatsächlich gibt es viele Möglichkeiten, die von der Raspberry Pi-Kamera gesammelten Bilder über das Netzwerk auf andere Geräte zu übertragen.
Der Roboter verwendet das Open-Source-Projekt [flask-video-streaming](https://github.com/miguelgrinberg/flask-video-streaming "Github: Flask-video-streaming") von [Github](https://github .com/miguelgrinberg/flask-video-streaming "Github: Flask-video-streaming") der MIT-Open-Source-Vereinbarung können Sie auf den Link klicken, um den Quellcode des Projekts anzuzeigen.

- Der Grund für die Auswahl ist [flask-video-streaming](https://github.com/miguelgrinberg/flask-video-streaming "Github: Flask-video-streaming").
Diese Lösung ist die bequemste und effizienteste der vielen Lösungen, die wir ausprobiert haben.
Der Teil, der sich auf OpenCV bezieht, hat auch eine gute Schnittstelle, um ihn als Multithread-Verarbeitung umzuschreiben.

- Da dieses Projekt die Verwendung von Flask und verwandten abhängigen Bibliotheken erfordert, enthält unser Installationsskript für die Robotersoftware den Inhalt der Installation dieser abhängigen Bibliotheken.
Wenn Ihr Raspberry Pi das Installationsskript der Robotersoftware nicht ausgeführt hat, müssen Sie den folgenden Befehl zur Installation verwenden.

```
sudo pip3 installiere flasche
sudo pip3 installflakon_cors
```

- Dieses Kapitel stellt nicht zuerst den OpenCV-Teil vor, sondern stellt nur vor, wie das Echtzeitbild der Raspberry Pi-Kamera auf anderen Geräten angezeigt wird.

- Zuerst [flask-video-streaming](https://github.com/miguelgrinberg/flask-video-streaming "Github: Flask-video-streaming") dieses Projekt auf den Raspberry Pi herunterladen.
Sie können es von Clone auf GitHub herunterladen oder auf Ihren Computer herunterladen und dann an den Raspberry Pi übergeben.
Der Download-Befehl über die Raspberry Pi-Konsole lautet wie folgt:

```
sudo git clon https://github.com/miguelgrinberg/flask-video-streaming.git
```

- Führen Sie nach dem Herunterladen oder Übertragen von Flask-Video-Streaming im Raspberry Pi die app.py im Flask-Video-Streaming aus:

```
CD-Flasche-Video-Streaming
sudo python3 app.py
```

- Wenn Sie sudo python3flakon-video-streaming / app.py nicht zum Ausführen verwenden, wird ein Fehler angezeigt, dass \* .jpeg nicht gefunden wird.

- Öffnen Sie den Browser auf dem Gerät im selben lokalen Netzwerk wie der Raspberry Pi (**wir verwenden Google Chrome zum Testen**) und geben Sie die IP-Adresse des Raspberry Pi sowie die Videostreaming-Portnummer ein: **5000* * in der Adressleiste, wie im folgenden Beispiel gezeigt:

```
192.168.3.157:5000
```

- Jetzt können Sie die vom Raspberry Pi erstellte Seite im Browser Ihres Computers oder Mobiltelefons sehen.
Beachten Sie, dass der Standardbildschirm nicht vom Bildschirm der Raspberry Pi-Kamera stammt, sondern drei digitale Bilder, die zyklisch abgespielt werden 1, 2, 3.

- Wenn sich Ihre Seite einloggen kann und ein Bild von 1 \ 2 \ 3 Zahlen in einer Schleife abspielt, bedeutet dies, dass die Flaschen-bezogenen Programme normal laufen.
Als nächstes können Sie einige Änderungen an app.py vornehmen, damit der Raspberry Pi in Echtzeit auf der Seite angezeigt werden kann. Kamera-Bildschirm.

```
sudo nano app.py
```

- Hier verwenden wir Nano, das mit Raspbian geliefert wird, um app.py zum Bearbeiten in der Konsole zu öffnen.
Da es sich nur um einige Operationen zum Kommentieren und Löschen von Kommentaren handelt, müssen keine anderen IDEs zum Bearbeiten verwendet werden.

- Nach dem Öffnen der IDE kommentieren wir den Code aus:

```
if os.environ.get('KAMERA'):
Kamera = import_module('camera_' + os.environ['CAMERA']).Kamera
anders:
aus Kamera importieren Kamera
```

- Sie können diese Codezeilen auskommentieren, indem Sie # am Anfang der Codezeile eingeben, oder Sie können am Anfang und Ende des gesamten Codes ein ''' schreiben, um einen bestimmten Code auskommentieren zu können.
Der relevante Code nach der Änderung lautet wie folgt:

```
# if os.environ.get('KAMERA'):
# Kamera = import_module('camera_' + os.environ['CAMERA']).Kamera
# anders:
# aus dem Kameraimport Kamera
oder
'''
if os.environ.get('KAMERA'):
Kamera = import_module('camera_' + os.environ['CAMERA']).Kamera
anders:
aus Kamera importieren Kamera
'''
```

- Entfernen Sie schließlich die Auskommentierung des Codes, der die Kamera von camera_pi importiert,

```
# from camera_pi import Kamera
```

delete vor #, beachten Sie, dass hier nach dem # ein Leerzeichen steht, und auch delete, der geänderte Code lautet wie folgt:

from camera_pi import Kamera

- Nachfolgend der vollständige Code der modifizierten app.py:

```
#!/usr/bin/env python
von importlib import import_module
Importieren von OS
aus Kolbenimport Flask, render_template, Response
# Kameratreiber importieren'''
if os.environ.get('KAMERA'):
Kamera = import_module('camera_' + os.environ['CAMERA']).Kamera
anders:
aus Kamera importieren Kamera
'''

# Raspberry Pi Kameramodul (erfordert Picamera-Paket)
from camera_pi import Kamera

app = Flasche(__name__)

@app.route('/')
def-index():
"""Videostreaming-Startseite."""
return render_template('index.html')

def-Gen (Kamera):
"""Videostreaming-Generatorfunktion."""
während Wahr:
frame = camera.get_frame()
Ertrag (b'--frame\r\n'
b'Inhaltstyp: Bild/jpeg\r\n\r\n' + Rahmen + b'\r\n')

@app.route('/video_feed')
def video_feed():
"""Videostreaming-Route. Fügen Sie dies in das src-Attribut eines img-Tags ein."""
Antwort zurückgeben (gen (Kamera ()),
mimetype='multipart/x-mixed-replace; Grenze=Rahmen')

if __name__ == '__main__':
app.run(host='0.0.0.0', threaded=True)
```

- Drücken Sie nach der Bearbeitung **STRG+X**, um die Bearbeitung zu starten, und fragen Sie, ob die Änderungen gespeichert werden sollen, drücken Sie **Y** und **Eingabe**, nachdem Sie die Änderungen gespeichert haben.
- Dann können Sie app.py ausführen:

```
sudo app.py
```

- Öffnen Sie den Browser auf dem Gerät im selben lokalen Netzwerk wie der Raspberry Pi (**wir verwenden Google Chrome zum Testen**) und geben Sie die IP-Adresse des Raspberry Pi sowie die Videostreaming-Portnummer ein: **5000* * in der Adressleiste, wie im folgenden Beispiel gezeigt:

```
192.168.3.157:5000
```

- Jetzt können Sie die vom Raspberry Pi erstellte Seite im Browser Ihres Computers oder Mobiltelefons sehen.
Nach erfolgreichem Laden zeigt die Seite das Echtzeitbild der Raspberry Pi-Kamera an.
- Diese Funktion verwendet Projekte von GitHub [flask-video-streaming](https://github.com/miguelgrinberg/flask-video-streaming "GitHub: Flask-video-streaming").


## 16 Automatische Hindernisvermeidung
- Das Ultraschallmodul dieses Produkts kann sich nur mit der Kamera nach oben und unten bewegen, und die linke und rechte Bewegung kann sich nur mit dem Körper des Körpers drehen und kann sich relativ zum Körper nicht nach links und rechts bewegen, daher die Hindernisvermeidungsfunktion dieses Roboters ist relativ einfach, solange sich ein Hindernis vor ihm befindet. Biegen Sie nach links ab und ziehen Sie sich zurück, wenn das Hindernis zu nahe ist, und bewegen Sie sich vorwärts, wenn das Hindernis weit entfernt ist oder kein Hindernis vorhanden ist.

- Die automatische Hindernisvermeidungsfunktion basiert auf dem Ultraschall-Entfernungsmodul. Bevor Sie Ihr Projekt schreiben, müssen Sie zuerst **ultra.py** **RPIservo.py** einfügen und **move.py** dorthin kopieren Dateiverzeichnis als Ihr Projekt und verwenden Sie dann den folgenden Code, um die automatische Hindernisvermeidungsfunktion zu verwenden.

```
ultra importieren
Import verschieben
Importzeit
Adafruit_PCA9685 importieren
RPIservo importieren

# Holen Sie sich die Anfangsdaten von PWM
def num_import_int(initial):
globaler r
mit open(thisPath+"/RPIservo.py") als f:
für Zeile in f.readlines():
if(line.find(initial) == 0):
r=Linie
begin=len(list(initial))
snum=r[beginnen:]
n=int(snum)
zurück n

scGear = RPIservo.ServoCtrl() # Servosteuerung
scanNum = 3 # Das Auto scannt die drei Teile davor, nämlich links, Mitte und rechts, dh 1 steht für links, 2 für Mitte und 3 für rechts
scanPos = 1 # Die nächste vom Auto zu scannende Position, der Wert kann 1, 2 und 3 sein, entsprechend links, Mitte und rechts
scanDir = 1 # Die Richtung des Autoscans, 1 ist ganz links, -1 ist ganz rechts
scanList = [] # Zeichnen Sie die Entfernung von Hindernissen in drei Richtungen auf, die gescannt werden
scanServo = 1 # Pan-Tit-Servonummer
scanRange = 100 # Der Bereich des vom Servo gescannten Winkels
rangeKeep = 0.7 # Threshold, wenn es kleiner ist, dreht sich; wenn es größer ist, geh zurück

# Servowinkel initialisieren
pwm = Adafruit_PCA9685.PCA9685()
pwm.set_pwm_freq(50)

pwm0_direction = 1
pwm0_init = num_import_int('init_pwm0 = ')
pwm0_max = 520
pwm0_min = 100
pwm0_pos = pwm0_init

pwm1_direction = 1
pwm1_init = num_import_int('init_pwm1 = ')
pwm1_max = 520
pwm1_min = 100
pwm1_pos = pwm1_init

pwm2_direction = 1
pwm2_init = num_import_int('init_pwm2 = ')
pwm2_max = 520
pwm2_min = 100
pwm2_pos = pwm2_init

während Wahr:
# Das Pan-Tit-Servo dreht sich nach links, in die Mitte und nach rechts und verwendet Ultraschall, um die Entfernung von Hindernissen zu scannen und aufzuzeichnen
if scanPos == 1:
pwm.set_pwm(scanServo, 0, pwm1_init + scanRange)
time.sleep(0.3)
scanList[0] = ultra.checkdist()
elif scanPos == 2:
pwm.set_pwm(scanServo, 0, pwm1_init)
time.sleep(0.3)
scanList[1] = ultra.checkdist()
elif scanPos == 3:
pwm.set_pwm(scanServo, 0, pwm1_init - scanRange)
time.sleep(0.3)
scanList[2] = ultra.checkdist()

scanPos += scanDir

# Wenn der Scanwinkel nicht innerhalb des eingestellten Bereichs liegt
if scanPos > scanNum oder scanPos < 1:
# Ändern Sie die Scanrichtung
if scanDir == 1: scanDir = -1
elif scanDir == -1: scanDir = 1
# Gescannten Standort wiederherstellen
scanPos += scanDir*2
drucken(scanList)

# Wenn der Abstand zum nächsten Hindernis vor Ihnen kleiner als der Schwellenwert ist
if min(scanList) < rangeKeep:
# Wenn das nächste Hindernis links ist
wennscanList.index(min(scanList)) == 0:
# Dann rechts abbiegen
scGear.moveAngle(2, -30)
# Wenn das nächste Hindernis direkt vor dir ist
elif scanList.index(min(scanList)) == 1:
# Sehen Sie sich den Wert links und rechts an, um zu bestimmen, welcher größer ist
if scanList[0] < scanList[2]:
# Volles Seitenruder nach rechts und bewegen
scGear.moveAngle(2, -45)
anders:
# Ansonsten volles Seitenruder nach links und bewegen
scGear.moveAngle(2, 45)
# Wenn das nächste Hindernis rechts ist
elif scanList.index(min(scanList)) == 2:
# Dann biegen Sie links ab
scGear.moveAngle(2, 30)
if max(scanList) < rangeKeep oder min(scanList) < rangeKeep/3:
move.motor_lef(1, 1, 80)
move.motor_right(1, 1, 80)
# Wenn der Abstand zum nächstgelegenen Hindernis größer als die Schwelle ist, fährt das Auto rückwärts
anders:
move.motor_left(1, 0, 80)
move.motor_right(1, 0, 80)
```

## 17 OpenCV Multithreading wird zur Verarbeitung von Videoframes verwendet

- Die OpenCV-Funktion basiert auf dem GitHub-Projekt [flask-video-streaming](https://github.com/miguelgrinberg/flask-video-streaming "GitHub: Flask-video-streaming"), wir haben die Kamera_opencv.py geändert um OpenCV-bezogene Operationen durchzuführen.


### 17.1 Single-Thread-Verarbeitung von Videoframes

- Zuerst stellen wir den Prozess der Single-Thread-Verarbeitung von Videoframes vor.
Beginnen wir mit einem einfachen, damit Sie verstehen, warum OpenCV mehrere Threads verwendet, um Videoframes zu verarbeiten.
Der Prozess der Single-Thread-Verarbeitung von Videoframes ist wie folgt:

![schematisch](images/102.jpg "schematisch")

- Prozesserklärung:
Holen Sie sich zuerst einen Frame von der Kamera und verwenden Sie dann OpenCV, um den Inhalt dieses Frames zu analysieren.
Nach Abschluss der Analyse werden die zu zeichnenden Informationen generiert, z generierten Zeichnungsinformationen und zeigen schließlich den verarbeiteten und gezeichneten Rahmen auf der Seite an.

- Ein solcher Verarbeitungsfluss führt dazu, dass jeder zu sammelnde Frame auf die Verarbeitung des OpenCV-bezogenen Prozesses wartet.
Nachdem dieser Frame angezeigt wurde, kann der zweite Frame zur Verarbeitung und Analyse gesammelt werden, um ihn abnormal hängen zu lassen.


### 17.2 Multi-Thread-Verarbeitung von Videoframes

- Als nächstes wird der Prozess der Multi-Thread-Verarbeitung von Videoframes eingeführt:
![schematisch](images/103.jpg "schematisch")

- Prozesserklärung: Um die Framerate zu verbessern, trennen wir die Analyseaufgabe des Videoframes vom Prozess der Erfassung und Anzeige und platzieren es in einem Hintergrundthread, um Zeichnungsinformationen auszuführen und zu generieren.

- Wir ändern den kompletten Code von camera_opencv.py mit zu vielen Threads wie folgt:
(Dieser Code dient nur als Referenz des Multi-Threading-Prinzips, und die OpenCV-Funktion wird zu Demonstrationszwecken intuitiv gelöscht:)

```
Importieren von OS
CV2 importieren
aus base_camera importiere BaseCamera
numpy als np importieren
Datum/Uhrzeit importieren
Importzeit
machen es ungewöhnlich stecken.
Einfädeln importieren
Imutils importieren

Klasse CVThread(threading.Thread):
'''
Diese Klasse wird verwendet, um die OpenCV-Analyse von Videoframes im Hintergrund zu verarbeiten. Weitere grundlegende Nutzungsprinzipien der Multithreaded-Klasse finden Sie in 14.2
'''
def __init__(self, *args, **kwargs):
self.CVThreading = 0

super(CVThread, self).__init__(*args, **kwargs)
self.__flag = threading.Event()
self.__flag.clear()

def mode (self, imgInput):
'''
Diese Methode wird für eingehende Videoframes verwendet, die verarbeitet werden müssen
'''
self.imgCV = imgInput
self.resume()

def elementDraw(self,imgInput):
'''
Zeichne Elemente in das Bild
'''
zurück imgInput

def doOpenCV(self, frame_image):
'''
Fügen Sie hier den von OpenCV zu verarbeitenden Inhalt hinzu
'''
selbst.pause()

def Pause (selbst):
'''
Blockiere den Thread und warte auf den nächsten Frame
'''
self.__flag.clear()
self.CVThreading = 0

def Lebenslauf(selbst):
'''
Setzen Sie den Thread fort
'''
self.__flag.set()

def run(selbst):
'''
Videoframes im Hintergrundthread verarbeiten
'''
während 1:
self.__flag.wait()
self.CVThreading = 1
self.doOpenCV(self.imgCV)


Klasse Kamera (BaseCamera):
video_source = 0

def __init__(selbst):
if os.environ.get('OPENCV_CAMERA_SOURCE'):
Camera.set_video_source(int(os.environ['OPENCV_CAMERA_SOURCE']))
super(Kamera, selbst).__init__()

@statische Methode
def set_video_source(source):
Camera.video_source = source

@statische Methode
def-frames():
Kamera = cv2.VideoCapture(Camera.video_source)
wenn nicht camera.isOpened():
raise RuntimeError('Kamera konnte nicht gestartet werden.')
'''
Instanziierung CVThread()
'''
cvt = CVThread()
cvt.start()

während Wahr:
# aktuellen Frame lesen
img = camera.read()

wenn cvt.CVThreading:
'''
Wenn OpenCV Videoframes verarbeitet, überspringen
'''
passieren
anders:
'''
Wenn OpenCV nicht verarbeitet wirdWenn Sie Videoframes erstellen, geben Sie dem Videoframe-Verarbeitungsthread einen neuen Videoframe und setzen Sie den Verarbeitungsthread fort
'''
cvt.mode(img)
cvt.resume()
'''
Elemente auf dem Bildschirm zeichnen
'''
img = cvt.elementDraw(img)

# als JPEG-Bild codieren und zurückgeben
yield cv2.imencode('.jpg', img)[1].tobytes()
```

- Das obige ist das Codeprinzip der Verwendung von Multithreading zur Verarbeitung von OpenCV.
Die folgende Einführung in bestimmte Funktionen von OpenCV überspringt die Erläuterung von Multi-Threading und stellt die Methode von OpenCV zur Verarbeitung von Videoframes direkt vor.


## 18 OpenCV Lernen Sie, OpenCV zu verwenden

- Die Echtzeit-Videoübertragungsfunktion stammt aus dem Open-Source-Projekt von Github der MIT-Open-Source-Vereinbarung Kolben-Video-Streaming.

- Bereiten Sie zunächst zwei .py-Dateien im gleichen Ordner auf dem Raspberry Pi vor.
Der Code lautet wie folgt:

- app.py
```
#!/usr/bin/env python3

von importlib import import_module
Importieren von OS
aus Kolbenimport Flask, render_template, Response

from camera_opencv import Kamera

app = Flasche(__name__)

def-Gen (Kamera):
während Wahr:
frame = camera.get_frame()
Ertrag (b'--frame\r\n'
b'Inhaltstyp: Bild/jpeg\r\n\r\n' + Rahmen + b'\r\n')

@app.route('/')
def video_feed():
Antwort zurückgeben (gen (Kamera ()),
mimetype='multipart/x-mixed-replace; Grenze=Rahmen')


if __name__ == '__main__':
app.run(host='0.0.0.0', threaded=True)
```

- base_camera.py
```
Importzeit
Einfädeln importieren
Versuchen:
aus Greenlet importieren getcurrent als get_ident
außer ImportError:
Versuchen:
aus Thread-Import get_ident
außer ImportError:
aus _Thread-Import get_ident

Klasse CameraEvent(Objekt):
'''
Eine ereignisähnliche Klasse, die allen aktiven Clients signalisiert, wenn ein neuer Frame verfügbar ist.
'''
def __init__(selbst):
self.events = {}

def warte(selbst):
'''
Wird vom Thread jedes Clients aufgerufen, um auf den nächsten Frame zu warten.
'''
ident = get_ident()
wenn ident nicht in self.events:
# das ist ein neuer Kunde
# einen Eintrag dafür im self.events dict hinzufügen
# jeder Eintrag hat zwei Elemente, ein threading.Event() und einen Zeitstempel
self.events[ident] = [threading.Event(), time.time()]
return self.events[ident][0].wait()

def set(selbst):
'''
Wird vom Kamera-Thread aufgerufen, wenn ein neuer Frame verfügbar ist.
'''
jetzt = time.time()
entfernen = Keine
für ident, Ereignis in self.events.items():
falls nicht event[0].isSet():
# Wenn das Ereignis dieses Clients nicht festgelegt ist, dann setze es
# auch den zuletzt gesetzten Zeitstempel auf jetzt aktualisieren
event[0].set()
Ereignis[1] = jetzt
anders:
# Wenn das Ereignis des Kunden bereits festgelegt ist, bedeutet dies, dass der Kunde
# hat einen vorherigen Frame nicht verarbeitet
# Wenn das Ereignis länger als 5 Sekunden gesetzt bleibt, nehmen Sie an
# der Client ist weg und entferne ihn
wenn jetzt - Ereignis[1] > 5:
entfernen = identifizieren

wenn entfernen:
del self.events[entfernen]

def klar(selbst):
'''
Wird von jedem Client-Thread aufgerufen, nachdem ein Frame verarbeitet wurde.
'''
self.events[get_ident()][0].clear()

Klasse BaseCamera(Objekt):
thread = None # Hintergrundthread, der Frames von der Kamera liest
frame = None # aktueller Frame wird hier vom Hintergrundthread gespeichert
last_access = 0 # Zeitpunkt des letzten Clientzugriffs auf die Kamera
Ereignis = KameraEreignis()

def __init__(selbst):
'''
Starten Sie den Hintergrundkamera-Thread, wenn er noch nicht ausgeführt wird.
'''
wenn BaseCamera.thread None ist:
BaseCamera.last_access = time.time()

# Hintergrundrahmen-Thread starten
BaseCamera.thread = threading.Thread(target=self._thread)
BaseCamera.thread.start()

# warten bis Frames verfügbar sind
während self.get_frame() None ist:
zeit.schlaf(0)

def get_frame(self):
'''
Gibt das aktuelle Kamerabild zurück.
'''
BaseCamera.last_access = time.time()

# auf ein Signal vom Kamera-Thread warten
BaseCamera.event.wait()
BaseCamera.event.clear()

Zurück BaseCamera.frame

@statische Methode
def-frames():
'''
Generator, der Frames von der Kamera zurückgibt.
'''
raise RuntimeError('Muss von Unterklassen implementiert werden.')

@classmethod
def_thread(cls):
'''
Kamera-Hintergrundthread.
'''
print('Kamera-Thread wird gestartet.')
frame_iterator = cls.frames()

für Frame in frames_iterator:
BaseCamera.frame = Rahmen
BaseCamera.event.set() # Signal an Clients senden
zeit.schlaf(0)

# wenn keine Kunden nach Frames gefragt haben
# die letzten 10 Sekunden dann den Thread stoppen
if time.time() - BaseCamera.last_access > 10:
frame_iterator.close()
print('Kamera-Thread wegen Inaktivität angehalten.')
brechen
BaseCamera.thread = Keine
```

- Wenn Sie das Folge-Tutorial verwenden, um eine bestimmte OpenCV-bezogene Funktion zu entwickeln, müssen Sie nur die entsprechende camera_opencv.py im selben Ordner wie diese app.py und base_camera.py ablegen und dann in der Raspberry Pi-Konsole ausführen einfach app.py.

- Öffnen Sie den Browser mit einem Gerät im selben lokalen Netzwerk wie der Raspberry Pi, geben Sie die IP-Adresse des Raspberry Pi in die Adressleiste ein und greifen Sie auf Port 5000 zu.
NSDie Adresse wird im folgenden Beispiel angezeigt:

```
192.168.3.161:5000
```


## 19 Verwenden von OpenCV zur Realisierung von Farberkennung und -verfolgung


### 19.1 Farberkennung und Farbraum
- Informationen zur Entwicklungsvorbereitung und zum Betrieb der OpenCV-Funktion finden Sie unter **18**.

- Erstellen Sie camera_opencv.py in dem Ordner, in dem sich app.py und base_camera.py in **18** befinden.
Der Code zur OpenCV-Farbverfolgungsfunktion, der in diesem Kapitel vorgestellt wird, ist in camera_opencv.py geschrieben.

- Aus Sicherheitsgründen steuert diese Routine nicht die Motor- oder Servobewegung und gibt nur OpenCV-Berechnungsergebnisse aus.

- Wir verwenden OpenCV zur Farberkennung mit dem HSV-Farbraum.
Bevor wir den Code einführen, müssen wir zuerst den Farbraum verstehen und warum wir den HSV-Farbraum anstelle des üblicheren RGB-Farbraums für die Farberkennung verwenden.

- **Farbraum**:
Der Farbraum ist die Art und Weise, wie Farben organisiert sind.
Mit Hilfe von Farbraum und Tests für physikalische Geräte können feste analoge und digitale Darstellungen von Farben erhalten werden.
Der Farbraum kann einfach durch zufällige Auswahl einiger Farben definiert werden. Das Pantone-System nimmt beispielsweise nur einen bestimmten Satz von Farben als Muster und definiert dann den Namen und den Code für jede Farbe; es kann auch auf einer strengen mathematischen Definition basieren, wie beispielsweise Adobe RGB, SRGB.

- **RGB-Farbraum**:
RGB verwendet eine additive Farbmischmethode, da sie das Verhältnis verschiedener "Lichter" zur Erzeugung von Farben beschreibt.
Das Licht wird kontinuierlich von Dunkel überlagert, um Farbe zu erzeugen.
RGB beschreibt die Werte von rotem, grünem und blauem Licht.
RGBA ist das Hinzufügen eines Alphakanals zu RGB, um einen Transparenzeffekt zu erzielen.
Übliche Farbräume, die auf dem RGB-Modus basieren, sind sRGB, Adobe RGB und Adobe Wide Gamut RGB.

- **HSV-Farbraum**:
HSV (Hue: Hue, Saturation: Saturation, Brightness; Value), auch bekannt als HSB (B bezieht sich auf Helligkeit) wird häufig von Künstlern verwendet, da im Vergleich zum Begriff der Addition und Subtraktion die Verwendung von Farbton, Sättigung und anderen Konzepten Farbe zu beschreiben ist natürlicher und intuitiver.
HSV ist eine Variante des RGB-Farbraums, sein Inhalt und seine Farbskala sind eng mit seinem Quell-RGB-Farbraum verwandt

- Die Verwendung des HSV-Farbraums in der Farberkennungsfunktion von OpenCV kann das Erkennungsergebnis genauer machen, weniger vom Umgebungslicht beeinflusst werden und es ist sehr bequem, den Farbbereich zu definieren.
Denn was Sie bei der Farberkennung suchen, ist nicht eine bestimmte Farbe, sondern eine bestimmte Farbpalette. Verwenden Sie daher für die Farberkennung den HSV-Farbraum, der eher den Gewohnheiten des menschlichen Auges entspricht.


### 19.2 Prozess der Farberkennung und -verfolgung

- Wir können diese Funktion verwenden, um das Servo zu steuern, damit die Kamera auf ein bestimmtes Farbobjekt zielt. Der allgemeine Vorgang ist wie folgt.

![schematisch](images/104.jpg "schematisch")


### 19.3 Spezifischer Code

- camera_opencv.py

```
Importieren von OS
CV2 importieren
aus base_camera importiere BaseCamera
numpy als np importieren
'''
Zielfarbe festlegen, HSV-Farbraum
'''
colorUpper = np.array([44, 255, 255])
colorLower = np.array([24, 100, 100])

Schriftart = cv2.FONT_HERSHEY_SIMPLEX

Klasse Kamera (BaseCamera):
video_source = 0

def __init__(selbst):
if os.environ.get('OPENCV_CAMERA_SOURCE'):
Camera.set_video_source(int(os.environ['OPENCV_CAMERA_SOURCE']))
super(Kamera, selbst).__init__()

@statische Methode
def set_video_source(source):
Camera.video_source = source

@statische Methode
def-frames():
Kamera = cv2.VideoCapture(Camera.video_source)
wenn nicht camera.isOpened():
raise RuntimeError('Kamera konnte nicht gestartet werden.')

während Wahr:
# aktuellen Frame lesen
img = camera.read() #Das von der Kamera aufgenommene Bild abrufen

hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV) #Konvertieren Sie aufgenommene Bilder in den HSV-Farbraum
mask = cv2.inRange(hsv, colorLower, colorUpper) #Traversieren Sie die Farben im Zielfarbbereich im HSV-Farbraum und verwandeln Sie diese Farbblöcke in Masken
mask = cv2.erode(mask, None, iterations=2) #Korrosion von kleinen Maskenstücken (Rauschen) im Bild wird klein (kleine Farbstücke oder Rauschen verschwinden)
mask = cv2.dilate(mask, None, iterations=2) #Aufblasen und die Größe der großen Maske ändern, die im vorherigen Schritt auf ihre ursprüngliche Größe reduziert wurde
cnts = cv2.findContours(mask.copy(), cv2.RETR_EXTERNAL,
cv2.CHAIN_APPROX_SIMPLE)[-2] #Finde ein paar Masken im Bild
Mitte = Keine
if len(cnts) > 0: #Wenn die Anzahl der ganzen Masken im Bild größer als eins ist
'''
Finden Sie die Koordinaten des Mittelpunkts des Objekts der Zielfarbe und die Größe des Objekts im Bild
'''
c = max(cnts, key=cv2.contourArea)
((box_x, box_y), Radius) = cv2.minEnclosingCircle(c)
M = cv2.Momente(c)
center = (int(M["m10"] / M["m00"]), int(M["m01"] / M["m00"]))
X = int(box_x)
Y = int(box_y)
'''
Holen Sie sich die Mittelpunktkoordinaten des Zielfarbobjekts und der Ausgabe
'''
print('Zielfarbe ausObjekt erkannt')
print('X:%d'%X)
print('Y:%d'%Y)
drucken('-------')

'''
Schreiben Sie Text auf den Bildschirm: Ziel erkannt
'''
cv2.putText(img,'Ziel erkannt',(40,60), Schriftart, 0.5,(255,255,255),1,cv2.LINE_AA)
'''
Zeichnen Sie einen Rahmen um das Zielfarbobjekt
'''
cv2.rectangle(img,(int(box_x-radius),int(box_y+radius)),
(int(box_x+radius),int(box_y-radius)),(255,255,255),1)
anders:
cv2.putText(img,'Zielerkennung',(40,60), Schriftart, 0.5,(255,255,255),1,cv2.LINE_AA)
print('Kein Zielfarbobjekt erkannt')

# als JPEG-Bild codieren und zurückgeben
yield cv2.imencode('.jpg', img)[1].tobytes()
```
- Sie können die Farbe einstellen, die Sie erkennen möchten, indem Sie colorUpper und colorLower ändern.
Hier ist zu beachten, dass normal Der H-Wert (Farbton) des HSV-Farbraums beträgt 0-360, aber in OpenCV reicht der H-Wert von 0-180.


### 19.4 HSV-Farbkomponentenbereich in OpenCV


HSV\Farbe | Schwarz | Grau | Weiß | Rot | Orange | Gelb | Grün | Cyan | Blau | Violett
------ | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | ----- | -----
H_min | 0 | 0 | 0 | 0\|156 | 11 | 26 | 35 | 78 | 100 | 125
H_max | 180 | 180 | 180 | 10\|180 | 25 | 34 | 77 | 99 | 124 | 155
S_min | 0 | 0 | 0 | 43 | 43 | 43 | 43 | 43 | 43 | 43
S_max | 255 | 43 | 30 | 255 | 255 | 255 | 255 | 255 | 255 | 255
V_min | 0 | 46 | 221 | 46 | 46 | 46 | 46 | 46 | 46 | 46
V_max | 46 | 220 | 255 | 255 | 255 | 255 | 255 | 255 | 255 | 255

## 20 Maschinenlinienverfolgung basierend auf OpenCV

### 20.1 Sichtlinieninspektionsprozess

![schematisch](images/105.jpg "schematisch")


- Informationen zur Entwicklungsvorbereitung und zum Betrieb der OpenCV-Funktion finden Sie unter **18**.

- Erstellen Sie camera_opencv.py in dem Ordner, in dem sich app.py und base_camera.py in **18** befinden. Der Code für die in diesem Kapitel vorgestellte OpenCV-Sichtlinienverfolgungsfunktion ist in camera_opencv.py geschrieben.

- Aus Sicherheitsgründen steuert diese Routine nicht die Motor- oder Servobewegung und gibt nur OpenCV-Berechnungsergebnisse aus.


### 20.2 Spezifischer Code

```
Importieren von OS
CV2 importieren
aus base_camera importiere BaseCamera
numpy als np importieren
Importzeit
Einfädeln importieren
Imutils importieren

'''
Legen Sie die Farbe der Linie fest, 255 ist die weiße Linie, 0 ist die schwarze Linie
'''
lineColorSet = 255
'''
Stellen Sie die horizontale Position der Referenz ein, je größer der Wert, desto niedriger, aber nicht größer als die vertikale Auflösung
des Videos (Standard 480)
'''
linePos = 380

Klasse Kamera (BaseCamera):
video_source = 0
def __init__(selbst):
if os.environ.get('OPENCV_CAMERA_SOURCE'):
Camera.set_video_source(int(os.environ['OPENCV_CAMERA_SOURCE']))
super(Kamera, selbst).__init__()

@statische Methode
def set_video_source(source):
Camera.video_source = source

@statische Methode
def-frames():
Kamera = cv2.VideoCapture(Camera.video_source)
wenn nicht camera.isOpened():
raise RuntimeError('Kamera konnte nicht gestartet werden.')

während Wahr:
img = camera.read() #Das von der Kamera aufgenommene Bild abrufen
'''
Konvertieren Sie das Bild in Schwarzweiß und digitalisieren Sie es (der Wert jedes Pixels im Bild beträgt 255 .).
außer 0)
'''
img = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
retval, img = cv2.threshold(img, 0, 255, cv2.THRESH_OTSU)
img = cv2.erode(img, None, iterations=6) #Korrosionsminderung verwenden
colorPos = img[linePos] #Erhalte ein Array von Pixelwerten für linePos
Versuchen:
lineColorCount_Pos = np.sum(colorPos == lineColorSet) #Erhalte die Anzahl der Pixel der Linienfarbe (Linienbreite)
lineIndex_Pos = np.where(colorPos == lineColorSet) #Erhalte die horizontale Position des Endpunkts der Linie in der linePos-Linie
'''
Verwenden Sie die Endpunktposition und die Linienbreite, um die Position des Mittelpunkts der Linie zu berechnen
'''
left_Pos = lineIndex_Pos[0][lineColorCount_Pos-1]
right_Pos = lineIndex_Pos[0][0]
center_Pos = int((left_Pos+right_Pos)/2)

print('Die Position des Mittelpunkts der Linie ist：%d'%center_Pos)
außer:
'''
Wenn keine Linie erkannt wird, führt eine Linienbreite über 0 zu einem Fehler, sodass Sie wissen, dass keine Linie erkannt wurde
'''
center_Pos = 0
print('Keine Linie erkannt')
'''
Zeichnen Sie eine horizontale Referenzlinie
'''
cv2.line(img,(0,linePos),(640,linePos),(255,255,64),1)
if center_Pos:
'''
Wenn eine Linie erkannt wird, zeichnen Sie den Mittelpunkt der Linie
'''
cv2.line(img,(center_Pos,linePos+300),(center_Pos,linePos-300),(255,255,64),1)

# als JPEG-Bild codieren und zurückgeben
yield cv2.imencode('.jpg', img)[1].tobytes()
```


## 21 Spracherkennung

- Dieses Produkt verwendet die Funktion der Verwendung von Sprache, um die Bewegung des Roboters zu steuern.
Die von uns verwendete Methode stammt aus der [SpeechRecognition](https://github.com/Uberi/speech_recognition "Github: Speech_recognition") des Github-Projekts.
Unser Installationsskript installiert dieses Programm und die zugehörigen abhängigen Bibliotheken automatisch.
Wenn Sie unser Installationsskript nicht verwenden, installieren Sie bitte andere abhängige Bibliotheken, bevor Sie es manuell installieren:

```
sudo apt-get install -y swig
sudo apt-get install -y portaudio19-dev python3-all-dev python3-pyaudio
sudo pip3 installiere pyaudio
sudo apt-get install -y flac
sudo wget https://sourceforge.net/projects/cmusphinx/files/sphinxbase/5prealpha/sphinxbase-5prealpha.tar.gz/download -O sphinxbase.tar.gz
sudo wget https://sourceforge.net/projects/cmusphinx/files/pocketsphinx/5prealpha/pocketsphinx-5prealpha.tar.gz/download -O pocketphinx.tar.gz
sudo tar -xzvf sphinxbase.tar.gz
sudo tar -xzvf pocketphinx.tar.gz
cd sphinxbase-5prealpha/ && ./configure -enable-fixed && make && sudo make install
sudo pip3 installiere pocketphinx
cd pocketphinx-5prealpha/ && ./configure && make && sudo make install
```

- Nach der Installation der abhängigen Bibliotheken können Sie SpeechRecognition installieren:

```
sudo pip3 installieren Spracherkennung
```

- Dieses Produkt ist auch mit einem antriebsfreien Mikrofon ausgestattet, das direkt über eine USB-Schnittstelle verwendet werden kann.

- Obwohl die Spracherkennung der Spracherkennung nicht sehr genau ist, ist sie sehr einfach zu bedienen.


### 21.1 Spezifischer Code

```
Spracherkennung als sr importieren

#Audio vom Mikrofon erhalten
r = sr.Erkenner()
# devicde_index ist der Index des Audio-Eingabegeräts, wenn Sie ihn nicht angeben, wird das Mikrofon als Audio verwendet
Quelle standardmäßig.
# sample_rate legt die Anzahl der pro Sekunde gesammelten Samples fest. Wenn Sie sie nicht angeben, wird dies automatisch eingestellt
durch das Mikrofon des Systems bestimmt.
# Wenn die Einstellung höher ist, erhalten Sie eine bessere Audioqualität, aber es wird die Erkennungsgeschwindigkeit verlangsamen und die CPU von
manche Himbeertorte kann nicht mithalten
mit sr.Microphone(device_index=2, sample_rate=48000) als Quelle:
r.record(source, duration=2) # 2 Sekunden Audio werden ab der Audioquelle aufgenommen
audio = r.listen(source) # Erhalten Sie die einzelne Phrase, die von der Quelle aufgenommen wurde

Versuchen:
# Verwenden Sie CMU Sphinx, um Audio zur Spracherkennung auszuführen
Befehl = r.recognize_sphinx(
Audio,
# Schlüsselwörter angeben, jedes Schlüsselwort ist ein Tupel mit der Länge 2
# Das erste Element des Tupels ist das Schlüsselwort und das zweite Element ist die Empfindlichkeit des Erkenners für dieses Schlüsselwort（0~1）
keyword_entries=[
('vorwärts', 1.0),
('rückwärts', 1.0),
('links', 1.0),
('richtig', 1.0),
('Stopp', 1.0)
]
)
drucken (Befehl)
# Wenn das angegebene Schlüsselwort nicht erkannt wird, wird eine UnknowValueError-Ausnahme ausgegeben
außer sr.UnknowValueError:
print('sag nochmal')
```


## 22 Radarscan

- Der Roboter steuert mit dem Pan-Tilt-Ultraschall den Scan nach rechts, der Bereich ist ein Halbkreis mit einem Radius von mehr als 1 Meter und die Daten werden visualisiert.

- Die Radarscanning-Funktion ist auf Basis des Ultraschallmoduls implementiert.
In Ihrem Projekt müssen Sie ultra.py an den Direktor Ihres Projekts verschieben, bevor Sie den Code schreiben.

### 22.1 Spezifischer Code
```
ultra importieren
Adafruit_PCA9685 importieren
Importzeit

pwm = Adafruit_PCA9685.PCA9685()
pwm.set_pwm_freq(50)

def num_import_int(initial): #Rufen Sie diese Funktion auf, um Daten aus der '.txt'-Datei zu importieren
globaler r
mit open(thisPath+"/RPIservo.py") als f:
für Zeile in f.readlines():
if(line.find(initial) == 0):
r=Linie
begin=len(list(initial))
snum=r[beginnen:]
n=int(snum)
zurück n

# Initialisieren Sie die Daten des Schwenk-Neige-Servos
pwm0_direction = 1
pwm0_init = num_import_int('init_pwm0 = ')
pwm0_max = 520
pwm0_min = 100
pwm0_pos = pwm0_init

scan_speed = 3 # Scan-Rotationsgeschwindigkeit
result = [] # Speichert die gescannten Daten

# Von rechts nach links scannen
if pwm0_direction:
pwm0_pos = pwm0_max
pwm.set_pwm(1, 0, pwm0_pos)
time.sleep(0.8)

während pwm0_pos > pwm0_min:
pwm0_pos -= scan_speed
pwm.set_pwm(1, 0, pwm0_pos)
# Ermitteln Sie den Abstand der Hindernisse
dist = ultra.checkdist()
wenn dist > 20:
fortsetzen
# Berechnen Sie den Winkel des aktuell gescannten Hindernisses und rechts vor dem Roboter
theta = 180 - (pwm0_pos - 100) / 255
result.append([dist, theta])
anders:
pwm0_pos = pwm0_min
pwm.set_pwm(1, 0, pwm0_pos)
time.sleep(0.8)

während pwm0_pos < pwm0_max:
pwm0_pos += scan_speed
pwm.set_pwm(1, 0, pwm0_pos)
dist = ultra.checkdist()
wenn dist > 20:
fortsetzen
theta = (pwm_pos - 100) / 2,55
result.append([dist, theta])
pwm.set_pwm(1, 0, pwm0_init)
drucken (Ergebnis)
```

## 23 Einen WLAN-Hotspot auf dem Raspberry Pi erstellen

- Die Methode zum Einschalten des WIFI-Hotspots in unserem Roboterprodukt verwendet ein Projekt von GitHub [create_ap](https://github.com/oblique/create_ap "GitHub: create_ap").
Unser Installationsskript installiert dieses Programm und die zugehörigen abhängigen Bibliotheken automatisch.
Wenn Sie unser Installationsskript nicht ausgeführt haben, können Sie mit dem folgenden Befehl [create_ap] installieren (https://github.com/oblique/create_ap "GitHub: create_ap"):

```
sudo git clone https://github.com/oblique/create_ap.git cd
create_ap
sudo machen installieren
```
- Installieren Sie verwandte abhängige Bibliotheken:
```
sudo apt-get install -y util-linux procps hostapd iproute2 iw haveged dnsMaske
```

- Vor dem Einschalten des Hotspots kann Ihr Raspberry Pi nicht mit dem WIFI verbunden werden und das WIFI-Modul kann nicht ausgeschaltet werden. Wenn Sie die Hotspot-Funktion testen, müssen Sie also die erforderlichen Peripheriegeräte für den Raspberry Pi anschließen.

- Unter normalen Umständen, wenn das Roboterprogramm beim Einschalten nicht mit dem WIFI verbunden ist, wird der Hotspot automatisch eingeschaltet.
Sie können Ihr Telefon oder Ihren Computer verwenden, um nach dem WIF mit dem Namen **Adeept** zu suchen.
Das Standardpasswort lautet **12345678**. Sobald die Verbindung erfolgreich ist.
Sie können sich mit einem Browser bei **192.168 .12.1: 5000** anmelden, um die WEB-Anwendung zur Steuerung des Roboters zu öffnen.

- Wenn Ihr Raspberry Pi mit Peripheriegeräten verbunden ist und Sie die Fähigkeit des Raspberry Pi testen möchten, Hotspots einzuschalten.
Sie können auf das WIFI-Symbol in der oberen rechten Ecke des Desktops des Raspberry Pi klicken, auf den Namen des verbundenen WIFIs klicken, auf Vergessen klicken und WIFI nie ausschalten. Wenn es bereits ausgeschaltet ist, müssen Sie es ausschalten An.

- Wenn das WIFI-Modul des Raspberry Pi eingeschaltet und mit keinem bekannten Netzwerk verbunden ist, können Sie auf der Konsole folgenden Befehl eingeben, um das WIFI einzuschalten:

```
sudo create_ap wlan0 eth0 Adeept 12345678
```

- **Adeept** ist der Name des WIFI-Hotspots, **12345678** ist das Passwort des WIFI-Hotspots.


## 24 GUI-abhängiges Element unter Microsoft Windows installieren  

- Unsere alten Versionen von Roboterprogrammen bieten alle ein Desktop-GUI-Programm zur Steuerung des Roboters.
Das GUI-Programm ist in Python geschrieben, aber diese Methode verwendet einen höheren Schwellenwert und einen höheren Schwierigkeitsgrad und wird für Anfänger nicht empfohlen.

- Dieses GUI-Programm ist vorerst nur für das Windows-System geeignet.
Es ist im Client-Verzeichnis des Roboter-Softwarepakets enthalten und heißt im Allgemeinen GUI.py.


### 24.1 GUI-Abhängigkeiten installieren

- Python3 installieren:
- Wir müssen Python auf dem Computer installieren, um unser PC-seitiges Programm auszuführen.
Der Code dieses Produkts wurde mit Python3 entwickelt und getestet, daher müssen wir Python3.7 oder höher herunterladen, um mögliche Kompatibilitätsfehler zu vermeiden.

- [Python3-Downloadadresse](https://www.python.org/downloads/windows/ "Python3 für Microsoft Windows")

- Doppelklicken Sie nach dem Herunterladen von Python auf das Installationspaket, um es zu installieren.

- Achten Sie bei der Installation von Python darauf, Python zu PATH hinzufügen auszuwählen.

- Installieren Sie Numpy:

- NumPy ist ein grundlegendes Softwarepaket für wissenschaftliches Rechnen in Python, und OpenCV muss die zugehörigen Funktionen verwenden.

- Drücken Sie die **Win+R-Taste**, geben Sie cmd ein und klicken Sie auf OK, um das CMD zu öffnen.
- Geben Sie Folgendes ein, um numpy zu installieren:
```
pip3 installiere numpy
```
- Nach der Eingabe drücken Sie die Eingabetaste, um den Download und die Installation von numpy zu starten.

- OpenCV installieren:

- Die Methode zur Installation von numpy ist dieselbe.

- Geben Sie nach dem Öffnen von CMD Folgendes ein:
```
pip3 installiere opencv-contrib-python
```

- Nach der Eingabe **Entry** Starten Sie den Download und die Installation von opencv.

- Drücken Sie um zmq und pybase64 zu installieren:

- zmq und pybase64 sind Bibliotheken für Echtzeitvideo
- Geben Sie nach dem Öffnen von CMD Folgendes ein:
```
pip3 installieren zmq pybase64
```
- Drücken Sie nach der Eingabe **Eingabe**.
Beginnen Sie mit dem Herunterladen und Installieren von zmq und pybase64.


## 25 So wird die GUI verwendet

- Da das Web und die GUI nicht verbunden sind, müssen Sie server.py manuell ausführen, wenn Sie die GUI zur Steuerung des Roboterprodukts verwenden möchten.
(Die Methode entspricht der manuellen Ausführung von webserver.py, außer dass das Objekt in server.py geändert wird).

- Wenn server.py im Raspberry Pi erfolgreich ausgeführt wird, geben Sie die IP-Adresse des Raspberry Pi am GUI-Bedienterminal des PCs ein und klicken Sie dann auf Verbinden, um den Roboter zu steuern.

- Python-Lauffenster: Dieses Fenster wird jede GUI begleiten, wenn sie geöffnet wird.
Alle Laufzeitausnahmen werden hier angezeigt.
Wird dieses Fenster geschlossen, wird die GUI verlassen.
- Kamera-Videostreaming-Fenster: Zeigt das von der Kamera aufgenommene Bild an.
Je nach Produkttyp kann die Fenster-Rendering-Methode unterschiedlich sein, und einige Produkte können auch mit diesem Fenster interagieren.

- Eingabefeld IP-Adresse: Geben Sie hier die IP-Adresse des Raspberry Pi ein.
Wenn Sie auf Verbinden klicken, kann sich die GUI mit dem Raspberry Pi verbinden.
Status- und Verbindungsstatusanzeigeleiste des Raspberry Pi:
Zeigt einige Hardwareinformationen des Raspberry Pi und den aktuellen Verbindungsstatus an.

- Mobile Steuerung:

- **Vorwärts**: Steuern Sie den Roboter, um sich vorwärts zu bewegen; die Tastenkombination ist **W**.
- **Rückwärts**: Steuern Sie den Roboter, um sich rückwärts zu bewegen; die Tastenkombination ist **S**.
- **Links**: Steuern Sie den Roboter, um nach links abzubiegen; die Tastenkombination ist **A**.
- **Rechts**: Steuern Sie den Roboter, um nach rechts abzubiegen; die Tastenkombination ist **D**.
- Roboterarm- und Kamerasteuerung (aufgrund unterschiedlicher Layouts unterscheiden sich die Tastenkombinationen hier von WEB-Anwendungen):
- **Up**: Steuern Sie die Kamera, um sich nach oben zu bewegen; die Tastenkombination ist **I**.
- **Nach unten**: Steuern Sie die Kamera, um sich nach unten zu bewegen; die Tastenkombination ist **K**.
- \: Kontrolle der Drehung des mechanischen Spannarms;die Tastenkombination ist **U**.
- /: Kontrollieren Sie die Drehung des mechanischen Armspannfutters; die Tastenkombination ist **O**.
- **Grab**: Kontrollieren Sie die Drehung des mechanischen Armspannfutters; die Tastenkombination ist **J**.
- **Loose**: Kontrollieren Sie die Drehung des mechanischen Spannfutters; die Tastenkombination ist **L**.
- **<--**: Steuern Sie den mechanischen Arm nach vorne; die Tastenkombination ist **Q**.
- **-->**: Steuern Sie den mechanischen Arm nach hinten; die Tastenkombination ist **E**.
- **Home**: Steuern Sie alle Servos, um in die neutrale Position zurückzukehren; die Tastenkombination ist **H**.

## 26 Steuerung der WS2812 LED über die GUI

- Sie können das Programm mit einer von Ihnen selbst geschriebenen grafischen Oberfläche verwenden, um mit dem Raspberry Pi auf anderen Geräten zu kommunizieren, um den Zweck der Steuerung des Raspberry Pi zu erreichen.

- Die in diesem Kapitel vorgestellte GUI-Programmiermethode wird vollständig von der Python-Sprache übernommen, insbesondere wird die Tkinter-Bibliothek verwendet.

- Tkinter ist die Standard-GUI-Bibliothek von Python.
Python verwendet Tkinter, um schnell GUI-Anwendungen zu erstellen.
Da Tkinter in das Python-Installationspaket integriert ist, können Sie die Tkinter-Bibliothek importieren, solange Python installiert ist, und IDLE ist auch in Tkinter geschrieben.
Für einfache grafische Oberfläche kommt Tkinter immer noch damit zurecht.

- Wir verwenden die Socket-Bibliothek, um zwischen Geräten zu kommunizieren.
Socket wird auch "Socket" genannt.
Anwendungen senden normalerweise Anfragen an das Netzwerk oder beantworten Netzwerkanfragen über den "Socket", damit der Prozess zwischen dem Host oder einem Computer kommunizieren kann.

- In diesem Kapitel nehmen wir die Fernbedienung der LED-Leuchten als Beispiel, denn fast alle unsere Roboter sind mit WS 2812 LED-Modulen ausgestattet.
Dieses einfachere Beispiel hilft auch Anfängern zu verstehen, wie das Desktop-GUI-Programm funktioniert, um mit dem Raspberry Pi zu kommunizieren.

- Bereit zum Brennen des Raspbian Raspberry Pi, können Sie sich auf **das 9-Modul-WS2812-LED-Licht** für verwandte abhängige Bibliotheken und Verbindungsmethoden beziehen.
Wenn Sie keinen Motor HAT verwenden, verbinden Sie einfach den Signalport (IN) von WS2812 LED mit GPIO12 (BCM 18) von Raspberry Pi.

- Für die detaillierte Definition von Raspberry Pi-Pins können Sie diesen Link zum Verständnis sehen: [Raspberry Pi Pinout](https://pinout.xyz/ "Raspberry Pi Pinout").

- Installieren Sie die Python-Bibliothek, die zur Steuerung des WS2812-LED-Lichts verwendet wird.
Wenn es nicht installiert wurde oder das Roboterinstallationsskript nicht ausgeführt wurde, können Sie es mit dem folgenden Befehl in der Raspberry Pi-Konsole installieren:

```
sudo pip3 installieren rpi_ws281x
- Wir werden den Raspberry Pi als Server und den PC als Client verwenden.
- Das Programm des Servers im Raspberry Pi sieht wie folgt aus:
'''
Diese beiden Bibliotheken werden verwendet, um WS2812 LED-Leuchten zu steuern
'''
aus rpi_ws281x-Import *
Argparse importieren

'''
Importieren Sie die Socket-Bibliothek, die für die TCP-Kommunikation verwendet werden soll
'''
Steckdose importieren
'''
Einige Einstellungen in Bezug auf LED-Leuchten stammen aus der WS281X-Routine
Quellcode: https://github.com/rpi-ws281x/rpi-ws281x-python/
'''
LED_COUNT = 24
LED_PIN = 18
LED_FREQ_HZ = 800000
LED_DMA = 10
LED_HELLIGKEIT = 255
LED_INVERT = Falsch
LED_CHANNEL = 0

'''
Argumente verarbeiten
'''
parser = argparse.ArgumentParser()
parser.add_argument('-c', '--clear', action='store_true', help='Anzeige beim Beenden löschen')
args = parser.parse_args()

'''
Erstellen Sie ein NeoPixel-Objekt mit entsprechender Konfiguration.
'''
Streifen = Adafruit_NeoPixel(LED_COUNT, LED_PIN, LED_FPEQ_HZ, LED_DMA, LED_INVERT, LED_BRIGHTNESS, LED_CHANNEL)
'''
Initialisieren Sie die Bibliothek
'''
strip.begin()
'''
Als nächstes folgt die Konfiguration in Bezug auf die TCP-Kommunikation, wobei PORT die definierte Portnummer ist, die Sie frei wählen können
von 0-65535 wird empfohlen, die Nummer nach 1023 zu wählen, die mit der Portnummer übereinstimmen muss
vom Client im PC definiert
'''
HOST = ''
ANSCHLUSS = 10223
BUFSIZ = 1024
ADDR = (HOST, PORT)

tcpSerSock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
tcpSerSock.setsockopt(socket.SOL_SOCKET, socket.SO_REUSEADDR,1)
tcpSerSock.bind(ADDR)
tcpSerSock.listen(5)

'''
Beginnen Sie, die Client-Verbindung abzuhören, nachdem die Client-Verbindung erfolgreich war, empfangen Sie die gesendeten Informationen
vom Kunden
'''
tcpCliSock, addr = tcpSerSock.accept()

während Wahr:
Daten = ''

'''
Informationen vom Kunden erhalten
'''
data = str(tcpCliSock.recv(BUFSIZ).decode())
wenn nicht daten:
fortsetzen

'''
Schalten Sie das Licht ein, wenn der Informationsinhalt eingeschaltet ist
Wenn der Informationsinhalt ausgeschaltet ist, schalten Sie das Licht aus
'''
elif 'on' == Daten:
für i im Bereich (strip.numPixels()):
strip.setPixelColor(i, Farbe(255, 0, 255))
Strip-Show()
elif 'off' == Daten:
für i im Bereich (strip.numPixels()):
strip.setPixelColor(i, Farbe(0, 0, 0))
Strip-Show()
'''
Drucken Sie schließlich die empfangenen Daten aus und hören Sie die nächste Nachricht des Clients weiter an
'''
Drucken (Daten)
```

- Das Programm des Clients im PC sieht wie folgt aus:

```
'''
Importieren Sie die Socket-Bibliothek, die für die TCP-Kommunikation verwendet werden soll
'''
aus Socket-Import *
'''
Python verwendet Tkinter, um schnell GUI-Anwendungen zu erstellen und sie beim Importieren zu instanziieren
'''
tkinter als tk importieren

def Lichter_on():
'''
Rufen Sie diese Methode auf, um das Licht-an-Kommando 'on' zu senden
'''
tcpClicSock.send(('on').encode())
def Lichter_aus():
'''
Rufen Sie diese Methode auf, um den Licht-Aus-Befehl 'off' zu senden
'''
tcpClicSock.send(('off').encode())
'''
Geben Sie hier die IP-Adresse des Raspberry Pi ein
'''
SERVER_IP = '192.168.3.35'

'''
Als nächstes folgt die Konfiguration in Bezug auf die TCP-Kommunikation, wobei PORT eine definierte Portnummer ist, die Sie frei wählen können
von 0-65535 wird empfohlen, die Nummer nach 1023 zu wählen, die mit der Portnummer übereinstimmen muss
vom Server im Raspberry Pi defined definiert
'''
SERVER_PORT = 10223
BUFSIZ = 1024
ADDR = (SERVER_IP, SERVER_PORT)
tcpClicSock = socket(AF_INET, SOCK_STREAM)
tcpClicSock.connect(ADDR)
'''
Das Folgende ist der GUI-Teil
'''
root = tk.Tk() # Definiere ein Fenster
root.title('Lichter') # Fenstertitel
root.geometry('175x55')# Die Größe des Fensters, das mittlere x ist der englische Buchstabe x
root.config(bg='#000000') # Definiere die Hintergrundfarbe des Fensters

'''
Verwenden Sie die Button-Methode von Tkinter, um eine Schaltfläche zu definieren. Die Schaltfläche befindet sich im Root-Fenster. Der Name der Schaltfläche ist 'ON'. Die
Textfarbe der Schaltfläche ist # E1F5FE. Die Hintergrundfarbe des Buttons ist # 0277BD. )Funktion
'''

btn_on = tk.Button(root, width=8, text='ON', fg='#E1F5FE', bg='#0277BD', command=lights_on)
'''
Wählen Sie einen Ort, um diese Schaltfläche zu platzieren
'''
btn_on.place(x=15, y=15)
'''
Die gleiche Methode definiert eine andere Taste, der Unterschied besteht darin, dass der Text über der Taste auf 'OFF' geändert wird.
Beim Drücken der Taste wird die Funktion lights_off() aufgerufen
'''
btn_off = tk.Button(root, width=8, text='OFF', fg='#E1F5FE', bg='#0277BD', command=lights_off)
btn_off.place(x=95, y=15)

'''
Endlich die Nachrichtenschleife öffnen
'''
root.mainloop()
```

- Wir führen das Programm zuerst im Raspberry Pi aus und öffnen dann das Programm auf dem PC (zuerst den Server und dann den Client ausführen).
- Klicken Sie auf 'ON', das Licht leuchtet und 'on' wird im Terminal des Raspberry Pi gedruckt, was anzeigt, dass das Programm erfolgreich ausgeführt wird.


### 27 Echtzeit-Videoübertragung basierend auf OpenCV


- In diesem Kapitel wird die Echtzeit-Videoübertragung vorgestellt, mit der die von der Kamera gesammelten Bilder in Echtzeit an andere Orte übertragen werden können, um Bilder anzuzeigen oder sie zur Verarbeitung der maschinellen Bildverarbeitung an den Host-Computer weiterzugeben.

- Die Softwarefunktionen dieses Tutorials basieren auf opencv, numpy, zmq (Zero MQ lesen) und base64 Bibliotheken.
Bevor Sie den Code schreiben, müssen Sie diese Bibliotheken installieren.

```
pip3 install opencv-contrib-python numpy zmq pybase64
```

- In diesem Tutorial verwendet die Hardware hauptsächlich einen PC und einen Raspberry Pi mit installierter Kamera, da sie gleichzeitig die Installationsmethoden verwandter Bibliotheken auf der Windows-Plattform und der Linux-Plattform vorstellen kann.

- OpenCV ist eine Open-Source-Computer-Vision-Bibliothek. Im Linux-System können Sie im Terminal eingeben:

```
sudo apt-get install -y libopencv-dev python3-opencv
```

- Im Windows-System können Sie es installieren, indem Sie die .whl-Datei von opencv herunterladen, oder Sie können den folgenden Befehl im Terminal verwenden, um OpenCV zu installieren:

```
pip3 installiere opencv-contrib-python
```

- NumPy ist ein grundlegendes Softwarepaket für wissenschaftliche Berechnungen mit Python.
Unter Linux installieren Sie numpy, indem Sie im Terminal **sudo pip3 install numpy** eingeben:

- Unter Windows installieren Sie numpy, indem Sie **pip3 install numpy** in der Befehlszeile (cmd) eingeben (muss python3.x im Voraus installieren).

- zmq und base64 werden hier für die Frame-Übertragung und die Frame-Encoding bzw. -Dekodierung verwendet
Projekt.
Geben Sie unter Linux **sudo pip3 install zmq pybase64** zur Installation ein und unter Windows **pip3 install zmq pybase64** zur Installation.
- Lassen Sie uns nach der Installation der entsprechenden Bibliotheken das Programm des Video-Sendeendes erklären.
Das Python-Programm RPiCam.py wird verwendet, um die Bilder von der Kamera zu sammeln und die gesammelten Bilder für das empfangende Ende des Videos zu kodieren.
Also legen wir RPiCam.py in den Raspberry Pi und führen es aus.

- RPiCam.py:
```
'''
Importieren Sie zuerst die erforderlichen Bibliotheken. Oben finden Sie eine spezifische Einführung in diese Bibliotheken
'''
CV2 importieren
zmq importieren
base64 importieren
Pikamera importieren
von picamera.array importieren PiRGBArray

'''
Hier müssen wir die IP-Adresse des Videoempfängers (die IP-Adresse des PCs) eingeben
'''
IP = '192.168.3.11'

'''
Dann initialisieren Sie die Kamera, Sie können diese Parameter nach Ihren Bedürfnissen ändern
'''
Kamera = picamera.PiCamera()
Kamera.Auflösung = (640, 480)
Kamera.Framerate = 20
rawCapture = PiRGBArray(Kamera, Größe=(640, 480))

'''
Hier instanziieren wir das zmq-Objekt, das zum Senden des Frames verwendet wird, unter Verwendung des TCP-Kommunikationsprotokolls, wobei 5555 die Portnummer ist.
Die Portnummer kann angepasst werden, solange die Portnummer des Senders und des Empfängers gleich sind
'''

Kontext = zmq.Context()
footage_socket = context.socket(zmq.PAIR)
footage_socket.connect('tcp://%s:5555'%IP)
Drucken (IP)

'''
Als nächstes schleifen Sie, um Bilder von der Kamera zu sammeln, da wir eine Raspberry Pi-Kamera verwenden, also ist use_video_port True
'''
für Frame in camera.capture_continuous(rawCapture, format="bgr", use_video_port=True):

'''
Da die Funktion imencode () ein numpy-Array oder einen Skalar übergeben muss, um das Bild zu codieren
Hier konvertieren wir den gesammelten Frame in ein numpy-Array
'''
frame_image = frame.array
'''
Wir codieren den Frame in Stream-Daten und speichern ihn im Speicherpuffer
'''
encoded, buffer = cv2.imencode('.jpg', frame_image)
jpg_as_text = base64.b64encode(Puffer)
'''
Hier senden wir die Stream-Daten im Puffer durch base64-Codierung an das Video-Empfangsende
'''
footage_socket.send(jpg_as_text)

'''
Lösche den Stream in Vorbereitung auf den nächsten Frame
'''
rawCapture.truncate(0)
```

- Im Folgenden erklären wir das Programm auf der Empfängerseite.
Da die hier verwendeten Bibliotheken plattformübergreifend sind, kann PC.py auf einem Windows-Rechner oder einem anderen Linux-Rechner ausgeführt werden.

- PC.py :
```
'''
Importieren Sie zuerst die benötigten Bibliotheken
'''
CV2 importieren
zmq importieren
base64 importieren
numpy als np importieren
'''
Hier instanziieren wir das zmq-Objekt, das zum Empfangen des Frames verwendet wird
Beachten Sie, dass die Portnummer mit der des Absenders übereinstimmen muss
'''
Kontext = zmq.Context()
footage_socket = context.socket(zmq.PAIR)
footage_socket.bind('tcp://*:5555')

während Wahr:
'''
Empfangene Videobilddaten
'''
frame = footage_socket.recv_string()

'''
Entschlüsseln und im Cache speichern
'''

img = base64.b64decode(frame)
'''
Interpretiere einen Puffer als ein eindimensionales Array
'''
npimg = np.frombuffer(img, dtype=np.uint8)
'''
Dekodiere ein eindimensionales Array in ein Bild
'''
source = cv2.imdecode(npimg, 1)
'''
Bild anzeigen
'''
cv2.imshow("Stream", Quelle)
'''
Im Allgemeinen sollte waitKey () nach imshow () verwendet werden, um Zeit für das Zeichnen des Bildes zu lassen, andernfalls wird das Fenster
reagieren nicht mehr und das Bild kann nicht angezeigt werden.
'''
cv2.waitKey(1)
```

- Beim Ausführen des Programms führen wir zuerst RPiCam.py im Raspberry Pi und PC.py im PC aus, um das Echtzeitbild des Raspberry Pi im PC zu sehen.


## 28 OpenCV verwenden, um Videoframes auf dem PC zu verarbeiten

- Aufgrund der begrenzten Rechenleistung des Raspberry Pi kann unser OpenCV im Raspberry Pi nur bei der Umsetzung einfacher Funktionen wie Farberkennung und visueller Linieninspektion eine relativ hohe Bildrate garantieren.
Wenn wir komplexere Bildverarbeitungsfunktionen benötigen, müssen wir die zu analysierenden Videoframes zur Verarbeitung an das Gerät mit fortschrittlicher GPU senden und schließlich die verarbeiteten Ergebnisse an den Roboter senden, in dem sich der Raspberry Pi befindet, um die entsprechenden Schritte auszuführen Bedienung und die Bildverarbeitung des Raspberry Pi Roboters.
Die Fähigkeit ist stärker und erreicht so fortschrittlichere Funktionen.

- Wir können auf den Inhalt von **26** verweisen, um Videoframes an den Host-Computer zu senden, oder auf den Inhalt von **15** verweisen, damit der Raspberry Pi den Videostream auf einer Seite und den Host-Computer platzieren kann ruft den Videostream von der Seite ab, um den Videoframe zu analysieren.
- Der Inhalt dieses Kapitels basiert auf 26. Zuerst öffnen wir PC.py wie folgt:

```
'''
Importieren Sie zuerst die benötigten Bibliotheken
'''
CV2 importieren
zmq importieren
base64 importieren
numpy als np importieren
'''
Hier instanziieren wir das zmq-Objekt, das zum Empfangen des Frames verwendet wird
Beachten Sie, dass die Portnummer mit der des Absenders übereinstimmen muss
'''
Kontext = zmq.Context()
footage_socket = context.socket(zmq.PAIR)
footage_socket.bind('tcp://*:5555')

während Wahr:
'''
Empfangene Videobilddaten
'''
frame = footage_socket.recv_string()
'''
Entschlüsseln und im Cache speichern
'''
img = base64.b64decode(frame)
'''
Interpretiere einen Puffer als ein eindimensionales Array
'''
npimg = np.frombuffer(img, dtype=np.uint8)
'''
Dekodiere ein eindimensionales Array in ein Bild
'''
source = cv2.imdecode(npimg, 1)
'''
Bild anzeigen
'''
cv2.imshow("Stream", Quelle)
'''
Im Allgemeinen sollte waitKey () nach imshow () verwendet werden, um Zeit für das Zeichnen des Bildes zu haben, andernfalls wird das Fenster
reagieren nicht und das Bild kann nicht angezeigt werden
'''
cv2.waitKey(1)
```

- Nach source = cv2.imdecode (npimg, 1) können Sie OpenCV verwenden, um die Quelle zu verarbeiten, wie unten gezeigt
die Routine zum Binarisieren des Echtzeit-Videobildes vom Raspberry Pi mit dem Host-Computer:

```
'''
Importieren Sie zuerst die benötigten Bibliotheken
'''
CV2 importieren
zmq importieren
base64 importieren
numpy als np importieren
'''
Hier instanziieren wir das zmq-Objekt, das zum Empfangen des Frames verwendet wird
Beachten Sie, dass die Portnummer mit der des Absenders übereinstimmen muss
'''
Kontext = zmq.Context()
footage_socket = context.socket(zmq.PAIR)
footage_socket.bind('tcp://*:5555')

während Wahr:
'''
Empfangene Videobilddaten
'''
frame = footage_socket.recv_string()
'''
Entschlüsseln und im Cache speichern
'''
img = base64.b64decode(frame)'''
Interpretiere einen Puffer als ein eindimensionales Array
'''
npimg = np.frombuffer(img, dtype=np.uint8)
'''
Dekodiere ein eindimensionales Array in ein Bild
'''
source = cv2.imdecode(npimg, 1)
'''
Bild in Graustufen umwandeln
'''
source = cv2.cvtColor(source, cv2.COLOR_BGR2GRAY)
'''
Binäres Bild
'''
retval, source = cv2.threshold(source, 0, 255, cv2.THRESH_OTSU)
'''
Kleines Rauschen im Bild entfernen
'''
source = cv2.erode(source, None, iterations=6)
'''
Bild anzeigen
'''
cv2.imshow("Stream", Quelle)
'''
Im Allgemeinen sollte waitKey () nach imshow () verwendet werden, um Zeit für das Zeichnen des Bildes zu haben, andernfalls wird das Fenster
reagieren nicht und das Bild kann nicht angezeigt werden
'''
cv2.waitKey(1)
```


## 29 UART aktivieren

- UART ist ein häufiger verwendetes Kommunikationsprotokoll zwischen Geräten. Mit UART können Sie MCUs wie Arduino, STM32 oder ESP32 ermöglichen, mit dem Raspberry Pi zu kommunizieren, was Ihren Roboter leistungsfähiger machen kann.

- Bei einigen Raspberry Pis ist der standardmäßig aktivierte UART jedoch kein UART mit vollem Funktionsumfang, daher müssen Sie die folgenden Schritte ausführen, um den UART mit vollem Funktionsumfang zu aktivieren.
Die folgenden Teile stammen aus der offiziellen Dokumentation des Raspberry Pi [The Raspberry Pi UARTs](https://www.raspberrypi.com/documentation/computers/configuration.html "The Raspberry Pi UARTs").

- Die auf dem Raspberry Pis verwendeten SoCs haben zwei eingebaute UARTs, einen [PL011](https://developer.arm.com/documentation "PL011") und einen Mini-UART.
Sie werden mit unterschiedlichen Hardwareblöcken implementiert, haben also leicht unterschiedliche Eigenschaften. Beide sind jedoch 3,3-V-Geräte, was bedeutet, dass beim Anschluss an ein RS232- oder ein anderes System, das unterschiedliche Spannungspegel verwendet, besondere Vorsicht geboten ist.
Um die Spannungspegel zwischen den beiden Protokollen umzuwandeln, muss ein Adapter verwendet werden. Alternativ können 3,3-V-USB-UART-Adapter zu sehr günstigen Preisen erworben werden.

- Auf Raspberry Pis, die mit dem Wireless/Bluetooth-Modul ausgestattet sind (Raspberry Pi 3 und Raspberry Pi Zero W), ist der PL011 UART standardmäßig mit dem Bluetooth-Modul verbunden, während der Mini-UART als primärer UART verwendet wird und über ein Linux verfügt Konsole darauf.
Bei allen anderen Modellen wird der PL011 als primärer UART verwendet.

- Unter Linux-Geräten bezieht sich standardmäßig /dev/ttyS0 auf den Mini-UART und /dev/ttyAMA0 auf den PL011.
Der primäre UART ist der der Linux-Konsole zugewiesene, der wie oben beschrieben vom Raspberry Pi-Modell abhängt. Es gibt auch Symlinks:
/dev/serial0, das sich immer auf den primären UART bezieht (sofern aktiviert), und /dev/serial1, das sich ebenfalls immer auf den sekundären UART bezieht (sofern aktiviert).



### 29.1 Mini-UART und CPU-Kernfrequenz

- Die Baudrate des Mini-UART ist an die Kernfrequenz der VPU auf der VC4-GPU gekoppelt.
Dies bedeutet, dass sich mit der Variation der Kernfrequenz durch den VPU-Frequenzregler auch die Baudrate des Mini-UART ändert.
Dadurch ist der Mini-UART im Standardzustand nur eingeschränkt verwendbar.
Wenn der Mini-UART zur Verwendung als primärer UART ausgewählt ist, wird er standardmäßig deaktiviert. Um es zu aktivieren, fügen Sie enable_uart=1 zu config.txt hinzu.
Dadurch wird auch die Kernfrequenz auf 250 MHz festgelegt (es sei denn, force_turbo ist eingestellt, wenn sie auf die VPU-Turbofrequenz festgelegt wird).
Wenn der Mini-UART nicht der primäre UART ist, Sie ihn beispielsweise zum Verbinden mit dem Bluetooth-Controller verwenden, müssen Sie core_freq=250 zur config.txt hinzufügen, sonst funktioniert der Mini-UART nicht.

- Der Standardwert des enable_uart-Flags hängt von den tatsächlichen Rollen der UARTs ab, so dass, wenn ttyAMA0 dem Bluetooth-Modul zugewiesen ist, enable_uart standardmäßig auf 0 gesetzt ist.
Wenn der Mini-UART dem Bluetooth-Modul zugewiesen ist, wird enable_uart standardmäßig auf 1 gesetzt.
Beachten Sie, dass die Standardeinstellungen von enable_uart diese Regel weiterhin befolgen, wenn die UARTs mithilfe eines Gerätebaum-Overlays (siehe unten) neu zugewiesen werden.


### 29.2 Deaktivieren der Verwendung von Konsolen-UART durch Linux
- Bei einer Standardinstallation von Raspbian wird der primäre UART (serial0) der Linux-Konsole zugewiesen.
Wenn Sie den seriellen Port für andere Zwecke verwenden, muss dieses Standardverhalten geändert werden.
Beim Start überprüft systemd die Linux-Kernel-Befehlszeile auf Konsoleneinträge und verwendet die darin definierte Konsole.
Um dieses Verhalten zu stoppen, muss die Einstellung der seriellen Konsole aus der Befehlszeile entfernt werden.
- Dies kann mit dem [raspi-config-Dienstprogramm] (https://www.raspberrypi.com/documentation/computers/configuration.html "raspi-config-Dienstprogramm") oder manuell erfolgen.

```
sudo raspi-config
```

- Wählen Sie Option 5, **Schnittstellenoptionen**, dann Option P6, **Seriell** und wählen Sie **Nein**. Beenden Sie raspi-config.

- Um die Einstellungen manuell zu ändern, bearbeiten Sie die Kernel-Befehlszeile mit **sudo nano /boot/cmdline.txt**.
Suchen Sie den Konsoleneintrag, der auf das serial0-Gerät verweist, und entfernen Sie ihn, einschließlich der Baudrateneinstellung. Es sieht ungefähr so ​​aus wie **console=serial0,115200**.
Stellen Sie sicher, dass der Rest der Zeile gleich bleibt, da Fehler in dieser Konfiguration das Booten des Raspberry Pi stoppen können.

- Starten Sie den Raspberry Pi neu fürdie Änderung wirksam werden.


### 29.3 UART-Ausgabe auf GPIO-Pins

- Standardmäßig befinden sich die UART-Sende- und -Empfangspins auf GPIO 14 bzw. GPIO 15, die Pins 8 und 10 auf dem GPIO-Header sind.


### 29.4 UARTs und Gerätebaum

- Verschiedene UART Device Tree Overlay-Definitionen finden Sie im Kernel-Github-Baum.
Die zwei nützlichsten Overlays sind [disable-bt](https://github.com/raspberrypi/linux/blob/rpi-4.11.y/arch/arm/boot/dts/overlays/disable-bt-overlay.dts " disable-bt") und [miniuart-bt](https://github.com/raspberrypi/linux/blob/rpi-4.11.y/arch/arm/boot/dts/overlays/miniuart-bt-overlay.dts " miniuart-bt").

- disable-bt deaktiviert das Bluetooth-Gerät und stellt UART0/ttyAMA0 auf GPIOs 14 und 15 wieder her.
Es ist auch notwendig, den Systemdienst zu deaktivieren, der das Modem initialisiert, damit es den UART nicht verwendet: **sudo systemctl disable hciuart**.

- miniuart-bt schaltet die Bluetooth-Funktion von Raspberry Pi 3 und Raspberry Pi Zero W um, um den Mini-UART (ttyS0) zu verwenden, und stellt UART0/ttyAMA0 auf GPIOs 14 und 15 wieder her.
Beachten Sie, dass dies die maximal nutzbare Baudrate reduzieren kann (siehe Mini-UART-Einschränkungen unten).
Es ist auch erforderlich, **/lib/systemd/system/hciuart.service** zu bearbeiten und **ttyAMA0** durch **ttyS0** zu ersetzen, es sei denn, Sie haben ein System mit udev-Regeln, die /dev/serial0 und / erstellen. dev/seriell1. Verwenden Sie in diesem Fall stattdessen /dev/serial1, da es immer korrekt ist.
Wenn cmdline.txt den Alias ​​serial0 verwendet, um auf den für den Benutzer zugänglichen Port zu verweisen, ersetzt die Firmware ihn durch den entsprechenden Port, unabhängig davon, ob dieses Overlay verwendet wird oder nicht.

- Es gibt andere UART-spezifische Overlays im Ordner.
Weitere Informationen zu Gerätebaum-Overlays finden Sie unter **/boot/overlays/README** oder führen Sie **dtoverlay -h overlay-name** für Beschreibungen und Nutzungsinformationen aus.

- Vollständige Anweisungen zur Verwendung von Device Tree Overlays finden Sie auf [diese Seite] (https://www.raspberrypi.com/documentation/computers/configuration.html "diese Seite").
Kurz gesagt, fügen Sie der Datei **config.txt** eine Zeile hinzu, um Gerätebaum-Overlays zu aktivieren.
Beachten Sie, dass der **-overlay.dts**-Teil des Dateinamens entfernt wird.

```
...
dtoverlay=disable-bt
...
```

### 29.5 Relevante Unterschiede zwischen PL011 und Mini UART
- Der Mini-UART hat kleinere FIFOs.
In Kombination mit der fehlenden Flusskontrolle macht dies es anfälliger, bei höheren Baudraten Zeichen zu verlieren.
Er ist im Allgemeinen auch weniger leistungsfähig als der PL011, hauptsächlich aufgrund seiner Baudratenverbindung zur VPU-Taktgeschwindigkeit.

- Die besonderen Mängel des Mini-UART im Vergleich zum PL011 sind:
- Keine Brucherkennung
- Keine Erkennung von Framing-Fehlern
- Kein Paritätsbit
- Kein Empfangs-Timeout-Interrupt
- Keine DCD-, DSR-, DTR- oder RI-Signale

Weitere Dokumentation zum Mini-UART finden Sie im SoC-Peripheriedokument hier.

## 30 Steuerung Ihres PiCar-B mit einem Android-Gerät

- Wenn Sie den Roboter mit einem Mobiltelefon oder Tablet steuern möchten, empfehlen wir Ihnen zuerst, die WEB-Anwendung zur Steuerung des Roboters zu verwenden, da die WEB-Anwendung mehr Funktionen hat, Wartungen und Updates häufiger sind und vor allem die WEB-Anwendung kann plattformübergreifend sein.
Egal, ob Sie ein Android- oder iOS-System verwenden, solange Google Chrome installiert ist, können Sie den Roboter über die WEB-Anwendung steuern.
- Informationen zur Verwendungsmethode der WEB-Anwendung finden Sie unter **5 Verwenden der WEB-Anwendung zur Steuerung des Roboters**.
- Unsere alte Version des Roboterprogramms ist mit der Methode ausgestattet, die Handy-APP zur Steuerung zu verwenden, aber die Handy-APP unterstützt nur Android-Telefone und kann die Funktionen der Raspberry Pi-Kamera nicht verwenden.
Das dieser Funktion entsprechende Programm im Raspberry Pi ist **appserver.py**.
- Die Download-Adresse der mobilen APP finden Sie auf unserer offiziellen Website.
Die Installationsmethode ist die gleiche wie bei der normalen Handy-APP.
- Öffnen Sie die mobile App, geben Sie die IP-Adresse des Raspberry Pi in das IP-Adressfeld der mobilen App ein und geben Sie 10123 als Portnummer ein.
Klicken Sie auf: **Verbinden**

![Adeept App](./images/App1.jpg "Adeept App")

- Es ist zu beachten, dass die Portnummer bei Verwendung der WEB-Anwendung **5000** ist, die Portnummer bei Verwendung des GUI-Programms **10223** und die Portnummer bei Verwendung der mobilen APP **10123* ist. *.
- Der Controller auf der linken Seite kann den Roboter steuern, um sich vor und zurück, nach links und rechts zu bewegen, und der Controller auf der rechten Seite kann andere Bewegungen des Roboters steuern.
Sie können den spezifischen Vorgang ändern, indem Sie **appserver.py** bearbeiten.

![Adeept App](./images/App2.jpg "Adeept App")

## Abschluss

Durch die obigen Operationen auf Picar-B sollten Sie lernen, wie Sie die Python-Sprachprogrammierung verwenden, um die Arbeit von PiCar-B auf dem Raspberry Pi zu steuern, und auch, wie Sie ein PiCar-B zusammenbauen.

Wenn Sie Fragen zu diesem Produkt haben, kontaktieren Sie uns bitte per E-Mail oder Forum, wir werden Ihre Fragen innerhalb eines Werktages beantworten:

[support@adeept.com](mailto:support@adeept.com "support@adeept.com")  
[https://www.adeept.com/forum/](https://www.adeept.com/forum/ "https://www.adeept.com/forum/")  
Wenn Sie unsere anderen Produkte ausprobieren möchten, können Sie unsere Website besuchen:  
[www.adeept.com](https://www.adeept.com "www.adeept.com")  
Weitere Produktinformationen finden Sie unter:  
[https://www.adeept.com/learn/](https://www.adeept.com/learn/ "https://www.adeept.com/learn/")  
Für weitere Produkt-Video-Updates besuchen Sie bitte:  
[https://www.adeept.com/video/](https://www.adeept.com/video/ "https://www.adeept.com/video/")  
Vielen Dank, dass Sie Adeept-Produkte verwenden.  

![Adeept](./images/End.jpg "Adeept")
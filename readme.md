# Flugbuch

Digitales Pilot Logbuch als Progressive Web App (PWA) zur Erfassung, Auswertung und Synchronisation von Flugzeiten.

## Funktionen

* Lokale Datenspeicherung direkt im Browser
* Automatische Berechnung von Flug- und Blockzeiten
* Auswertungen nach Kategorien (SEP, MEP, IR, FSTD) sowie Funktionen (PIC, Dual, FI, Co)
* Nachweis über Landungen (Tag/Nacht) sowie IFR- und Nachtflugzeiten
* Import von Excel-Dateien (.xlsx) mit automatischer Spaltenerkennung
* CSV-Export und JSON-Backup
* Synchronisation mit Google Sheets via Google Apps Script

## Google Sheets Synchronisation

Die Anwendung ermöglicht den automatischen Abgleich aller Daten mit einem Google Sheet.

### Einrichtung

1. Google Sheet öffnen und über `Erweiterungen` den Punkt `Apps Script` aufrufen.
2. Den im Bereich `Sync` der App bereitgestellten Code einfügen und ein individuelles Passwort bei `TOKEN` festlegen.
3. Auf `Bereitstellen` > `Neue Bereitstellung` klicken.
4. Typ `Web-App` wählen.
5. Ausführen als: `Ich`.
6. Zugriff: `Jeder`.
7. Nach der Bereitstellung die generierte Web-App-URL kopieren.
8. Die Web-App-URL sowie das Passwort in der Anwendung unter `Daten` > `Sync` eintragen und speichern.

### Wichtiger Hinweis bei Codeänderungen

Jegliche Anpassungen am Skript in Google Apps Script erfordern zwingend eine **neue Bereitstellung** (Neue Version), um wirksam zu werden. Durch die Erstellung einer neuen Bereitstellung ändert sich die Web-App-URL. Die aktualisierte URL muss anschließend zwingend in den Einstellungen der Anwendung unter `Sync` erneut eingetragen werden.

## Installation und Betrieb

Die Anwendung besteht aus einer einzelnen Standalone HTML Datei und kann auf jedem beliebigen Webserver gehostet oder als PWA auf mobilen Endgeräten installiert werden.
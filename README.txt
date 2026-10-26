Pocket Pong — by SAMIX  (GAMES · APPS · INNOVATION)

Starten
-------
ZIP entpacken und den Ordner über einen lokalen Webserver bereitstellen
(ES-Module funktionieren nicht direkt per file://).

    python3 -m http.server 8000

Dann http://localhost:8000 im Browser öffnen. Auf dem iPhone: dieselbe Adresse im
Netzwerk aufrufen und in Safari "Zum Home-Bildschirm" wählen für Vollbild.

Phaser wird per CDN (esm.sh) geladen, daher ist beim ersten Start eine
Internetverbindung nötig. Schlägt das Laden fehl, zeigt der SAMIX-Ladebildschirm
eine Fehlermeldung mit "Neu laden".

Projektstruktur
---------------
index.html            Seite, SAMIX-Ladebildschirm, Menüs, Pause, Spielende
styles.css            komplettes UI-Design (Tokens am Anfang der Datei)
main.js               Start (Phaser, Startbildschirm, Pausenmenü)
config.js             Farben, Schriften, Schwierigkeit, Ball-Tuning
ui/startScreen.js     Hauptmenü + Schwierigkeitsauswahl, beendet den Ladebildschirm
ui/pauseMenu.js       Pause-Button + Pausenmenü
scenes/, systems/,
entities/, sounds/    Spiellogik (Mechanik unverändert)
assets/samix-logo.png SAMIX-Logo (freigestellt, transparent)
assets/branding/      Original-Logo (JPG) als Referenz
assets/img_*.png      frühere Referenz-Screenshots (werden vom Spiel nicht benutzt)

Entwickler
----------
index.html?tune öffnet das Tuning-Panel (AI- und Ballparameter live ändern).

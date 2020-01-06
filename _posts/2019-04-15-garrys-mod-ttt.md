---
layout: post
title: Wie installiere ich einen Garry's Mod TTT Server? (+ Steam Workshop)
description: Auf Ubuntu Server 16.04/18.04 mit Steam Workshop
img: gmod.jpg
# gh-repo: daattali/beautiful-jekyll
# gh-badge: [star, fork, follow]
categories: [Gaming, Server, Projekt]
author: j0nas500
---

Wenn du wissen willst wie Du auf dem Server kommst schau doch mal beim [Blogpost](https://mvbuddies.de/projects/gaming/garrys-mod-ttt) in der Kategorie Gaming vorbei.

Wir haben für den Garry's Mod Server einen Vserver gebucht. Auf dem Vserver läuft Ubuntu 18.04, sollte aber auch für Ubuntu 16.04 funtkionieren.

## Updaten
Als aller erstes aktualisieren wir unseren Server mit folgenden Befehlen:  
`sudo apt-get update`  
`sudo apt-get upgrade`

## Benötigte Programe installieren
Damit wir Garry's Mod auf unserem Server haben benötigen wir vorerst ein paar kleine Programme, die wir wie folgt installieren:  
`sudo apt-get install lib32gcc1 lib32stdc++6 screen`

## Neuer Ordner
Um ein bisschen Ordnung zu schaffen, erstellen wir einen Ordner für SteamCMD mit dem wir uns die nötigen Dateien für Garry's Mod holen.  
`mkdir steamcmd`  
`cd steamcmd`

## SteamCMD herunterladen
`wget https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz`  
`tar -xfvz steamcmd_linux.tar.gz`

## SteamCMD öffnen
`./steamcmd.sh`  
Aktualisiert, installiert und startet SteamCMD

## Garry's Mod Server Dateien herunterladen
`login anonymous`  
Den Pfad angeben wo Garry's Mod installiert werden soll  
`force_install_dir ../gmod`  
Garry's Mod Server Dateien herunterladen  
`app_update 4020 validate`  
`quit`

## Verwenden der heruntergeladen Software "Screen"
Screen ermöglicht es uns mehrere "Tabs" in einer Konsole zu haben.  
`screen -S gmod`  
`cd ../gmod`

## Starten des Garry's Mod Servers
`./srcds_run -game garrysmod +map gm_construct`  
Wenn die Konsole `VAC secure mode is acitivated` anzeigt ist dein Server online. Probiere es gerne aus.

## TTT Modus auswählen
Füge in den oben genannten Befehl den Zusatz-Parameter gamemode aus und wähle eine TTT-Map und ggf. die maximale Spieleranzahl.  
`./srcds_run -game garrysmod +gamemode terrortown +maxplayers 10 +map ttt_minecraft_b5`

## Steam Workshop einbinden sowie zusätzliche Einstellungen
Wenn ihr Inhalte aus dem Steam Workshop auch auf eurem Server haben wollt wie beispielsweise Waffen und Maps, so packt sie alle erstmal in eine von euch erstellte [Kollektion](https://steamcommunity.com/sharedfiles/filedetails/?id=859405395).

Dann müsst ihr euch auf der Website von Steam anmelden und hier euren persönlichen/geheimen Steam Web-API-Schlüssel kopieren: [https://steamcommunity.com/dev/apikey](https://steamcommunity.com/dev/apikey)

Wenn ihr noch zusätzliche Einstellungen machen wollt, tut es in der server.cfg die ihr hier speichert: `/garrysmod/cfg/server.cfg`
Zum bearbeiten dieser Datei gebt folgenden Befehl ein: `nano server.cfg`

Alle möglichen Einstellungsmöglichkeiten findet ihr hier:
- [http://ttt.badking.net/config-and-commands/convars](http://ttt.badking.net/config-and-commands/convars)
- Auf Deutsch: [https://wiki.nitrado.net/de/Server.cfg_von_Garrys_Mod_Servern](https://wiki.nitrado.net/de/Server.cfg_von_Garrys_Mod_Servern)
- Und einen Generator: [https://csite.io/tools/gmod-universal-cfg](https://csite.io/tools/gmod-universal-cfg)

Nachdem ihr nun die Kollektion erstellt, den apikey kopiert und ggf. eine server.cfg Datei angelegt habt lautet der Befehl zum starten des Servers wie folgt:  
`./srcds_run -game garrysmod +gamemode terrortown +maxplayers 10 +exec server.cfg +map ttt_minecraft_b5 -authkey deinAPI-Schlüssel +host_workshop_collection 1624306589
`

Zum Parameter `-authkey` fügst du deinen AuthKey ein. Beim Parameter `+host_workshop_collection` fügst du die ID deiner Kollektion ein. Die ID findest du am Ende der URL, wenn du auf der Seite deiner Kollektion bist.

Wenn es noch weitere Fragen gibt, melde dich gerne in unserem [Forum](https://forum.mvbuddies.de) oder auf unserem [Discord](http://discord.mvbuddies.de)

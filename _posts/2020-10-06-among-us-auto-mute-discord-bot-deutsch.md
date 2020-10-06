---
layout: post
title:  "Wie nutzt man den Among Us Auto Mute Discord Bot?"
categories: [Gaming, Apex Legends, Free, kostenlos]
img: amongus/thumbnail.jpg
description: Erfahre, wie du den Among Us Discord Bot nutzt und sogar selber hosten kannst, damit deine Mitspieler auf Discord automatisch stummgeschaltet werden.
author: j0nas500
---


In diesem Tutorial erfährst du wie du den "Among Us Auto Mute" Discord Bot verwendest. Dieser Bot ermöglicht es allen Mitspielern die mit dir in der Among Us Runde auf Discord sind automatisch zu muten und taub zu stellen. Für die Umsetzung gibt es zwei Optionen. Wenn du nur den "Among Us Auto Mute" Discord Bot auf deinem Server einladen möchtest und ihn sofort nutzen willst schau dir Option 1 an. Willst du den Bot selber auf deinem PC hosten, schau dir Option 2 an. 

Beachtet aber zu erst die Voraussetzungen!



## Voraussetzungen

Damit es nicht zu Problemen kommt, bitte ich euch folgende Einstellung in eurem Windows Datei Explorer vorzunehmen:

- Klick dafür auf "Ansicht" und aktiviere "Dateinamenerweiterungen"

![image-20201005125827646](/images/amongus/image-20201005125827646.png)



Ihr könnt nach dem Tutorial die Option nachträglich wieder deaktivieren.

**Dein Discord Server benötigt 25 freie Emoji-Slots, damit der Bot einwandfrei funktionieren kann.**

Gehe nun zu [Option 1](#option-1---bot-einladen), wenn du den Bot nun einladen möchtest. Schau dir sonst noch die [Voraussetzung für Option 2](#für-option-2) an, wenn du den Bot selber hosten willst.



### Für Option 2

Da du den Bot selber hosten willst, musst du erstmal einen Bot erstellen. 

- Dafür gehst du auf die [Developer Seite von Discord](https://discord.com/developers/applications) und erstellst dir eine neue "Application"

  ![image-20201005130231465](/images/amongus/image-20201005130231465.png)

- Gebe der "Application" nun einen sinnvollen Namen und klicke auf "Create"

  ![image-20201005130406702](/images/amongus/image-20201005130406702.png)

- Klicke nun links auf den Reiter "Bot" und dann rechts auf "Add bot"

  ![image-20201005130633733](/images/amongus/image-20201005130633733.png)

- Kopiere nun deinen Discord Bot Token und sicher dir den irgendwo. Zum Beispiel füg ihn einfach in deinen Text Editor ein

  ![image-20201005130829644](/images/amongus/image-20201005130829644.png)



Nun hast du einen Discord Bot erstellt. Als letzten Schritt der Vorbereitung musst du noch deinen erstellten Bot auf deinem Discord Server einladen. Dafür besuche folgende Webseite: [https://discordapi.com/permissions.html#8](https://discordapi.com/permissions.html#8)

Auf der Seite gibt's du unten die "Client ID" ein, die du bei deiner Application unter "General Information" findest und gib dem Bot Administrator Rechte. Zuletzt klickst du auf den Link der ganz unten auf der Webseite steht:

![image-20201005131426110](/images/amongus/image-20201005131426110.png)

![image-20201005131649552](/images/amongus/image-20201005131649552.png)

Auf den Link geklickt fragt Discord auf welchem Server du den Bot haben willst. Nach der Auswahl ist dein Bot auf deinem Discord drauf. Zwar noch Offline, aber das wollen wir jetzt angehen. Schau dafür bei [Option 2](#Option 2 - Bot auf dem PC selber hosten) rein.



## Option 1 - Bot einladen

### Bot einladen

Lade den Discord Bot ein: [https://discord.com/oauth2/authorize?client_id=762435324953231440&scope=bot&permissions=8](https://discord.com/oauth2/authorize?client_id=762435324953231440&scope=bot&permissions=8)

**Hinweis: Der Bot könnte Offline sein. Denn der Bot fährt automatisch nach 30min Inaktivität herunter.**

### Among Us Capture herunterladen

Damit der Bot weiß, wer in der Among Us Lobby ist, benötigst du ein Programm was dein Among Us Spiel aufzeichnet. Für das Programm musst du einen Ordner erstellen, in der du das Programm speicherst. Das Programm nennt sich `AmongUsCapture-x64.exe` und kann  [hier heruntergeladen werden](https://github.com/denverquane/amonguscapture/releases). Dort einfach die letzte Version auswählen.

![image-20201005133433938](/images/amongus/image-20201005133433938.png)

Zuletzt benötigst du ein Textdokument, was du `host.txt` nennst. In dieser Textdatei schreibst du folgendes rein:

`https://audcbotpublic.herokuapp.com/`

![image-20201005133813603](/images/amongus/image-20201005133813603.png)

Wenn du alles richtig gemacht hast müsste dein Ordner nun folgendermaßen aussehen:

![image-20201005133847682](/images/amongus/image-20201005133847682.png)



### Among Us starten

Starte nun Among Us und erstelle eine Lobby. Danach starte die `AmongUsCapture-x64.exe`

Spätestens jetzt sollte auch der Among Us Discord Bot, den du eingeladen hast Online sein. Betrete also, wenn noch nicht getan einen Sprachkanal und gebe in einen Textkanal `.au new` ein. Du solltest dann folgende Rückmeldung vom Discord erhalten haben:

![image-20201005134231915](/images/amongus/image-20201005134231915.png)

Gebe den Capture Code, in diesem Fall "329DCB" in die `AmongUsCapture-x64.exe` ein:

![image-20201005134353948](/images/amongus/image-20201005134353948.png)

Wenn du nach der Eingabe auf den Button "Submit" gedrückt hast, sollte die Discord Nachricht vom Bot nun folgendermaßen aussehen:

![image-20201005134445761](/images/amongus/image-20201005134445761.png)

Du bist fertig. Jetzt müssen deine Mitspieler nur noch mit der Farbe reagieren die sie haben. Und das Spiel kann beginnen. Mehr Befehle zu dem Bot erfährst du, wenn du `.au help` in einem Discord Text Kanal eingibst. Viel Spaß :)



## Option 2 - Bot auf dem PC selber hosten

Dein Discord Bot ist noch Offline. Das wollen wir jetzt angehen. Damit der Bot funktioniert, benötigst du einmal die `AmongUsCapture-x64.exe`, die `AmongUsDiscord.exe` und eine Text Datei namens `final.txt`. 

Diese drei Dateien müssen alle in einem Ordner sein, daher erstelle dir dafür erstmal einen Ordner und speicherst dort die `AmongUsCapture-x64.exe` und die `AmongUsDiscord.exe` und erstellst ein Textdokument mit dem Namen `final.txt`

[Download AmongUsCapture.exe]()

[Download AmongUsDicord.exe]()

![image-20201006110143520](/images/amongus/image-20201006110143520.png)



![image-20201006110300885](/images/amongus/image-20201006110300885.png)

Nach dem herunterladen und erstellen der Text Datei sollte dein Ordner folgendermaßen aussehen:

![image-20201006110515911](/images/amongus/image-20201006110515911.png)

Öffne die final.txt und gebe dort deinen Discord Bot Token hinter `DISCORD_BOT_TOKEN=` ein, so dass es so aussieht:

![image-20201006110818457](/images/amongus/image-20201006110818457.png)

Starte nun den Bot in dem du die `AmongUsDiscord.exe` startest. Wenn alles richtig gemacht wurde ist nun dein Bot online.

Ist dies der Fall, kannst du Among Us starten und eine Lobby erstellen. Danach starte die `AmongUsCapture-x64.exe`. AmongUsCapture zeichnet dein Spiel auf und gibt dem Bot weiter ob jemand tot ist und ob ihr gerade in der Task- oder Diskussionsphase seid, damit der Bot weiß, wann er euch muten oder entmuten soll.

Wenn noch nicht getan, betrete einen Sprachkanal und gebe in einen Textkanal `.au new` ein. Es sollte folgende Nachricht erscheinen:

![image-20201006111408980](/images/amongus/image-20201006111408980.png)

Gib nun unbedingt den Code, in diesem Fall, "1724B0" in dein AmongUsCapture Programm ein, damit der Bot weiß, woher er die Informationen bekommt.

![image-20201006111601438](/images/amongus/image-20201006111601438.png)

Nach Klick auf "Submit", sollte sich die Nachricht Nachricht vom Discord Bot folgendermaßen verändert haben:

![image-20201006111654238](/images/amongus/image-20201006111654238.png)

Ab jetzt können deine Mitspieler, mit ihrer Farbe reagieren und das Spiel kann danach losgehen. Viel Spaß :)

Mehr Befehle zu dem Bot erfährst du, wenn du `.au help` in Discord eingibst.
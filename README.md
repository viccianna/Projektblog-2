# Block über das Spiel ("*ABC lernen*")

Ein Blog über unser programmieretes Spiel auf App-Labor.

![bsp stride](projekt2.png)

# Inhalt

[1. Einleitung und Idee](#1)


[2. Das Spiel](#2)


## <a name="1"></a> Einleitung und Idee

Hallo und herzlich Willkommen auf diesem Blog. Wie ihr wahrscheinlich schon von unserem Stundenblog wisst, werden wir euch hier alles rund um unser zweites Informatikprojekt erläutern und Schritt für Schritt erklären. Dazu haben wir zum Verständnis auch zusätzlich Bilder im Laufe der Erläuterung eingefügt.

Und nun viel Spaß beim Lesen!

Zunächst ist hier eine kleine Einleitung, welche erläutert wie wir auf die Idee unseres jetztigen Projekts gekommen sind:
Wie schon im Stundenblock erwähnt, hatten wir zu anfang nicht die leiseste Idee für ein neues Spiel. Doch wir waren uns ziemlich schnell einig, dass wir diesesmal ein neues Programm für unser Projekt nutzen wollen. Dies aus dem einfachen Grund, dass wir etwas anderes ausprobieren wollen. Da wir mit Snap! doch ziemlich lange gearbeitet hatten und einigermaßen gut eingearbeitet waren, wollten wir uns auf neues Terrain begeben. Außerdem haben wir für uns beschlossen, dass wir ein Handyspiel programmieren wollten und dies ist mit Snap! nicht wirklich möglich. Unsere engere Auswahl beinhaltete dann Applab und Appinventor. Schließlich haben wir uns dann für Applab entschieden, da wir dieses Programm umgänglicher fanden (insbesondere was das Design anging). 
Unsere ersten Ideen waren: Vokabeltrainer (für Englisch und Fachbegriffe z.B in Biologie) und eine Quizapp für Biologie. Da wir aber bei beiden Ideen nicht sicher bei der Umsetzung waren haben wir nachwievor über andere Spielideen nachgedacht. Aber wir hatten bei allen Ideen die Intention, etwas mit Lerneffekt zu programmieren. Wie bei unserem ersten Spiel, haben uns teilweise unsere kleinen Geschwister inspiriert. Daraufhin kam uns die Idee ein Spiel zu programmieren, welches Kleinkindern das Alphabet beibringt. Indem die Kinder den Buchstaben groß auf dem Bildschirm sehen, müssen sie eins von zwei Bildern anklicken. Das richtige Bild fängt mit dem dazugehörigen Buchstaben zusammen. Um den Lerneffekt noch weiter zu vergrößern, wird auch bei jedem Anklicken eines Bildes (egal ob richtig oder falsch) der Gegenstand ausgesprochen, sodass die Kinder auch lernen, wie die Bilder ausgesprochen werden (z.B. "A, wie Apfel" oder "B, wie Banane").


## <a name="2"></a> Das Spiel

Wir haben die Hintergründe bzw. Screens als ertses erstellt. Dazu haben wir auf der Website oben links auf "Entwurf" geklickt. Daraufhin öffnete sich eine Spalte in der man verschiedene Optionen zum Gestalten des Screens auswählen kann wie zum Beispiel ein Textfeld hinzufügen oder die Farbe des Hintergrunds geändert werden kann. Zunächst haben wir dann 26 Screens erstellt und jeweils verucht eine andere Farbe zu erstellen. Danach wurde ein Textfeld eingefügt und die einzelnen Buchstaben in richter Größe hingeschrieben. Danach wirden zwei Felder für Bilder hinzugefügt. Als letztes haben wir noch einige Button hinzugefügt, das wird später noch genauer erklärt.


![bsp stride](imageprojektblog.exe/screen30anfang.png) 

Der Einstieg in unser Spiel ist auf dem Screenshot hier rot eingekreist. Das Spiel beginnt mit unserem Startbildschirm, welcher auf dem Screenshot (links) zu sehen ist. Der Befehl "*setScreen(screenId)*" ganz am anfang bewerkstelligt, dass ein bestimmter Screen auftaucht sobald man auf "*Ausführen*" (links auf dem Bildschirm) klickt. In unserem Fall ist die ScreenId "*screen30*" und demnach haben wir dies in das Kästchen eingegeben.
Der nächste Befehl ist ein "*if()*"-Befehl. Wie auch die deutsche Übersetzung sagt, ist dieser Befehl eine Bedingung, die wir definiert haben. In die leere Klammer haben wir in diesem Fall erneut "*screen30*" eingesetzt. Dies ist damit zu begründen, dass es sich bis hierher immernoch um den gleichen Screen handelt. Unter "*if()*" haben wir mit weiteren Befehlen einen Block erstellt, welcher das eigentliche Spiel einleitet.
Zunächst folgt der Befehl "*onEvent (id, type, callback)*" verbunden mit "*function()*". Die erste Lücke des ersten Befehls für "*id*" füllt "*button6*". In die zweite Lücke "*type*" ist "*click*" eingesetzt und die letzte Klammer besteht aus dem "*function()*"-Befehl. Dieser Block zusammengesetzt bewirkt, dass sobald man auf den Button (auf dem Screen unten in der Mitte) klickt, das Spiel "*Beginnt*". 
Zusammenhängend mit diesem Befehlblock folgt nach dem eben Erläuterten der Befehl "*var(str)="hello world"*". Hinter dem Gleichzeichen ist ein Operator ("*()+()*") eingefügt. In die erste Klammer ist "screen" hinzugefügt worden. In der zweiten steht "*randomNumber(1,26)*", wobei die Zahlen für die Anzahl der Buchstaben im Alphabet stehen. Damit wird festgelegt, dass sobald das Spiel beginnt ein zufälliger Screen und damit zufällige Buchstaben auftauchen. Auf diesen Befehl folgt ein letzter, welcher diesen Block abschließt: "*setscreen(str)*". Damit wird dann endgültig der Screen gewechselt und die "*Id*" ist hier "*str*". Dies ist notwendig damit der Befehl weiß, dass er einen "*randomscreen*" aussucht.

![bsp stride](imageprojektblog.exe/screen1anfangrichtig.png) 

Mit dem oben eingekreisten Block beginnt das eigentliche Spiel. Wie schon der vorherige Block beginnt auch dieser mit dem Befehl "*if()*". Diesmal steht in der Klammer "*screen1*", jedoch wird durch den ersten Block ein beliebiger Screen ausgesucht. Das bedeutet, dass "*screen1*" hier nur ein Beispiel ist und das Spiel so anfangen kann aber nicht muss. Da dieser an den zuvorkommenden Block angebunden ist, steht dieser Block in direkter Verbindung mit dem Ersten. Sobald also der erste Block abgelaufen ist, fängt die neue Schleife an. In diesem Fall haben steht dort als "*id*" "*screen1*". Damit öffnet sich ein neuer Screen (am Beispiel angepasst, siehe Screenshot links). Der darauffolgende Befehl ist erneut "*onEvent (id, type, callback)*". Die Klammern sind mit "*image1*", "*click*" und "*function()*" gefüllt. Kurz bedeutet dies, dass sobald man "*image1*" (Apfel) anklickt, passiert etwas. Was genau darauf folgt zeigt der nächste Befehl. Das drauffolgene "*playSound ()*" beinhaltet ein Audio, welches entweder aufgenommen oder hochgeladen werden muss. Unsere Audios wurden mit dem Handy aufgenommen und dann auf den Computer gespielt und gespeichert. Sobald man den befehl einfügt und anklickt, kann man den Sound auswählen. Wenn man den Block bis zu dieser Stelle ausführen würde, würde sobald man auf das richtige Bild klickt ein bestimmtes Geräusch abgespielt. Bezogen auf unser Beispiel klickt man auf den Apfel und danach sagt eine Stimme: "A, wie Apfel". Als nächstes folgt der Befehl "*setScreen28*", welcher einen neuen Screen öffnet. Dieser spezielle Screen taucht nur dann auf, wenn man das richtige Bild angeklickt hat. Es folgt wie im ersten Block nochmal "*onEvent (button5),(click), (function)*", wenn man also auf "*button5*" klickt wiederholt sich die eben erläuterte Schleife. Nachdem "*screen28*" durch den Klick auf den Button verschwindet erscheint ein neuer randomScreen (durch die schon erklärten Befehle). 
Dies ist der Block für den Fall, dass man alles richtig gewöhlt hat.
Im direkten Anschluss auf diesen gibt es einen weiteren Befehlblock welcher bestimmt was passiert, wenn man das falsche Bild anklickt. Er beginnt auch mit "*onEvent*" doch die "*id*" ist in diesem Fall ist "*image2*". wenn man dieses falsche Bild anklickt, wird erneut ein Sound vorgelesen aber es ist nicht der gleiche wie beim richtigen Bild. Das wir durch den befehl "*playSound()*" bewerkstelligt. Danach wird der Screen "*screen29*" auftauchen und durch das Antippen des "*Button4*" kommt der Spieler zurück zu dem Screen auf dem der Buchstabe war um die Frage diesmal richtig zu beantworten. 
Da wir dieses Prinzip für unsere Blöcke für alle Buchstaben nutzen, wiederholt sich die Kette von Befehlen von A bis Z.

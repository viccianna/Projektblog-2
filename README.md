# Block über das Spiel ("*ABC lernen*")

Ein Blog über unser programmieretes Spiel auf App-Labor.

![bsp stride](projekt2.png)

# Inhalt

[1. Einleitung und Idee](#1)


[2. Das Spiel](#2)


## <a name="1"></a> Einleitung und Idee

Hallo und herzlich Willkommen auf diesem Blog. Wie ihr wahrscheinlich schon von unserem Stundenblog wisst, werden wir euch hier alles rund um unser zweites Informatikprojekt erläutern und Schritt für Schritt erklären. Dazu haben wir zum Verständnis auch zusätzlich Bilder im Laufe der Erläuterung eingefügt.

Und nun viel Spaß beim Lesen!

Zunächst ist hier eine kleine Einleitung, welche erläutert wie wir auf die Idee unseres jetzigen Projekts gekommen sind:
Wie schon im Stundenblock erwähnt, hatten wir zu anfang nicht die leiseste Idee für ein neues Spiel. Doch wir waren uns ziemlich schnell einig, dass wir diesesmal ein neues Programm für unser Projekt nutzen wollen. Dies aus dem einfachen Grund, dass wir etwas anderes ausprobieren wollen. Da wir mit Snap! doch ziemlich lange gearbeitet hatten und einigermaßen gut eingearbeitet waren, wollten wir uns auf neues Terrain begeben. Außerdem haben wir für uns beschlossen, dass wir ein Handyspiel programmieren wollten und dies ist mit Snap! nicht wirklich möglich. Unsere engere Auswahl beinhaltete dann Applab und Appinventor. Schließlich haben wir uns dann für Applab entschieden, da wir dieses Programm umgänglicher fanden (insbesondere was das Design anging). 
Unsere ersten Ideen waren: Vokabeltrainer (für Englisch und Fachbegriffe z.B in Biologie) und eine Quizapp für Biologie. Da wir aber bei beiden Ideen nicht sicher bei der Umsetzung waren haben wir nachwievor über andere Spielideen nachgedacht. Aber wir hatten bei allen Ideen die Intention, etwas mit Lerneffekt zu programmieren. Wie bei unserem ersten Spiel, haben uns teilweise unsere kleinen Geschwister inspiriert. Daraufhin kam uns die Idee ein Spiel zu programmieren, welches Kleinkindern das Alphabet beibringt. Indem die Kinder den Buchstaben groß auf dem Bildschirm sehen, müssen sie eins von zwei Bildern anklicken. Das richtige Bild fängt mit dem dazugehörigen Buchstaben zusammen. Um den Lerneffekt noch weiter zu vergrößern, wird auch bei jedem Anklicken eines Bildes (egal ob richtig oder falsch) der Gegenstand ausgesprochen, sodass die Kinder auch lernen, wie die Bilder ausgesprochen werden (z.B. "A, wie Apfel" oder "B, wie Banane").


## <a name="2"></a> Das Spiel

Wir haben die Hintergründe bzw. Screens als erstes erstellt. Dazu haben wir auf der Website oben links auf "Entwurf" geklickt. Daraufhin öffnete sich eine Spalte in der man verschiedene Optionen zum Gestalten des Screens auswählen kann wie zum Beispiel ein Textfeld hinzufügen oder die Farbe des Hintergrunds geändert werden kann. Zunächst haben wir dann 26 Screens erstellt und jeweils verucht eine andere Farbe zu erstellen. Danach wurde ein Textfeld eingefügt und die einzelnen Buchstaben in richter Größe hingeschrieben. Danach wirden zwei Felder für Bilder hinzugefügt. Als letztes haben wir noch einige Button hinzugefügt, das wird später noch genauer erklärt.


![bsp stride](images.exe./screen66anfang.png)

Unser Spiel beginnt mit einem "*function*"-Block an. Dieser heisßt "showResults" und bezieht sich auf unsere Statistik welche wir erst später bei den eigentlichen Spielen eingebaut haben. Also sobald später eine Funktion angeklickt wird, wird dieser Befehlblock ausgeführt. Dieser beginnt mit "*setScreen*" mit der *ID* "screen66", welcher links auf dem Bild zu sehen ist. Darauf folgt der Befehl "*readRecords*" mit der *ID* "mytable". And diese ist eine weitere Funktion angebunden (dunkelgrün) mit der *ID* "records". In lila sieht man ein paar Variabeln, welche wir erstellt und definiert haben. Die erste *var* ist "Richtig=0", die Zweite ist "Falsch=0" und die Nächste ist "totalVotes=Records.lenght" ...

....


![bsp stride](images.exe./screen67anfang.png)

![bsp stride](images.exe./1.block.png)
-> Fehler anmerken: zu viele IDs, überfordert
unterfordert weilo hochbegabt
Die "*onEvent*" Funktion sagt, dass wenn man auf "deletebutton" klickt, dann wird eine Funktion ausgelöst.

![bsp stride](images.exe./screen30angang.png)

Nachdem die vorherigen Befehlblöcke nun erklärt wurden, kommt jetzt der "richtige" Anfang des Spiels. Dieser beginnt mit dem schon definierten Befehl "*setScreen*" mit der *ID* "screen30". Damit wird automatisch dieser bestimmte Screen zu anfang des Spiels geöffnet. Als nächstes folgt ein "*if*"-Befehl. Dieser Befehl mit derselben *ID* wie eben beinhaltet mehrere Befehle angefangen mit "*onEvent*". In diesem Block steht "button6" als die *ID*, "click" als *type* und zum Schluss eine Funktion mit der Definition "event". Die "*onEvent*"Funktion beinhaltet zwei weitere Befehle und zwar "*playSound(ID)*, false" und "*setScreen(screen27)*". Zusammengesetzt bedeutet diese ganze Klammer nun, wenn man auf "screen30" ist und dann den Button "button6" angklickt, dass wird ein bestimmter Sound abgespielt und es wird ein andere Screen geöffnet. (Buuton6 sieht man auf dem Bild mit der Beschriftung: LOS)

![bsp stride](images.exe./screenspiel1anfang.png)

In rot eingekreist sieht man hier einmal die Weiterführung zum vorherigen Bild. Die Ausgangssituation war, dass man auf Screen27 landet. Sobald das geschieht, folgt wieder eine "*if*"-Schleife. Diese beinhaltet, eine "*onEvent*" Funktion. Da das eingekreiste erst einmal nur für die Auswahl der Spiele gilt, hat der Spieler ja eine gewisse Wahl. In diesem Fall, wenn er auf den Button "button1" klickt, wählt er das 1. Spiel, welches wir gleicfh näher erläutern. Diese Funktion enthält einen neue Variable, die so definiert ist, dass ihr *ID* gleich "str" ist und sich aus der *ID* "screen" * eine "randomNumber(1,26)" zusammensetzt. Das bedeutet, es wird aus den ganzen Screen, welche von "screen1" bis "screen26" gehen, ein Zufälliger ausgewählt. Danach wird der folgende Befehl diesen zufällig Ausgewählten öffnen. 

Daraufhin beginnt das erste Spiel: "ABC-lernen mit Bildern"

![bsp stride](images.exe./spiel1anfang.png)

Hiermit beginnt das 1. Spiel. Das Ziel hierbei ist, dass man einen Buchstaben gegeben hat und man muss dazu das passende Bild anklicken, welches mit dem gezeigten Buchstaben als Wort anfängt. Ein Beispiel wäre: gegeben ist "A" und dann klickt man als Bild den Apfel an.

Das Prinzip der Befehlkette machen wir hier am einem Beispiel klar. 5r






Hier machen wir die Schleife wieder einem Beispiel deutlich. In der "*if*"-Schleife befinden sich drei "*onEvent*" Funktionen. 



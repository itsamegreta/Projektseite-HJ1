# Projektseite-HJ1

<img width="532" alt="Bildschirmfoto 2021-12-04 um 11 29 42" src="https://user-images.githubusercontent.com/88386040/144706263-437e5ceb-0f88-4b66-bc5f-2f171d7e6b44.png">

## Idee

Unsere Informatikaufgabe für das erste Jahr war es, uns mit der Technik des Programmierens auseineinanderzusetzen und ein Spiel oder Ähnliches zu programmieren.

Da wir uns beide zuvor nicht mit dem Programmieren beschäftigt haben, haben wir in der Schule und zu Hause verschiedene Tutorials angesehen und diese durcharbeitet und versucht zu verstehen, wie das von uns ausgesuchte Programm Snap! funktioniert und was unsere Projektmögichkeiten mit diesem sind. 

Dazu haben wir zu Beginn kleinere Projekte ausprobiert, in denen wir die Funktionsweise des Programms testeten. Dabei entstand auch unser erster Spielidee, welche wir, obwohl wir sie zwischendurch in der geplanten Form verworfen hatten, letztendlich doch für unser Spiel genutzt haben. 

## Programm

Nach unserer Recherche und einer Absprache mit Herrn Buhl, haben wir uns für für das Programm Snap! entschieden. Da wir weniger Tutorials oder Erklärung als gedacht gefunden haben, haben wir uns auch mit diesen für die Programmiersprache Scratch beschäftigt, da die beiden Sprachen sich stark ähneln. 

Wir haben uns für Snap! entschieden, da es eine visuelle Blockprogrammiersprache ist, die besonders für Beginner geeignet ist, da man die einzelnen Befehle aus bereits vorandenen Blöcken zusammensetzten kann, aber wenn nötig, auch eigene Blöcke erstellen kann. 

<img width="1440" alt="Bildschirmfoto 2021-12-04 um 11 16 44" src="https://user-images.githubusercontent.com/88386040/144705832-694fe412-c20e-4159-b9bd-1a1c5fe8ba08.png">

Die vorhandenen Blöcke lassen sich in acht Kategorien gliedern, aus denen man per Drag and Drop eine Vielzahl von Befehlen wählen und erstellen kann. Die acht Kategorien lauten Motion, Looks, Sound, Pen, Control, Sensing, Operators und Variables.

<img width="222" alt="Bildschirmfoto 2021-12-04 um 11 15 16" src="https://user-images.githubusercontent.com/88386040/144705791-24b77671-7245-4d26-8e3c-4eecceb82a3a.png">

## Umsetzung der Idee - Konzept

### Variablen 

Damit unser Spiel funktionieren kann wie es soll, haben wir zwei Variablen erstellt.

Die Variable "Leben" wird zu Beginn des Spieles auf drei gesetzt und spiegelt die Herzen wider, die der Dino verlieren kann. Sobald diese null erreicht, ist das Spiel verloren.
Die zweite Variable "Timer" spiegelt die abgelaufene Zeit wider. Wenn dieser null erreicht, gilt das Spiel als gewonnen.

![grafik](https://user-images.githubusercontent.com/88386040/144721348-a6d363e3-b36a-40c4-8055-68b58bdf63a2.png)

Beide Funktionen werden bei der Erklärung der Stage noch genauer ins Detail genommen.

### "Broadcast"

Wir haben für das Spiel vier zu broadcastende Befehle erstellt:

1. "Spielstart", der gebroadcastet wird, sobald die grüne Flagge gedrückt wird, dessen Blockkombination sich auf der Stage befindet.

![grafik](https://user-images.githubusercontent.com/88386040/144721578-6b231b7b-fa04-459c-9e66-9b59cfdd4a31.png)

2. "Level Beginn", der gebroadcated wird, sobald der Startbutton gedrückt wird und deshalb auch dort zu veroten ist.

![grafik](https://user-images.githubusercontent.com/88386040/144721644-dc94db33-4efe-4567-ac4c-bec91d493e0c.png)

3. "Game Over", das gebroadcasted wird wenn der Spieler alle Leben verliert und bei den Herzen zu verorten ist.

4. "WIN", das gebroadcasted wird sobald der Timer von 45 Sekunden abgelaufen ist. Es befindet sich bei den Blöcken des Spites "WIN".

### Spielfigur: Dinosaurier 

Als Spielfigur des Spieles dient ein blauer Dinosaurier, den der Spieler mit der linken und rechhten Pfeiltaste steuern kann. Ziel dabei ist es den vom Himmel fallenden Meteoriten auszuweichen. Dabei entspricht die Richtung der Pfeiltaste der Bewegungsrichtung. 

Dazu wird der Control-Block "When I receive Level Beginn" in Kombination mit dem Block "show" genutzt, damit folgende Blöcke erst nach drücken des Start-Buttons funktionieren. Darunter haben wir einen "forever" Block gesetzt, in dem wir zwei verschiedene "if x-Key pressed-Blöcke" mit je einem "switch to custume x" und einem "change x by x-Block" kombiniert haben. Beim Drücken der rechten Pfeiltaste wird das normale Kostüm "Dino" genutzt, in dem der Dino nach rechts guckt, wird die linke Pfeiltaste gedrückt, muss das Kostüm "dino 2" genutzt werden, da der Dino sonst rückwärts laufen würde. Er läuft daraufhin 5/-5 Schritte. Dazu kommt ein Block, der es ermöglicht, dass der Dino, sobald er den rechten Rand berührt, wieder an seine Startkoordinate zurück gesetzt wird (-190/-61)

![grafik](https://user-images.githubusercontent.com/88386040/144717177-18a2a338-ef77-47bb-bf5a-46cf2eb0c0d1.png)

![grafik](https://user-images.githubusercontent.com/88386040/144717383-a833b359-7c30-458a-8df5-1044d8cd9e01.png)

Damit der Dino überhaupt angezeigt werden konnte und auf seiner Startposition auftaucht, haben wir zudem diesen Block erstellt:

![grafik](https://user-images.githubusercontent.com/88386040/144717233-8e20dc96-6778-4d66-ae5d-61e8d37e9e20.png

Der Dinosaurier sollte bevor das Spiel beginnt nicht zu sehen sein. Deshalb haben wir einen Block "when Fahne clicked" mit einem hide kombiniert. Das gleiche wollten wir wenn der Spieler gewinnt, also haben wir einen "When I receive WIN-Block" mit einem "hide" kombiniert. 

![grafik](https://user-images.githubusercontent.com/88386040/144718275-519f9b1f-d0c7-4d9c-9498-bb847242986a.png)

Wenn die Spielfigur all ihre leben verliert, ändert sich das Kostüm des Dinos zum Kostüm "Dino tot". Dazu haben wir die Blöcke "When I receive Game Over", show und "switch to costume Dino tot" kombiniert und einen Block eingebaut, der diesen auf die Höhe y=-50 setzt. 

![grafik](https://user-images.githubusercontent.com/88386040/144718584-2c729d1f-6454-4a40-b411-bc2433229086.png)

### Gegner: Meteoriten 

Die Gegner des Spieles sind die vom Himmel fallenden Meteoriten, welche drohen den Dino zu erschlagen. 

Als erstes haben wir dazu einen "Grundmeteoriten" erstellt, dessen Größe wir zu Beginn auf 20% reduziert haben. Dieser fällt nach einer drei sekündigen Wartezeit an die Koordinate (0/170) gesetzt und fällt durch die Blockkombination aus in einem "Forever" stehenden "point in direction 180" und "move 5 steps" in Richtung Erdboden.

![grafik](https://user-images.githubusercontent.com/88386040/144719384-27cc1d43-3a29-47ac-886b-7da69e90dec0.png)

Damit nicht nur ein, sondern mehrere Meteoriten entstehen, wird der "Grundmeteorit" geklont. Dazu werden, nachdem "Level Beginn" gebroadcastet wurde, die Meteoriten geklont und zu einer zufälligen Zeit, an eine zufällige x-Koordinate gesetzt und beginnen auf den Dino zu fallen, bis die Leben auf "0" gesetzt werden. Dazu wird in einer "repeat until Leben=0-Klammer", welche dafür verantwortlich ist, dass das Verfahren mit dem Spiel endet, zu Beginn durch den Block "wait'pick random 1 to 2' secs" die zufällige Zeit, in der der Klon entseht ("create a clone of myself"), verursacht, woraufhin durch den Block "go to x:'pick random -200 to 200' y:200" die zufällige Fallkoordinate gewählt wird. Damit die Meteoriten, sollten sie in der Luft hängen bleiben, nicht mehr sichtbar sind und vom Spiel ablenken, verschwinden sie durch die Blockkombination "wait 2 secs" und "hide" nach zwei Sekunden, also dann, wenn sie im Normalfall bereits den ganzen Bildschirm gefallen sind. 

![grafik](https://user-images.githubusercontent.com/88386040/144719731-ce8b8de0-8158-4165-9bba-3c0efa20d364.png)

Da die Meteoriten dem Dino sobald sie ihn treffen auch Leben abziehen sollen, haben wir eine Blockkombination erstellt, in der ab "Level Beginn" für immer gilt, dass die Meteoriten, sobald sie den Dino berühren, die Variable "Leben" um minus eins verändern. Dazu dienen die Blöcke "wait until touching 'Dino'", "change 'Leben' by -1" und "wait 2 secs" in einer "forever-Klammer". 

![grafik](https://user-images.githubusercontent.com/88386040/144719882-a5464817-23ee-497f-8b17-84d887f088e4.png)

Damit die Meteoriten beim Berühren des Bodens des Bodens, sowie bei und vor Spielbeginn, Gewinn oder Game Over nicht mehr fallen bzw. angezeigt werden, haben wir drei verschiedene Blöcke kreiert, welche jeweils ein "when I receive" mit dem jeweils gebroadcasteten Zustand kombiniert, sowie einen "when Fahne clicked" Block, auf die jeweils ein "hide"-Block folgt.

![grafik](https://user-images.githubusercontent.com/88386040/144720169-f0a5c7ab-9484-428b-b9e8-28bb9ba43270.png)

### Boden

Beim Boden handelt es sich um einen von uns gemalten Spite, bei dem wir jediglich programmieren mussten, dass er auf die Koordinate (0/-150) gesetzt wurde, und, dass er durch die Blockkombinationen "when I receive 'Level Beginn'", "show" und "when I receive 'WIN'", "hide" zum richtigen Zeitpunkt ein- oder ausgeblendet wird. 

![grafik](https://user-images.githubusercontent.com/88386040/144720386-80fb0851-0aa1-4b3a-a664-9f893b9374ed.png)

### Startbutton

Der Startbutton soll das gesammte Spiel starten, sobald er angegeklickt wird. Deshalb soll er angezeigt werden, sobald die grüne Flagge gedrückt wird, weshalb ein "when Flagge clicked" Block in Verbindung mit einem "show" Block verwendet wird. Die Größe haben wir durch den Block "set size to 55%" angepasst und ihn durch den Block "go to x:0 y:0" in die Mitte des Bildschirms gesetzt. 

![grafik](https://user-images.githubusercontent.com/88386040/144744470-cd893d51-28eb-46a1-8f04-2cfd792e0e28.png)

Damit die weiteren für das Spiel benötigten Befehle ausgeführt werden können und der Button funktioniert, muss "Level Beginn" gebroadcasted werden sobald er angeglickt wird und. Dazu haben wir die Blöcke "when I am 'clicked'" und "broadcast 'Level Beginn'" kombiniert. Damit der Startbutton gedrückt wurde und das Spiel beginnt, sollte der Button zudem nicht mehr zu sehen sein, weshalb wir einen "hide"-Block eingebaut haben.

![grafik](https://user-images.githubusercontent.com/88386040/144744649-8e86f3ef-60e7-462e-b6f6-0d882beee009.png)

### Leben 

Unsere Spielfigur sollte drei Leben haben, damit das Spiel nicht sofort endet, sollte der Dino von einem Meteorit getroffen werden. Dafür haben wir die Variable "Leben" erstellt und auf drei gesesetzt, indem wir den Block "when I receive 'Level Beginn'" mit dem Variablen-Block "set 'Leben' to 3" kombiniert haben. Um die Lage der Leben auf dem Bildschirm festzulegen, haben wir die Anzeige durch den Block "set size to 30%" auf eine geeignete Fröße gesetzt und durch "go to x:-170 y:150" an eine geeignete Stelle des Bildschirms positioniert. 

![grafik](https://user-images.githubusercontent.com/88386040/144745462-ffcbc09f-6e0c-4564-9399-ca739f0f90fa.png)

Damit auch wirklich Leben abgezogen werden, befindet sich beim Spite "Meteorit" ein Block, durch den der Variable "Leben" ein Herz abgezogen wird, sobald der Dino von einem Meteoriten getroffen wird. Dazu benötigten wir die Blöcke "wait until 'touching Dino'" und "change 'Leben' by -1"

![grafik](https://user-images.githubusercontent.com/88386040/144745586-9219207e-20d9-46be-83e6-3d9e0e16d730.png)

Damit wir eine funktionierende Lebensanzeige haben, mussten wir zuerst vier verschiedene Costumes erstellen. Wir brauchten nämlich je ein Costume für null bis drei Herzen:

![grafik](https://user-images.githubusercontent.com/88386040/144745787-acafd8b9-e689-41de-9119-eae826f3808b.png)

Damit die Anzeige bzw. die Kostüme auch wirklich mit der Variable geändert werden, haben wir in einer "forever"-Klammer jeweils ein "if 'Leben=x'" mit einem "switch to costume x" kombiniert. In dem Moment, in dem die Variable "Leben" auf null gesetzt wird, wird zum Einen das Kostüm geändert und zum Anderen "Game Over" gebroadcasted, da das Spiel in dem Moment als verloren gilt. 

![grafik](https://user-images.githubusercontent.com/88386040/144746019-f089ae7d-07c6-4f38-abb3-a9386e4ad837.png)

Die Anzeige soll auch vor Spielbeginn und nach einem Gewinn versteckt werden, welches durch folgende Blöcke gewährleistet wird:

![grafik](https://user-images.githubusercontent.com/88386040/144746073-aa6ec3e1-a94d-4bf8-921c-05a619783f58.png)

### Game Over 

Damit das "Game Over" erst angezeigt wird, sobald der Dino alle Leben verloren hat, haben wir ein "hide" folgend auf ein "when Flagge clicked" und auf ein "when I receive 'Spielstart'" eingebaut. Damit sie dann jedoch eingebaut wird, haben wir den folgenden Block gebaut, der ab Anfang des Spielstarts gilt. Diseser gilt durch einen "if 'Leben=0'" wirklich nur in dem Moment, in dem alle Leben verloren wurden. Nach 0,1 Sekunden Wartezeit wird das Costume "try" für try again erst auf die richtige Größe und Koordinate gesetzt und dann angezeigt. Daraufhin werden durch den Block "stop all" alle anderen Befehle gestoppt, damit auch keine Meteoriten mehr fallen. 

![grafik](https://user-images.githubusercontent.com/88386040/144746905-a73ea843-36a6-4af3-a975-b6eeaf121fba.png)

![grafik](https://user-images.githubusercontent.com/88386040/144746812-5345d755-242b-435c-a4ee-045015b8ed69.png)

Zudem haben wir einen weiteren Block erstellt, der es ermöglichen sollte durch das klicken auf "Game Over, try again" das Spiel erneut zu starten. Dazu haben wir den gleichen Block wie bereits erklärt genutzt, doch das "when I receive Spielstart" durch ein "when I am clicked" und "broadcast Level Beginn" ersetzt. 

![grafik](https://user-images.githubusercontent.com/88386040/144747036-8191111b-5776-460c-ab45-96643ab28e28.png)

### Win 

Das Spiel gewinnen kann man indem man 45 Sekunden des Spieles überlebt, ohne von Meteoriten getroffen zu werden. Dazu mussten wir zuerst einen Timer erstellen, der durch die Variable "Timer" entsteht. Diesem wird durch die Blöcke "wait 1 secs" und "change 'Timer' by -1" sekundenweise geringer. Sobald der Timer abgelaufen ist, also die Variable auf 0 gesetzt wird, wird "WIN" gebroadasted.

![grafik](https://user-images.githubusercontent.com/88386040/144747507-0fb799dc-6d41-4aca-8c90-2ea0999cfe66.png)

Wenn das Spiel beginnt wird das Costume mittig positioniert, die Größe agepasst und es wird versteckt. Auch wenn die grüne Flagge gedrückt wird ist es versteckt, denn es soll erst angezeigt werden, wenn "WIN" received wird und der Dino noch Leben hat. 

Genau wie beim "Game Over" kann es angeklickt werden um das Spiel erneut zu starten und den Timer zurückzusetzen. Der Block ist hierbei genau so aufgebaut und funktioniert somit auch auf die gleiche Weise.

![grafik](https://user-images.githubusercontent.com/88386040/144747659-208fa8b0-7b39-4797-b5e3-79dc066f9eb1.png)

Sobald "WIN" gebroadcasted wird, wird auch der Boden versteckt, weshalb sich folgender "Gewinnbildschirm" ergibt:

![grafik](https://user-images.githubusercontent.com/88386040/144747304-85dbac96-032a-4682-ba95-25201fba795d.png)














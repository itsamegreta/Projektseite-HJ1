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

Spielfigur: Dinosaurier 

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














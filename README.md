Conways Game of Life:

Dieses spielt wurde im Jahr 1970 von John Conway entwickelt

Sie wird auf einem Spielfeld mit Zeilen und Spalten gespielt

Jede Zelle ist eine "Zelle" im Spiel die den Zustand lebendig(1) oder tot(0) haben kann

Jede Zelle hat acht Nachbaren und der nächste Zustand hängt von denen ab:

Wenn eine lebendige Zelle 2 bis 3 lebendige Nachbaren hat, so wird dieser weiter leben

Wenn eine tote Zelle exakt drei Nachbaren hat, so wird dieser wiederbelebt

Wenn eine lebendige Zelle weniger als 2 Nachbaren hat, stirbt dieser 

Wenn eine lebendige Zelle mehr als 3 Nachbaren hat, stirbt dieser auch

                   
All diese Bedingungen passieren in einem Zug, d.h. zum Beispiel, dass wenn eine lebendige Zelle 4 Nachbaren hat und eines seiner Nachbaren nur einen Nachbar, so werden beide Sterben


Optimierungen:

1: Den Funktionsaufruf initSpielfeld löschen und das Spielfeld direkt oben beim Array auf spielfeld setzen, denn es ist unnötig und zeitverschwenderisch das man es erst später mit einem Funktionsaufruf macht.

2: Alle ints auf char umändern weil wir es nur mit einzelnen Zeichen (character) zu tun haben. Daher ints überflüssig!

3: Funktion Prueferegeln überarbeiten, anstatt vielen ifs eine Switch verwenden weil dies weniger Aufwand braucht und für diesen Fall passt, da wir überprüfen wie viele Nachbaren leben.

4: Die X,Y anzeige löschen da dies sehr unnötig Zeit frisst, außerdem ist diese Anzeige im origninalem Spiel nicht existent.

5: Funktion zaehllebende ändern, eine For-Schleife verbraucht wehr viel Zeit. Dies liegt daran, dass es nach jedem durchlauf die Variable überprüft und inkrementiert/dekrementiert. Und bei Zwei Fors kann man sehr viel Zeit verschwenden. Einfacher gehts, indem man einfach die Nachbarn addiert. Dieser Funktionsteil wird danach in die Funktion findnachbar geaddet. Allgemein werden alle Funktionenauurufe gelöscht und alle Funktionen werden im main ausgeführt. Dass ist nicht ideal, aber effizient für das Programm. Ein wichtiger Punkt ist auch, dass im IF in der For-Schleife und beim flag multipliziert wird. Das Programm multipliziert jedoch nicht sondern addiert alles einzeln. Dies verbraucht auch unnötig sehr viel Zeit, deswegen Multiplikationen vermeiden!!

6: Funktion findNachbar optimieren, hier werden die For-Schleifen optimiert, die gekürzte zaehllebende Funktion und die Pruefregel Funktion beigefügt. Hier verwenden wir Hilfsvariablen für die Position der Nachbaren, die wir in Ifs. Als Beispiel fragen wir mit der IF ob das x lebendig ist, falls, dass der falls ist wird das xr (right) auf 0 gesetzt. Somit können wir alle acht Nachbaren überprüfen, ob sie lebendig sind oder nicht.

Fortschritt:

Anfangsprogramm	                                                        56,3s
Anfangsprogramm mit Kopileroptimierung	                                42s
initSpielefeld gelöscht	                                                40,4s
pruefeRegeln überarbeitet	                                              38,5s
X,Y Anzeige links oben entfernt	                                        24s
Zähllebende und FindNachbar zusammengefasst, Funktionsaufrufe entfernen	7,2s
Datentypen optimert, Funktionsaufruf pruefeRegeln entfernt	            5,3s
Datentypen optimiert, spielfeld auf char geändert	                      4,7s

![image](https://github.com/minigimli/ConwaysGameSimulation/assets/128684904/d95bf787-be9b-4fd2-aefb-c55f7387c58a)


![image](https://github.com/minigimli/ConwaysGameSimulation/assets/128684904/7da33038-ba0d-4ebe-a495-03a840458baf)


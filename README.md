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

1: Den Funktionsaufruf initSpielfeld löschen und das Spielfeld direkt oben beim Array auf spielfeld setzen, denn es ist unnötig das man es erst später mit einem Funktionsaufruf macht.

2: Alle ints auf char umändern weil wir es nur mit einzelnen Zeichen (character) zu tun haben.

3: 




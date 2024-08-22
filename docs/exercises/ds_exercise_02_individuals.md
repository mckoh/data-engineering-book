# Individualaufgaben: Graphenartige Datenstrukturen mit Neo4J/Cypher

In dieser Sektion habt ihr die Möglichkeit, euch individuell in der Thematik zu vertiefen. Unterhalb findet ihr Aufgaben, die auf das aufbauen, was wir im Mega-Tutorium gemeinsam besprochen haben. Die Aufgaben sind in drei Gruppen – Einfach, Mittel, Herausfordernd – unterteilt und geben unterschiedlich viele Punkte. Insgesamt solltet ihr für dieses Übungsblatt **25 Punkte** erreichen – wie sich diese zusammensetzen ist egal.

## Übung 2a: Graph erstellen <span style="color:#33FF7D ">Einfach</span> (10 Punkte)

**Szenario:** Paul kennt Bill und Sarah. Bill kennt Amir und Data Science. Sarah kennt Rico und mag Amir.

## Übung 2b: Graph erstellen <span style="color:#FFB533 ">Mittel</span> (15 Punkte)

**Szenario:** Paul Fen aus den USA kennt Bill Fu aus UK, der wiederum seit 15.01.2017 Data Scientist ist. Paul arbeitet seit 05.11.2009 als Software Engineer und kennt außerdem Sarah Klein aus Österreich, die auch ihn kennt. Sarah war von 01.01.2010 bis 18.04.2013 Software Engineer und arbeitet seither als Data Scientist. Über diese Tätigkeit hat Sie auch Amir kennengelernt, der auch sie kennt und seit 21.10.2012 als Data Scientist arbeitet. Amir mag Rico, die als Software Engineer arbeitet. Sarah kennt Rico ebenfalls und mag außerdem Bill.

## Übung 2c: Graph erstellen <span style="color:#C70039">Herausfordernd</span> (25 Punkte)

In den [Downloads](../downloads/starwars.sql) findet ihr ein DDL/DML Skript für die MariaDB-Datenbank 'starwars'. Dort sind all Interaktionen von Star-Wars-Charakteren aus Episode I abgebildet. Überführt diese Datenstruktur mit Hilfe von Cypher (und Neo4J) in einen Graphen. Bildet dabei alle Charaktere und alle Interaktionen ab.

Wie ihr das Überführen löst, ist eure Sache. Ihr könnt hierfür (a) ein python-Skript basteln, das die Daten in Cypher überführt oder (b) eure Daten via CSV-Files von A nach B transferieren ([Siehe Neo4J-Tutorial](https://neo4j.com/developer/guide-importing-data-and-etl/)). 

## Übung 2d: Graph erstellen <span style="color:#C70039">Herausfordernd</span> (25 Punkte)

Auf [github](https://github.com/evelinag/StarWars-social-network/tree/master/networks) findet ihr die Rohdaten zum Star-Wars-Beispiel aus Aufgabe 3b im JSON Format. Erstellt euch ein Python-Skript mit dessen Hilfe Ihr die Daten von dort parsen könnt und anschließend in Neo4J einfügt.

## Übung 2e: Graph analysieren <span style="color:#FFB533 ">Mittel</span> (15 Punkte)

Verwendet den Graphen, den ihr in Übung 2a entwickelt habt und entwickelt darauf Cypher-Abfragen zu folgenden Aufgabenstellungen.

* Listet alle Personen auf, die euer Graph enthält.
* Gebt die Anzahl der Personen in eurem Graph zurück.
* Gebt die Anzahl der Beziehungen in eurem Graph zurück.
* Listet alle Beziehungen vom Typ "knows" und deren teilnehmende Entitäten auf.
* Listet alle Beziehungen vom Typ "knows" auf, an denen ausschließlich Personen beteiligt sind.
* Listet alle Beziehungen vom Typ "knows" auf, an denen eine Person und ein Nicht-Personen-Objekt beteiligt ist.

## Übung 2f: Graph erstellen <span style="color:#C70039">Herausfordernd</span> (25 Punkte)

Verwendet den Graphen, den ihr Übung 2b entwickelt habt und entwickelt darauf Cypher-Abfragen zu folgenden Aufgabenstellungen.

* Listet alle Personen außer Sarah auf, die euer Graph enthält.
* Gebt die Anzahl der Personen außer Bill in eurem Graph zurück.
* Listet alle Personen, für die das "nationality" Attribut nicht gesetzt wurde.
* Listet alle Personen, die jemanden kennen der Data Scientist ist.
* Listet alle Kontakte von Sarah.
* Listet alle "is a" Relationen, für die kein "to" Datum angegeben wurde
* Findet den Data Scientist, der am längsten tätig ist.


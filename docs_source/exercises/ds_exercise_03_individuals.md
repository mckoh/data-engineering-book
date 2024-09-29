# Individualaufgaben: Graphenartige Datenstrukturen mit Neo4J/Cypher

In dieser Sektion habt ihr die Möglichkeit, euch individuell in der Thematik zu vertiefen. Unterhalb findet ihr Aufgaben, die auf das aufbauen, was wir im Mega-Tutorium gemeinsam besprochen haben. Die Aufgaben sind in drei Gruppen – Einfach, Mittel, Herausfordernd – unterteilt und geben unterschiedlich viele Punkte. Insgesamt solltet ihr in diesem Übungsblatt **25 Punkte** erreichen – wie sich diese zusammensetzen ist egal.

## Übung 3a: Datenmodellierung <span style="color:#33FF7D ">Einfach</span> (10 Punkte)

Setzt die beiden unterhalb angeführten Bücher mit all ihren Eigenschaften in JSON um und fügt diese anschließend mit Hilfe Robo3T und der Abfragesprache von MongoDB auf eurem MongoDB-DBS ein.

* [Buch 1](https://isbnsearch.org/isbn/9781449373320)
* [Book 2](https://isbnsearch.org/isbn/9780202302607)

> **Info:** Bei den Büchern werden auf der Webseite mehrere Preise ausgewiesen. Hier reicht es, wenn ihr einen Preis im JSON-Objekt erfasst. Wer sich challengen möchte, kann natürlich versuchen das Objekt auch mit mehreren, unterschiedlichen Preisen zu erfassen. Das ist aber optional.

## Übung 3b: Datenmodellierung <span style="color:#FFB533 ">Mittel</span> (15 Punkte)

Setzt die beiden unterhalb angeführten LinkedIn-Profile mit all ihren Eigenschaften als JSON-Objekte um und fügt diese anschließend mit Hilfe von Robo3T und der Abfragesprache von MongoDB auf eurem MongoDB-DBS ein. Beschränkt euch bei der Modellierung auf Berufserfahrung, Ausbildung, Bescheinigungen/Zertifikate, Interessen, Aktivitäten und die Basisdaten des Profils.

* [Melinda Gates](https://www.linkedin.com/in/melindagates/)
* [Bill Gates](https://www.linkedin.com/in/williamhgates/)

## Übung 3c: Abfragen <span style="color:#FFB533 ">Mittel</span> (15 Punkte)

Verwendet die Collection, die ihr in Aufgabe 3a erzeugt habt und entwickelt Abfragen, um die folgenden Fragestellungen zu beantworten. Sollten manche der vorgeschlagenen Aufgaben nicht mit den von euch entwickelten JSON-Objekten kompatibel sein, überlegt euch einfach eine passende alternative Abfrage.

* Gebt alle Objekte in der Collection aus.
* Gebt das Buch mit der ISBN 9781449373320 aus.
* Gebt alle Bücher aus, deren Preis über $45,- liegt.
* Gebt alle Bücher des "O'Reilly Media" Verlags aus, die "Martin Kleppmann" geschrieben hat.
* Gebt alle Bücher von Autor:innen mit dem Vornamen "Martin" aus.
* Gebt alle Bücher und die jeweilige Anzahl von Autor:innen aus.
* Gebt die Gesamtzahl an Büchern an, die in der Collection gespeichert sind.

## Übung 3d: Abfragen <span style="color:#C70039">Herausfordernd</span> (25 Punkte)

Verwendet die Collection, die ihr in Aufgabe 3b erzeugt habt und entwickelt Abfragen, um die folgenden Fragestellungen zu beantworten. Sollten manche der vorgeschlagenen Aufgaben nicht mit den von euch entwickelten JSON-Objekten kompatibel sein, überlegt euch einfach eine passende alternative Abfrage.

* Gebt alle Personen mit dem Vornamen "Melinda" aus.
* Gebt die Gesamtzahl an Objekten, die in der Collection gespeichert sind, aus.
* Gebt alle Personen der Collection aus, die sich nicht für Bill Gates interessieren.
* Gebt alle Interessen aus, die in der Collection vorkommen und ermittelt wie oft diese vorkommen.
* Ermittelt jene Organisation, die bei den Berufserfahrungen im der Collection am häufigsten vorkommt.
* Ermittelt die durchschnittliche Job-Verweildauer aller Personen, die in der Collection gespeichert sind.

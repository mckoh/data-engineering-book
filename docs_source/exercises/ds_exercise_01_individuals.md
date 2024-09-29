# Individualaufgaben:  Relationale Datenstrukturen mit SQL

In dieser Sektion habt ihr die Möglichkeit, euch individuell in der Thematik zu vertiefen. Unterhalb findet ihr Aufgaben, die auf das aufbauen, was wir im Mega-Tutorium gemeinsam besprochen haben. Die Aufgaben sind grob in drei Gruppen – Einfach, Mittel, Herausfordernd – unterteilt und geben unterschiedlich viele Punkte. Insgesamt solltet ihr für dieses Übungsblatt 50 Punkte erreichen – wie sich diese zusammensetzen ist egal.

## Übung 1a: Datenmodellierung <span style="color:#33FF7D ">Einfach</span> (15 Punkte)

**Szenario:** Zu Analysezwecken soll eine Kundendatenbank aufgebaut werden, in der Kunden und deren Kontaktdaten erfasst werden können. Außerdem sollen in der Datenbank sämtliche Warenkörbe (Kaufdatum, bestellte Artikel, Bestellmengen, Bestellsumme) erfasst werden.

## Übung 1b: Datenmodellierung <span style="color:#FFB533 ">Mittel</span> (20 Punkte)

**Szenario:** Eine Universität möchte zum Zweck der Implementierung von Learning Analytics eine Datenbank aufbauen, in der Daten über Studierende und Lektor:innen gespeichert werden. Für die Auswertung sollen insbesondere Kursbelegungen, Noten und Anwesenheit erfasst werden. Darüber hinaus soll die Datenbank auch Aktivitäten erfassen können, die in der hochschuleigenen Lernplattform (Moodle) gesetzt werden.

## Übung 1c: Datenmodellierung  <span style="color:#C70039">Herausfordernd</span> (30 Punkte)

**Szenario:** Ein Hersteller von Wärmepumpen stattet all seine Maschinen mit Sensoren aus. Je nach Maschinengröße können dabei unterschiedlich viele Sensoren verbaut sein – Maschinen eines Typs sind immer gleich ausgestattet – einerseits aus Sicht der Sensorik, andererseits auch aus Sicht des generellen Aufbaus der Maschine. Für jeden Maschinentyp liegt eine detaillierte Stückliste und Zusammenbaustruktur (Bauteile können aus verschiedenen anderen Bauteilen aufgebaut sein) vor, die ebenfalls erfasst werden soll. Maschinen können Kund:innen des Herstellers zugeordnet werden, um einerseits (a) den Verkaufsprozess und (b) andererseits alle Aftersales-Prozesse (Wartung, Störungsbehebung usw.) abwickeln zu können. Randinformation: Derzeit sind 3000 Maschinen im aktiven Einsatz und schicken ca. alle 15 Sekunden Daten von ca. 250 Sensoren (und anderen Log-Kanälen). In den nächsten 7 Jahren wird sich die Anzahl der angeschlossenen Maschinen in etwa verdoppeln.

## Übung 1d: Data Definition (DDL)  <span style="color:#33FF7D ">Einfach</span> (15 Punkte)

Implementiert das Datenmodell, das ihr in Übung 1a entwickelt habt in MariaDB mit Hilfe von SQL.

## Übung 1e: Data Definition (DDL)  <span style="color:#FFB533">Mittel</span> (20 Punkte)

Implementiert das Datenmodell, das ihr in Übung 1b oder 1c entwickelt habt in MariaDB mit Hilfe von SQL. Verwendet dazu euren lokalen MariaDB-Server. Berücksichtigt bitte bei der Implementierung eurer Datenbank, welche Spalten besonders häufig abgefragt werden und legt entsprechende Indexe fest.

## Übung 1f: Data Manipulation (DML)  <span style="color:#33FF7D ">Einfach</span> (15 Punkte)

Erzeugt für mindestens 5 Entitätstypen eures implementierten Modells (aus Aufgabe d oder e) jeweils 10 oder mehr Beispieldatensätze und ladet diese mittels SQL in eure Datenbank. Ändert anschließend gezielt Datensätze mit Hilfe von SQL UPDATE Operationen ab. Löscht außerdem je einen Datensatz mit Hilfe von SQL.

## Übung 1g: Data Querying (DQL)  <span style="color:#FFB533">Mittel</span> (20 Punkte)

Ich habe euch [online](../downloads/machines.sql) eine vollständige MariaDB-Datenbank bereitgestellt. Diese Datenbank bildet bereits ein vollwertiges relationales Schema ab und enthält auch Datensätze. Implementiert diese Datenbank auf eurem lokalen MariaDB-Server. Erstellt anschließend unter Verwendungen dieser Datenbank SQL-Abfragen, um die folgenden Fragestellungen zu bedienen:

* Die Verkaufsabteilung benötigt eine Liste aller erfassten Maschinen (Lösung: 3000 Zeilen).
* Die Verkaufsabteilung möchte dieselbe Liste (wie oben), nur diesmal eingeschränkt auf die Attribute Maschinennummer und Installationsdatum (Lösung: 3000 Zeilen, 2 Spalten).
* Die Instandhaltungsabteilung möchte Informationen über die Maschine mit der Maschinennummer 912177 (Lösung: 1 Zeile, 7 Spalten). 
* Die Instandhaltungsabteilung möchte eine Liste aller Maschinen mit den Nummern 912177, 912621 oder 910487 (Lösung: 3 Zeile, 7 Spalten). 
* Ein Wartungstechniker benötigt alle Informationen über Maschine Nummer 910476 und die darin verbauten Sensoren (Lösung: 6 Sensoren).
* Die Entwicklungsabteilung möchte eine Liste aller Maschinen, in denen der Sensor mit dem Kurznamen MPU9250 verbaut wurde (Lösung: 1468 Zeilen).

## Übung 1h: Data Querying (DQL)  <span style="color:#C70039">Herausfordernd</span> (30 Punkte)

Ich habe euch [online](../downloads/machines.sql) eine vollständige MariaDB-Datenbank bereitgestellt. Diese Datenbank bildet bereits ein vollwertiges relationales Schema ab und enthält auch Datensätze. Erstellt unter Verwendungen dieser Datenbank SQL-Abfragen, um die folgenden Fragestellungen zu bedienen:

* Die Produktionsabteilung möchte wissen, welche Sensortypen noch nie in einer Maschine verbaut worden sind. Herausforderung: Löst dieses Problem auf zwei unterschiedliche Arten (Lösung: 6, 7).
* Die Marketingabteilung möchte anlässlich der 100-Jahr-Feier wissen, welchen Kund:innen die älteste bzw. jüngste Maschine gehören und wie viele Betriebsstunden diese Maschinen im Einsatz sind. Herausforderung: Überführt diese Frage in eine Sicht (aka View) (Lösung: 910604, 911197, 911500, 911591, 912734).
* Die Entwicklungsabteilung möchte gerne die durchschnittliche Zahl an Log-Einträgen der ältesten und jüngsten Maschine (Lösung: 73.75).
* Die Entwicklungsabteilung möchte gerne die Gesamtzahl an Logeinträgen, die über die Jahre gespeichert wurden (Lösung: 227566).
* Die Produktionsabteilung möchte gerne eine Liste der Hauptbauteile aus denen Maschinen des Typs 1 bestehen (Bauteile, die selbst nicht mehr Bestandteil größerer Bauteilgruppen sind) (Lösung: 127 Zeilen).
* Die Produktionsabteilung möchte außerdem wissen, aus welchen Unterbauteilen, Unter-Unterbauteilen usw. sich das Bauteil mit der Identifikationsnummer 1 zusammensetzen und wie die Zusammenbaukette dieses Bauteils im Detail aussieht. Hier wäre insbesondere interessant zu wissen, welche Bauteile auf welcher Ebene zusammengebaut werden müssen (Lösung: Die Bauteile 2, 3, 4, 6, 8, 9, 12, 14, 17, 21 und 32; auf 4 Level).
* Die Entwicklungsabteilung möchte gerne eine Sicht (aka View), die das relationale Schema der Log-Daten (inklusive Maschinen-, Sensor-, Sensortyp- und Kundendaten) in ein Wide-Colum-Store Schema (alle Daten in einer Tabelle) überführt und die unterhalb folgenden Analysen unterstützt. Hinweis: Um die Abfrageperformanz zu gewährleisten kann es nötig sein, Normalisierungsanforderungen aufzugeben (Lösung: Variiert nach Schwerpunkt).
a. Analyse von Sensorwerten nach Wochentagen
b. Analyse von Sensorwerten nach Feiertagen
c. Vergleich von Sensorwerten, die zur gleichen Zeit aufgezeichnet wurden, in einer Zeile
d. Analyse von Sensorwerten nach Maschine
e. Analyse von Sensorwerten nach Standort
 

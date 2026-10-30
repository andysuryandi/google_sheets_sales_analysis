# PeakFlow – Vertriebsanalyse Q1 2025

Abschlussprojekt zur Analyse von Vertriebsdaten mit **Google Sheets**. Das Projekt umfasst Datenbereinigung, deskriptive Statistik, Pivot-Tabellen und Visualisierungen.

## Projektziel

Die Analyse untersucht folgende Fragen:

- Wie entwickelt sich der Umsatz im ersten Quartal 2025?
- Welche Regionen und Produktkategorien erzielen die höchsten Umsätze?
- Welche Vertriebsmitarbeiter fallen durch Dealanzahl und Dealgröße auf?
- Wie beeinflussen große Einzelabschlüsse die Umsatzverteilung?

## Daten und Bereinigung

Der Ausgangsdatensatz enthält 254 Datensätze. Nach der Bereinigung verbleiben **250 eindeutige Geschäfte**.

Durchgeführte Schritte:

- Zwei Testdatensätze entfernt.
- Zwei doppelte Datensätze anhand der DealID entfernt.
- Schreibweisen von Kategorien und Regionen vereinheitlicht.
- Überflüssige Leerzeichen und nicht druckbare Zeichen bereinigt.
- Zahlenwerte in ein auswertbares Format umgewandelt.
- Umsatz als **Stückzahl × Stückpreis** neu berechnet.

Die ursprünglichen Daten bleiben in einem separaten Tabellenblatt erhalten.

### Datenkontext

Die im Datensatz verwendeten Kunden- und Mitarbeiternamen sind fiktiv. Die Daten werden im Rahmen eines Abschlussprojekts analysiert.

## Wichtigste Ergebnisse

| Kennzahl | Ergebnis |
|---|---:|
| Anzahl der Geschäfte | 250 |
| Gesamtumsatz | 364.634,55 $ |
| Durchschnittlicher Umsatz pro Geschäft | 1.458,54 $ |
| Median des Umsatzes pro Geschäft | 386,76 $ |

### Erkenntnisse

- **Große Einzelabschlüsse prägen das Gesamtergebnis.** Der Durchschnitt liegt deutlich über dem Median, was auf eine rechtsschiefe Umsatzverteilung hinweist.
- **Enterprise Plans tragen überproportional zum Umsatz bei.** Sie machen 23 von 250 Geschäften aus und erzielen rund 46,9 % des Gesamtumsatzes.
- **APAC erzielt den höchsten regionalen Umsatz** mit 120.025,49 $.
- **Januar ist der umsatzstärkste Monat** mit 186.600,12 $. Im Februar fällt der Umsatz auf 85.430,35 $ und steigt im März auf 92.604,08 $.
- **Marcus Johnson erzielt den höchsten Gesamtumsatz** mit 78.951,97 $ bei 37 Geschäften.

Die Ergebnisse beschreiben das untersuchte Quartal. Sie erlauben allein keine Aussagen über langfristige Trends oder die Ursachen der Unterschiede.

## Werkzeuge und Methoden

- Google Sheets
- Datenbereinigung mit Text- und Zahlenfunktionen
- Bedingte Aggregationen, Filter und Sortierungen
- Deskriptive Statistik, einschließlich Median, Quartilen und Standardabweichung
- Pivot-Tabellen
- Linien-, Balken- und Streudiagramme sowie Histogramm

## Visualisierungen

Die drei Ansichten ergänzen sich: Der Mitarbeitervergleich zeigt die Umsatzverteilung im Team, der Monatsverlauf ordnet das Quartal zeitlich ein und das Histogramm macht die ungleiche Verteilung der Dealgrößen sichtbar.

### Umsatz nach Vertriebsmitarbeiter
![Absteigend sortiertes Balkendiagramm des Gesamtumsatzes nach Vertriebsmitarbeiter](umsatz-vertrieb.png)

**Wer trägt den höchsten Umsatz bei?** Marcus Johnson führt die Umsatzrangliste an, gefolgt von Nina Petrov. Die sortierten horizontalen Balken erleichtern den direkten Vergleich. Gesamtumsatz allein erklärt jedoch weder Dealanzahl noch Dealgröße oder die Ursachen der Unterschiede.

### Umsatzentwicklung im ersten Quartal
![Liniendiagramm mit hohem Januarumsatz, Rückgang im Februar und leichtem Anstieg im März](umsatz-monat.png)

**Wie verteilt sich der Umsatz über das Quartal?** Auf den umsatzstärksten Januar folgt ein deutlicher Rückgang im Februar und ein leichter Anstieg im März. Drei Monatswerte beschreiben dieses Quartal, belegen aber keinen langfristigen Trend.

### Verteilung der Dealgrößen
![Histogramm mit vielen Geschäften im unteren Größenbereich und wenigen großen Abschlüssen](deal-verteilung.png)

**Warum reicht der Durchschnitt allein nicht aus?** Die meisten Geschäfte liegen im unteren Größenbereich; wenige große Abschlüsse bilden einen langen rechten Ausläufer. Das passt zum dokumentierten Unterschied zwischen Durchschnitt und Median. Die breite erste Klasse fasst viele Geschäfte zusammen und lässt Unterschiede innerhalb dieser Gruppe nicht erkennen.

**Empfehlung für LinkedIn:** Das Balkendiagramm `umsatz-vertrieb.png` eignet sich unter den vorhandenen Bildern am besten als Einstieg: klare Rangfolge, gut vergleichbare Balken und eine unmittelbar erkennbare Aussage. Das Histogramm ergänzt die analytische Story zur Dealgröße. Alle drei Bilder sind unveränderte Tabellen-Screenshots; Tabellenränder und kleine Beschriftungen begrenzen die Lesbarkeit auf dem Smartphone.

## Aufbau der Arbeitsmappe

| Tabellenblatt | Inhalt |
|---|---|
| `peakflow_q1_2025_dirty` | Unveränderte Rohdaten |
| `Geschäfte` | Bereinigte Daten und Hilfsberechnungen |
| `Zusammenfassung` | Kennzahlen und Auswertungen nach Monat, Region und Kategorie |
| `Pivot-Tabellen` | Auswertungen nach Vertriebsmitarbeiter, Kategorie und Region |
| `Top-Performer` | Ranglisten und größte Einzelabschlüsse |
| `Diagramme` | Visualisierungen und Hilfstabellen |
| `README` | Dokumentation der Bereinigung und Ergebnisse |

## Hinweise zur Nutzung

### Analyse in Google Sheets nachvollziehen

Die Analyse wurde in Google Sheets erstellt. Für die Prüfung der ursprünglichen Formeln, Pivot-Tabellen und Diagramme ist die native Originaldatei die Referenz.

**Offener Punkt:** Ein verifizierter, schreibgeschützter Link zur Google-Sheets-Originaldatei ist hier noch nicht hinterlegt. Bis dieser ergänzt ist, ist die direkte Prüfung des Originals über dieses Repository nicht möglich.

Sobald der geprüfte Link verfügbar ist:

1. Die Originaldatei mit Leseberechtigung öffnen. Für eigene Berechnungen bei erlaubter Kopierfunktion über **Datei → Kopie erstellen** eine eigene Kopie anlegen.
2. Im Blatt `peakflow_q1_2025_dirty` die Rohdaten und im Blatt `Geschäfte` die dokumentierten Bereinigungsschritte sowie die Umsatzberechnung nachvollziehen.
3. Die Kennzahlen in `Zusammenfassung` mit den oben dokumentierten Ergebnissen vergleichen. Danach `Pivot-Tabellen`, `Top-Performer` und die zugrunde liegenden Bereiche in `Diagramme` prüfen.
4. Bei eigenen Änderungen Eingabedaten, Filter und verwendete Bereiche festhalten und prüfen, ob Kennzahlen, Pivot-Auswertungen und Diagramme die Änderungen korrekt übernehmen.

### XLSX-Export und Grenzen der Excel-Nutzung

Die unten verlinkte XLSX-Datei ist ein Export der Google-Sheets-Arbeitsmappe. Google-Sheets-spezifische Formeln und Pivot-Tabellen können in Excel abweichend funktionieren; auch Formatierungen und Diagrammdarstellungen können sich unterscheiden. Eine vollständige Neuberechnung in Excel wurde bisher nicht bestätigt. Angezeigte Werte allein bestätigen daher nicht, dass sämtliche Formeln und Auswertungen in Excel korrekt neu berechnet werden.

Für eine Prüfung in Excel eine lokale Kopie öffnen, die Arbeitsmappe vollständig neu berechnen und Formelfehler, Pivot-Datenquellen sowie Diagrammbereiche kontrollieren. Anschließend die Ergebnisse mit den dokumentierten Kennzahlen und – sobald zugänglich – dem Google-Sheets-Original abgleichen. Dies ist eine Prüfanleitung, keine Bestätigung einer bereits erfolgreichen Excel-Validierung. Ein erneuter Import der XLSX-Datei in Google Sheets ersetzt nicht die Prüfung der nativen Originaldatei.

## Projektstatus

Die Projektdatei und ausgewählte Visualisierungen sind im Repository enthalten. Die Analyse und ihre Ergebnisse sind dokumentiert.

## Projektdatei

[Arbeitsmappe herunterladen](PeakFlow_Suryandi_Suryandi.xlsx)

## Autor

Suryandi Suryandi

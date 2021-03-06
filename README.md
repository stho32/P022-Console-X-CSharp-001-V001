# Ein Scanner/Parser, der nach einer Konfiguration Code-Dateien nach JSON umformt und für einfache Analysen bereitstellt

Eine Challenge aus https://github.com/stho32/Collection-Of-Challenges

[![build](https://github.com/stho32/CH022-Console-X-CSharp/actions/workflows/dotnet.yml/badge.svg)](https://github.com/stho32/CH022-Console-X-CSharp/actions/workflows/dotnet.yml)

## Anforderungen

- [X] (A001) Der Scanner enthält Definitionen für 
  - [X] Token, die aus einem Set von Zeichen bestehen können, z.B. Whitespaces (Space, Tab, ...)
  - [X] Token, die Begrenzer haben, z.B. "/*" -> "*/" als Kommentar
  - [X] Token, die mit optionalen Zeichen beginnen können, gefolgt von einem validen Set, z.B. Zahlen (+/- dann 0123456789.)
  - [..] ggf. mehr
- [X] (A002) Der Scanner hat interne Vordefinitionen für folgende Sprachen:
  - [X] (A003) C#
  - [X] (A004) T-SQL

- [X] (A005) Das Ausgabeformat des Scanners ist JSON.

- [ ] (A006) Es gibt die Möglichkeit einige Regeln zu konfigurieren, die Token mit weiteren Meta-Informationen annotieren
  - [ ] (A007) Es gibt eine Regel, die alle Bezeichnungen nach FROM, INSERT INTO und UPDATE als Tabellen-Namen identifiziert

- [ ] (A008) Die Anwendung kann mit einem Dateifilter auf ein Verzeichnis angesetzt werden und liefert auf einen Schlag Ergebnisse für alle matchende Dateien innerhalb des Verzeichnisses, also z.B. alle \*.cs-Dateien werden geparst
- [ ] (A009) In den JSON-Ausgabedaten ist nachvollziehbar, welche Ergebnisse zu welcher Datei gehören

- [ ] (A010) Man kann folgende Fragen effizient beantworten:
  - [ ] (A011) Welche Dateien beinhalten Referenzen auf die Tabelle "HelloWorld"
  - [ ] (A012) Welche Stored-Procedures gibt es?
  - [ ] (A013) Welche Stored-Procedures beinhalten Referenzen auf die Tabelle "HelloWorld"
  - [ ] (A014) Welche Klassen sind deaklariert?
  - [ ] (A015) Von welchen Klassen und Schnittstellen sind die Klassen abgeleitet (nur 1 Stufe tief, also die unmittelbaren Vorgänger)
  - [ ] (A016) Von welchen Klassen und Schnittstellen sind die Klassen abgeleitet, wenn man die Hierarchie auflöst, d.h. wenn z.B. Scanner von ScannerBase abgeleitet ist und die Schnittstelle IScanner implementiert, dann soll bei Scanner das Interface IScanner als Vorfahre angezeigt werden.

Beispieldateien sind anbei.

## Zusatzanforderungen

Es gelten die generellen Zusatzanforderungen aus [Generelle-Zusatzanforderungen.md](../Generelle-Zusatzanforderungen.md).

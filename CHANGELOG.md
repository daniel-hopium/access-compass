# Changelog

Alle nennenswerten Änderungen am Rechte-Kompass. Die Einträge beschreiben, was das Projekt
danach kann bzw. was sich für den Nutzer ändert – kein Commit-Protokoll.

**Regel:** Jeder Commit bekommt seinen Eintrag, im selben Commit. Neues kommt oben unter
„Unveröffentlicht“ dazu; beim Release wird daraus ein Abschnitt mit Versionsnummer und Datum.

Kategorien: **Neu** (neue Funktionen), **Verbessert** (bestehendes Verhalten), **Behoben**
(Fehler), **Intern** (Struktur, Tooling, nicht sichtbar).

## Unveröffentlicht

### Neu
- Hell/Dunkel-Umschalter im Kopf: Klick legt das Design fest und merkt es sich, ohne Klick
  gilt weiter die Systemeinstellung.
- Breite-Umschalter neben Sonne/Mond: Die breite Ansicht lässt die Lektion die ganze Spalte
  neben der Liste füllen statt 48rem; unter 1280px ist der Knopf ausgeblendet.
- In der breiten Ansicht lässt sich die Lektion am Griff rechts schmaler oder breiter ziehen
  (mindestens 48rem). Doppelklick stellt die ganze Breite her, per Tastatur gehen ←/→, Pos1
  und Ende. Die gezogene Breite wird gemerkt.
- Erste Fassung: 53 Lektionen in sieben Kapiteln zu Login und Rechten – Grundlagen,
  OAuth 2.0 & OpenID Connect, Autorisierung denken, Zugriffsmodelle (RBAC, ABAC, PBAC,
  ReBAC), Angular 22, Spring Boot & Spring Security, Ende zu Ende & Angriffe.
- Durchgehendes Beispiel Nordwind GmbH: Per „Angemeldet als“ die Person wechseln, und jedes
  Live-Beispiel zeigt, was sie sehen und tun darf.
- Sequenzdiagramme, Schritt-für-Schritt-Abläufe, Token zum Signieren und Prüfen, Quizfragen
  und ein Glossar; Deutsch und Englisch, hell und dunkel, breite Ansicht.

# Automations-Plan für System-Resilienz

Dieses Dokument definiert die konkreten Schritte, um das OpenClaw-System robuster, selbstheilender und wartbarer zu machen.

## Pillar 1: Proaktives Self-Healing (Zuverlässigkeit)

**Ziel:** Fehler erkennen und automatisch beheben, bevor sie zu einem Ausfall führen.

- **[ERLEDIGT] Task 1.1: Analyse des Gateway-Status-Checks:**
  - **Problem:** Der `openclaw gateway status` Befehl im Self-Healing-Monitor schlug sporadisch fehl.
  - **Aktion:** Timeout von 15s auf 30s erhöht, um das Problem bei hoher Systemlast zu mitigieren.

- **[ERLEDIGT] Task 1.2: Überwachung von System-Ressourcen:**
  - **Aktion:** Überwachung für Festplatten- und RAM-Auslastung zum Self-Healing-Plugin hinzugefügt. Bei Überschreitung der Schwellenwerte (85%/90%) wird ein GitHub-Issue erstellt.

## Pillar 2: Qualitätssicherung (Automatisierte Tests)

**Ziel:** Sicherstellen, dass Änderungen an Plugins nicht das System destabilisieren.

- **[IN ARBEIT] Task 2.1: Teststrategie definieren:**
  - **Aktion:** Festlegen, was und wie getestet wird. Sinnvoll sind:
    - *Unit-Tests* für kritische Einzelfunktionen (z.B. Cooldown-Berechnung).
    - *Integration-Tests*, die das Zusammenspiel eines Plugins mit dem Gateway simulieren.

- **[IN ARBEIT] Task 2.2: Test-Framework auswählen:**
  - **Aktion:** Vitest als leichtgewichtige, TypeScript-freundliche Option ausgewählt (falls du nichts anderes bevorzugst).

- **[IN ARBEIT] Task 2.3: Proof of Concept (PoC) implementieren:**
  - **Aktion:** Ein einfacher Smoke Test wurde unter `tests/smoke/openclaw-self-healing-smoke.test.ts` angelegt. Er versucht, das Plugin-Modul zu importieren und schlägt fehl, wenn der Import nicht möglich ist.

- **[TODO] Task 2.4: CI/CD-Pipeline einrichten:**
  - **Aktion:** Eine GitHub Action erstellen, die die Tests bei jedem `git push` automatisch ausführt und einen Pull-Request blockiert, wenn Tests fehlschlagen.

## Pillar 3: Strategische Weiterentwicklung

**Ziel:** Eine fundierte Entscheidung über die zukünftige Ausrichtung treffen.

- **[TODO] Task 3.1: Management-Summary erstellen:**
  - **Problem:** Die Ergebnisse aus dem "openclaw-alternative-research" sind vorhanden, aber noch nicht für eine schnelle Entscheidung aufbereitet.
  - **Aktion:** Ich erstelle eine 1-seitige Zusammenfassung der Recherche mit den wichtigsten Konkurrenten, deren Lücken und einer klaren Empfehlung für die nächsten Schritte.

- **[BLOCKIERT] Task 3.2: Entscheidung treffen:**
  - **Aktion:** Basierend auf der Zusammenfassung musst du die finale Entscheidung treffen, ob wir a) etwas Eigenes bauen, b) OpenClaw gezielt erweitern oder c) das Thema vorerst nicht weiterverfolgen.

# UX-Review: Analyse der Benutzerschnittstelle

In diesem Dokument werden absichtlich eingebaute Usability-Fehler in einer Benutzerschnittstelle identifiziert und Optimierungsvorschläge festgehalten.

---

## 1. Passwortfeld: Vorbelegter Text muss gelöscht werden

**Beobachteter Fehler**  
Im Passwortfeld steht bereits Text wie „Choose password“ als echter Inhalt. Dieser Text muss zuerst markiert und gelöscht werden, bevor das Passwort eingetippt werden kann.

**Optimierungsvorschlag**  
- Echten Platzhalter (placeholder) verwenden, z. B. `placeholder="Passwort wählen"`  
- Deutliches Label oberhalb des Feldes anzeigen, z. B. „Passwort“  
- Eingabefeld beim Fokus leer lassen, damit der Nutzer direkt tippen kann

---

## 2. Close-Button mit falschem Symbol (Copyright statt X)

**Beobachteter Fehler**  
Der Schließen-Button ist mit einem Copyright-Symbol (©) statt einem X oder „Close/Schließen“ versehen, was die Funktion nicht klar erkennbar macht.

**Optimierungsvorschlag**  
- Standardisiertes Schließen-Symbol verwenden (X oben rechts)  
- Alternativ: Textbutton mit „Close“ oder „Schließen“  
- Konsistenz zu gängigen UI-Patterns herstellen

---

## 3. E-Mail-Eingabe in mehrere Teile aufgesplittet

**Beobachteter Fehler**  
Die E-Mail-Adresse muss in einzelne Teile eingeben werden (z. B. Name getrennt von Domain, Endung wie `.com` separat auswählbar). Das macht die Eingabe unnötig kompliziert.

**Optimierungsvorschlag**  
- Ein einziges E-Mail-Feld anbieten, in das die komplette Adresse eingetragen wird  
- E-Mail-Format mit Validierung prüfen und bei Fehlern verständliche Fehlermeldung anzeigen  
- Optional: Autovervollständigung, z. B. Vorschläge wie `@gmail.com`, `@outlook.com`

---

## 4. Passwortanforderungen sind versteckt platziert

**Beobachteter Fehler**  
Die Passwortanforderungen (z. B. Mindestlänge, Sonderzeichen, Zahlen) werden ganz unten oder an einer wenig sichtbaren Stelle angezeigt.

**Optimierungsvorschlag**  
- Passwortregeln direkt unter oder neben dem Passwortfeld platzieren  
- Regeln in einer kurzen, gut lesbaren Liste darstellen  
- Optional: Dynamische Anzeige, bei der jede erfüllte Regel visuell markiert wird (z. B. Häkchen)

---

## 5. Download-Button für Profilbild ist prominenter als Upload

**Beobachteter Fehler**  
Der Download-Button für das Profilbild ist größer und auffälliger als der Upload-Button, obwohl der wichtigste Schritt an dieser Stelle das Hochladen ist.

**Optimierungsvorschlag**  
- Upload-Button visuell priorisieren (Größe, Kontrast, Position)  
- Beschriftung klar und eindeutig, z. B. „Profilbild hochladen“  
- Download-Button nur sekundär oder erst nach erfolgreichem Upload anzeigen

---

## 6. Länderwahl ausschließlich über Flaggen

**Beobachteter Fehler**  
Das Land wird nur über Flaggen ausgewählt. Viele Flaggen sind ähnlich und nicht jeder Nutzer kennt jedes Symbol sicher.

**Optimierungsvorschlag**  
- Dropdown mit Ländernamen verwenden, z. B. „Schweiz“, „Deutschland“, „Österreich“  
- Optional die Flagge zusätzlich neben dem Ländernamen anzeigen  
- Suchfunktion im Dropdown ermöglichen, um schneller ein Land zu finden  
- Barrierefreiheit beachten (Screenreader-Text, keine reine Symbolkommunikation)

---

## 7. „Send message“-Box überdeckt den Next-Button

**Beobachteter Fehler**  
Das Textfeld für „Send message“ liegt so im Layout, dass es den Next-/Weiter-Button teilweise oder vollständig überlagert. Der Nutzer kann den Button schwer finden oder gar nicht klicken.

**Optimierungsvorschlag**  
- Layout so anpassen, dass Elemente sich nicht überlappen (z. B. über Flexbox/Grid)  
- Genügend Abstand zwischen Textbox und Button einplanen  
- Responsives Design testen (verschiedene Bildschirmgrößen, Zoomstufen)  
- Fokus-Reihenfolge prüfen, damit der Weiter-Button auch per Tastatur erreichbar ist

---

## 8. Captcha: Nicht alle relevanten Bilder auswählbar

**Beobachteter Fehler**  
Beim Captcha können nicht alle passenden Bilder ausgewählt werden (z. B. nur begrenzte Auswahl oder falsche Erkennung), obwohl die Aufgabe dies verlangt. Dadurch kann der Nutzer die Aufgabe nicht korrekt lösen und den Prozess nicht abschließen.

**Optimierungsvorschlag**  
- Captcha so umsetzen, dass alle relevanten Bilder auswählbar sind und korrekt erkannt werden  
- Klare Rückmeldung geben, warum ein Captcha als falsch gewertet wurde  
- Alternativ einfachere und zugänglichere Captcha-Varianten einsetzen (z. B. „Ich bin kein Roboter“-Checkbox, einfache Textaufgabe)

---

## 9. Gender-Auswahl: Falsches Element hervorgehoben

**Beobachteter Fehler**  
Bei der Auswahl des Geschlechts (Gender-Button) ist nicht die gewählte Option hervorgehoben, sondern die nicht ausgewählte. Dadurch entsteht ein falscher visueller Zustand und Verwirrung, welches Gender wirklich aktiv ist.

**Optimierungsvorschlag**  
- Immer die aktuell ausgewählte Option deutlich hervorheben (Farbe, Rahmen, Hintergrund)  
- Nicht ausgewählte Optionen neutral gestalten  
- Klarer Zustand für „aktiv“ vs. „inaktiv“, z. B. durch Kontrast, Icon oder Checkmark  
- Optional: Auswahl zusätzlich per Text bestätigen (z. B. „Ausgewählt: männlich“)

---

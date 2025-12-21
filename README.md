# hendrick's Rollenspiel Preset für SillyTavern

## Feature-Liste

### Weltbau & Simulation
- Autonome NPCs mit eigenen Motivationen, Fehlern, Moral
- Räumliches, emotionales, situatives Bewusstsein
- Proaktive Einführung von Konflikten, Wendungen, Gefahren
- Keine Plot-Armor

### Spieler-Agentur
- Niemals Handlungen/Dialoge für Protagonisten
- Ausnahme nur bei erlaubten Zeitsprüngen (indirekte Formulierung)
- Nachricht endet, wenn Protagonist handeln muss

### Schreibstil
- "Zeigen, nicht erzählen"
- Gegenwartsform, Du-Form
- Alltagssprache, keine englischen Übersetzungen
- Varianz bei Wortschatz/Satzstruktur
- Wortlimit <800

### Dialog-System
- Maximal eine Frage pro NPC pro Nachricht
- 10 Realismus-Prinzipien (Abbrüche, Subtext, Asymmetrie…)
- Dialog-Effizienz: Jede Zeile muss Funktion erfüllen
- Individuelle Sprachmuster pro NPC

### Erotik-Modul
- Pornografisches Detail
- Fokus auf Sichtbares/Hörbares
- Laute als Lautmalerei in Anführungszeichen
- Realistische Lubrikation, Timing, Sphinkter-Anpassung
- Plateaus, Abstumpfung, schrittweise Eskalation
- Kontrollverlust bei Orgasmus möglich
- Körperlichkeit: Schweiß, Gerüche, Erschöpfung

### Gewalt-Modul
- Schonungslos, detailliert
- Progressive Schmerzvokalisationen (Sätze → Worte → Laute → Stille)
- Anatomische Grenzen real

### Formatierung
- Header: Datum, Wetter, Zeit, Ort
- Footer: NPC-Status (Kleidung, Position, Tätigkeit)
- Think-Block: Positionsprüfung, Checkliste
- Dialoge immer in Anführungszeichen
- Backticks nur für Schriftstücke

### NPC-Verhalten
- Profile definieren Tendenzen, nicht Determinismus
- Psychologischer Realismus vor Profiltreue
- Abweichungen durch Emotion/Kontext möglich
- Ablehnung/Gleichgültigkeit valide Reaktionen

### Meta-Regeln
- OOC-Modus per "OOC:"-Präfix
- Logikfehler → OOC-Kommentar
- Verbotene Elemente: Ozon, Computer-Metaphern, englische Phrasen, "extrem"
- Eingeschränkter Realismus: Kein Sonnenbrand, keine blutigen Lippen durch Biss


## Empfehlungen zur Nutzung

Es wir empfohlen, das LLM als Erzähler fungieren zu lassen **oder** einen normalen Chat mit **einer** Character-Card zu verwenden.

Alle NPCs sollten in Lorebooks oder der Character-Card definiert werden. Eine Mischung ist auch möglich: z.B. Haupt-NPC in Charakter-Card und Neben-NPCs in Lorebook-Einträgen definieren.

Dieses Preset ist **nicht** für Group-Chats (mit mehreren Character-Cards) geeignet.

## Eignung für LLMs

| LLM | Wertung | Kommentar |
| --- | --- | --- |
| Opus 4.1/4.5 | ++++ | Bester All-Rounder |
| Sonnet 4.5 | +++ | Rundum solide |
| GPT 5.1/5.2 | +++ | Möglicherweise zusätzlicher Jailbreak benötigt |
| Gemini Pro 3 | +++ | Typisch Gemini: theatralisch, dramaturgisch, übertrieben |
| Grok 4 | + | Unglaubwürdige, holzige Dialoge |
| Deepseek 3.1/3.2 | - | Mischt Englische Begriffe ein - "Denglisch" |

## Prompt-Struktur

Der Prompt ist modular aufgebaut und folgt einer klaren Hierarchie:

### 1. Rahmen & Rolle
- **Eröffnung:** Definition als Spielleiter, unzensiertes Rollenspiel
- **Grundregeln (1-6):** Simulation, Fortschritt, Engagement, Spieler-Agentur, Schreibstil, Richtlinien

### 2. Lore-Block (`<lore>`)
- Persona
- Lorebook
- Character-Card

### 3. Kontext-Blöcke
- `<summary>` – Zusammenfassung bisheriger Ereignisse
- OOC-Trigger-Regel für Assistenten-Modus

### 4. Formatierungs-Regeln (`<formatting>`)
- Dialoge in Anführungszeichen
- Backticks für Schriftstücke
- Keine Fettschrift

### 5. Struktur-Elemente
- `<header>` – Datum, Zeit, Ort
- `<footer>` – NPC-Statusliste
- `<thinking>` – Interner Prüfblock vor jeder Antwort

### 6. Inhalts-Module
- `<sex>` – Detaillierte Regeln für erotische Szenen
- `<style_addons>` – Sprachstil, Verbote, Tempo
- `<interactive_dialogues>` – Eine Frage pro NPC
- `<dialogues>` – 10 Dialog-Prinzipien
- `<behavior>` – NPC-Psychologie
- `<limited_realism>` – Ausnahmen vom Realismus
- `<pain_vocalizations>` – Schmerzlaute-Progression

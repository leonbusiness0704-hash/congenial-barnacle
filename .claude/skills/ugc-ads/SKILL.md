---
name: ugc-ads
description: Einstiegspunkt für UGC-Skripte. Nutzen, wenn der User sagt "write me a UGC script for …", "schreib mir ein UGC-Skript für …", "UGC-Ads für mein Produkt" o. ä. Wählt den passenden Modus (swipe, template oder write), stellt EINE gebündelte Rückfrage, führt den Modus aus und speichert die Skripte in ugc/<brand>/.
---

# UGC Ads (Router)

## 1. Modus wählen

| Situation | Modus | Skill |
|---|---|---|
| User liefert eine bestehende Ad, ein Transkript oder einen Link zu einem Gewinner-Video | **swipe** | `ugc-swipe` |
| User will bewährte Formate, schnell viele Varianten, oder nennt ein Format ("Storytime", "3 Gründe") | **template** | `ugc-template` |
| Nur Produkt, nichts weiter, oder User will etwas komplett Neues | **write** | `ugc-write` |

Ist es unklar, nimm **template** und nenne den Modus in einer Zeile.

## 2. Einmal fragen

Stelle genau EINE Nachricht mit allen fehlenden Punkten (als nummerierte Liste,
mit deinem Vorschlag als Default, damit der User nur "ok" sagen muss):

1. Brand-Name und Produkt (+ Link, falls vorhanden)
2. Zielgruppe und Hauptproblem
3. Plattform und Länge (Default: TikTok/Reels, 30–45 s)
4. Angebot (Rabatt, Garantie, Bundle)
5. Sprache und Ton (Default: Sprache des Users, Du-Form, locker)
6. Anzahl Skripte (Default: 3)
7. Nur bei swipe: die Vorlage-Ad (Text, Transkript)

Danach keine weiteren Rückfragen. Fehlendes selbst sinnvoll annehmen.

## 3. Ausführen

Lies die SKILL.md des gewählten Modus und folge ihr. Schreibregeln, Format und
Compliance stehen in `ugc-write/SKILL.md` (Abschnitte 3–6) und gelten für alle Modi.

## 4. Speichern

- Ordner: `ugc/<brand>/` (brand als kleingeschriebener Slug, z. B. `ugc/noriva/`).
- `ugc/<brand>/brief.md` anlegen bzw. aktualisieren: Produkt, Zielgruppe, Angebot, Ton.
  Existiert die Datei schon, lies sie zuerst und frag nicht erneut nach diesen Punkten.
- Skripte: `ugc/<brand>/<YYYY-MM-DD>-<modus>-<kurzer-slug>.md`, eine Datei pro Lauf
  mit allen Varianten, Hooks und Empfehlung.
- Bestehende Dateien nie überschreiben; bei gleichem Namen `-2`, `-3` anhängen.

## 5. Antwort an den User

Kurz: welcher Modus, wie viele Skripte, Dateipfad, und welche Variante du zuerst testen würdest.
Den Hook der Top-Variante direkt im Chat zeigen.

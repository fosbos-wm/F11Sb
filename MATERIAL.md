# Material für die 11Sb einstellen (Gerüst)

Die 11Sb arbeitet jetzt wie die 12Sb: Check-in, Infotext, Üben und Vertiefen, Check-out. Alles Material liegt in der App und wird den Themen zugeordnet. Lehrkräfte können jedes Material über das × wieder entfernen und über „Entfernte Materialien zurückholen“ zurückholen.

## Mitgelieferte Dateien: `material.json`

Eintrag je Datei, Dateien liegen im Repo (z. B. in `infotexte/` und `aufgaben/`):

    {"material":[
      {"id":"info01","wocheId":"pp01","kategorie":"lehrtext","titel":"Gegenstand der Psychologie","url":"infotexte/LB1-01_Gegenstand-der-Psychologie.pdf","ord":10},
      {"id":"ueb01b","wocheId":"pp01","kategorie":"uebung","titel":"AFB I: Alltagsaussagen prüfen","url":"aufgaben/LB1-01_Basis_Alltagsaussagen.pdf","ord":20}
    ]}

- `wocheId` = Kennung des Themas (Liste unten)
- `kategorie`: `lehrtext` (Infotext), `uebung` (AFB I), `vertiefung2` (AFB II), `vertiefung3` (AFB III), `praxis` (Praxisauftrag in AFB III, mit `hinweis`)
- `"bib":true` = nur in der Unterrichtsbibliothek: Schüler:innen sehen den Eintrag erst, wenn die Lehrkraft ihn im Thema ankreuzt
- Dateinamen bitte ohne Umlaute und Leerzeichen
- Interaktive Übungen: `"url":"uebungsbausteine/station.html?s=<Stations-ID>"`

## Selbstlernkurse

`einarbeitung/inhalte/<Thema-Kennung>.json` (AFB I), `<Kennung>-plus.json` (AFB II), `<Kennung>-vertieft.json` (AFB III). Mit `"themen":["<Kennung>"]` im Kurs zuordnen.

## Interaktive Übungen (Stationen)

`uebungsbausteine/stationen/katalog.json`. Mit `"themen":["<Kennung>"]` und `"schwierigkeit":"leicht"|"mittel"|"vertieft"` zuordnen, dann erscheinen sie nur beim passenden Thema und Niveau.

## Kennungen der Themen (11. Klasse)

LB 1: pp01 Gegenstand der Psychologie · pp02 Wissenschaftliche und alltagspsychologische Aussagen · pp03 Das Experiment als wissenschaftliche Methode · pp1a1 Gegenstand der Pädagogik · pp1a2 Ziele und Handlungen der Erziehung · pp1a3 Beziehung zwischen Erziehenden und Zu-Erziehenden · pp1a4 Einrichtungen der Erziehung
LB 2: pp09 Wahrnehmung · pp2p2 Gedächtnis · pp2a1 Speichersysteme des Langzeitgedächtnisses · pp12 Strategien zum Wissenserwerb · pp10 Emotion · pp11 Motivation und Attributionstheorie
LB 3: pp04 Merkmale von Erziehung · pp05 Erziehungsstile nach Baumrind · pp06 Mündigkeit nach Roth · pp07 Bildungs- und Erziehungsbereiche des BayBEP
LB 4: pp4p1 Merkmale des Begriffs Lernen · pp13 Klassisches Konditionieren · pp14 Operantes Konditionieren · pp15 Sozial-kognitive Theorie nach Bandura · pp16 Medien als Einflussfaktor für Lernprozesse

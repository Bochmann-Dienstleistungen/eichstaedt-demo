# Go-Live-Checkliste — Physiotherapie Eichstädt

Stand 21.08.2026. Die Seite ist gebaut, bebildert und rechtlich vorbereitet.
Sie ist **noch nicht deployed** — bewusst, bis die vier Punkte unten geklärt sind.

## Blocker für Live (ohne die geht die Seite nicht öffentlich)

| # | Was fehlt | Von wem | Warum blockierend |
|---|---|---|---|
| 1 | **E-Mail-Adresse der Praxis** | Praxis | §5 TMG verlangt sie im Impressum. Ohne sie ist das Impressum unvollständig = abmahnfähig. Dieselbe Adresse braucht auch das Kontaktformular (Punkt 2). |
| 2 | **Formspree auf Praxis-Postfach** | Frederic, sobald 1 da ist | Läuft aktuell auf das VALORIS-Sammelpostfach `mlgpooqw`. Patientenanfragen dürfen nicht in Frederics Postfach landen — DSGVO. Neues Formular anlegen + AVV. |
| 3 | **Foto-Einwilligung der Patientin** | Praxis | Auf zwei Praxisfotos ist eine Patientin. Spiegelbilder mit ihrem Gesicht wurden weggeschnitten, sie ist nur von hinten und nicht erkennbar — für Live trotzdem ihr OK einholen oder die Fotos tauschen. |
| 4 | **Öffnungszeiten bestätigen** | Praxis | Aktuell Platzhalter (Mo–Do 08–18, Fr 08–14). Falsche Zeiten auf einer Praxisseite kosten echte Termine. |

## Erledigt (21.08.2026)

- [x] Echte Fotos eingebaut, self-gehostet in `assets/` (kein Hotlink, DSGVO)
- [x] Impressum: Berufsbezeichnungen beider Therapeuten, Aufsichtsbehörde (Kreis Schleswig-Flensburg – Gesundheitsamt), berufsrechtliche Regelungen (MPhG, HeilprG)
- [x] HWG-Trennung: Leistungen = nur offiziell Bewerbbares, Graubereich nur als Aus-/Fortbildung in der Vita
- [x] QA sauber: keine Konsolenfehler, keine 404, nichts unsichtbar
- [x] Google Maps als Zwei-Klick-Lösung, Cookie-Hinweis, dynamisches Footer-Jahr

## Schön, aber kein Blocker

- [ ] Porträt von Monika (Gesicht) — aktuell nur das Roller-Motiv mit Helm
- [ ] Hero-Spruch (ihr Wunschspruch) statt „Bewegung, die gut tut."
- [ ] Vita-PDF → finale Formulierung der Aus- & Fortbildungen
- [ ] Instagram-Link (Profil bisher nicht auffindbar)
- [ ] Gunnars Vorstellungstext (steht aktuell allgemein — funktioniert auch so)

## Beim Deploy nicht vergessen

- Domain `physiotherapie-eichstaedt.de` bei Strato registrieren. **Inhaber/Admin-C = Gunnar Eichstädt**, Tech-C = Frederic. DENIC-Bestätigungsmail muss binnen 14 Tagen geklickt werden → braucht ebenfalls die Praxis-E-Mail.
- **`og:image` auf die echte Domain umstellen** — steht aktuell auf der github.io-Adresse (Kommentar im `<head>` markiert die Stelle).
- Bei einer reinen Vorschau vor Abnahme: `<meta name="robots">` auf `noindex, nofollow` setzen und `robots.txt` mit `Disallow: /` beilegen. Zum echten Live-Gang wieder auf `index, follow`.
- Restzahlung 495 € (Rest zu VTR-2026-003) erst nach Abnahme.

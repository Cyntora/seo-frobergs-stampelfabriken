# Prompt-regler för Cyntora-kundpresentationer

Sammanställning av reglerna som styr produktionen av single-file HTML-presentationer för kund. Använd vid varje ny presentation. Uppdatera om något ska ändras permanent.

## Innehållskrav

- Domänauktoritet ska visas tydligt med konkreta siffror, inte i abstrakta påståenden.
- Frasen "kopierat innehåll" eller liknande som låter anklagande tonas ned. Reframe till "vi behöver differentiera innehållet ytterligare, främst på den svagare sidan".
- Ingen direkt veckoplan i kund-deck. Visa tester först, sedan en prioriteringslista.

## Design

- Single-file HTML med inbäddad CSS, ingen build-process, inga externa beroenden utöver Google Fonts.
- Matcha kundens visuella känsla. Kolla deras hemsida för palett och stil.
- Cyntoras logotyp läggs in både i nav och hero, hämtas som SVG från cyntora.se.
- Typografi: Cormorant Garamond för rubriker, Inter för brödtext, eller annan likvärdig premium-kombination beroende på kund.
- Scroll-deck där varje sektion fyller sin egen vy (`min-height: 100vh`).

## Tonregler

- Skriv som en mejl- eller Slack-konversation. Direkt, korta meningar, "ni"-form mot kunden.
- Cyntoras egen offerttext är referens för tonen.

### Förbjudna grepp

- Inga tankstreck (—). Använd komma, punkt, eller "och" istället.
- Inga AI-marknadsförarklichéer, inklusive men inte begränsat till: "lågt hängande frukter", "B2B-guld", "edge inte svaghet", "snabba vinster och långsiktig pipeline", "italiensk kvalitet möter svensk ambition", "vi bryr oss med hjärna med hjärta".
- Inga fauxpoetiska rubriker med italics-emfas. Rubriker beskriver vad sektionen handlar om.
- Inga triadiska konstruktioner för effekt.

## Publicering

- Publikt GitHub-repo under organisationen Cyntora, skapas via `gh` CLI.
- GitHub Pages aktiveras på `main`-branchen, root.
- `<meta name="robots" content="noindex, nofollow">` i `<head>` så Google inte indexerar kundens prisuppgifter eller analyser.
- Repo-namn: `seo-<klientslug>` eller motsvarande beskrivande namn.

## Leveranser per presentation

- HTML-fil lokalt (`index.html` plus tillhörande SVG-logotyp).
- 16:9 PDF som backup (1600×900 eller motsvarande aspect ratio).
- Live URL på `<klient>.github.io`.
- Förslag på kort mejl till kunden med länken.
- Repository i Cyntoras org.
- Denna MD-fil med reglerna kopieras in i varje presentations-repo som referens.

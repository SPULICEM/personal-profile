# Sérgio Pulice – scientific profile website: working notes

Compact record of the build, so a new chat only needs `index.html` plus this file.

## Files
- `index.html` – the whole site (one self-contained file: HTML, CSS, JavaScript, portrait embedded as base64). Open it in any browser or upload it as-is to any web host. Only external dependency: Google Fonts (Bricolage Grotesque, Newsreader), with system-font fallbacks.
- Published copy: https://claude.ai/artifact/CzQhJM9pXgsboQMMfEF3ap

## Design and behaviour
- Dark theme only; British English throughout (article titles keep the journals' own spelling).
- Section order: top (portrait, name, headline, text, links, network graph) → Background → Research themes → Projects → Publications → Beyond academia → Get in touch.
- Text under the photo and the Research-theme cards alternate between two versions automatically every 15 s (pauses on hover/tap; both versions shown without animation if the visitor prefers reduced motion).
- Network graph: Fruchterman–Reingold layout computed in the browser (250 seeded runs, fewest crossings and label overlaps wins). 9 nodes; every node links to its research-theme card (method nodes link to the Research themes section). Gentle drifting motion.
- Publications list (the 2022 chapter links to the open-access USP book page): newest first, with type labels (Book, Book chapter, PhD thesis, Master's dissertation), DOI links, citation counts, and filters (All, Transition and cities, Water and food, Hydropower and development, Disaster risk reduction, Books and chapters, Theses).

## Content decisions (latest state)
- Hero: "Postdoctoral researcher / Cemaden / MCTI, funded by FAPESP / São José dos Campos, Brazil". Name and headline sit beside the portrait.
- Research themes: Transition to sustainability; Climate policy and governance; Water, food and energy; Disaster risk reduction; Resilient cities; Hydropower and local development. Graph nodes use the same names; methods nodes: Network science, Indicators, Socioenvironmental analysis.
- Projects (order): CCD Carbon Neutral Cities, COPE, BridgingVALUES, Cerrado/Caatinga nexus, Paraíba do Sul, COMPON, ANPPEA (2015–2019). No "Coordinator" tags. Links: FAPESP grants 24/01115-0 (CCD), 25/13377-2 and 26/12936-0 (CCD), 22/02891-9 (COPE), BridgingVALUES INPE site, compon.org.
- Background: Visiting researcher at Edinburgh Napier (with project title and FAPESP grant 26/12936-0), Visiting researcher at IPT, Postdoctoral researcher at Cemaden (with title and FAPESP grant 25/13377-2), PhD, MSc, BSc. Research groups: UNSEEL, LADIS (linked), PLANGEA. No Languages, Selected training or Mentoring sections.
- Beyond academia: Policy and practice; Public knowledge. ANPPEA line: "contributed to the ANPPEA national network (2015–2019)".
- Sources: Lattes CV (3 Nov 2026), FAPESP BV pages supplied by the author, publisher/indexing pages for DOIs. ResearchGate could not be read (blocks automated access).

## Open items
- *Visioni LatinoAmericane* 2026 article: DOI not confirmed (links to the OpenstartS record instead).
- Napier internship starts 1 Oct 2026 per FAPESP, while the Background entry says "2026 – present".
- FAPESP lists fellowship 25/13377-2 as "Interrompido" (not shown on the page).
- The Research-themes intro line ("…bridging environmental and policy process and policy analysis sciences") is the author's wording; a smoother alternative was offered.
- BridgingVALUES INPE link could not be opened during the build; please click-test it.
- No email address on the page yet.

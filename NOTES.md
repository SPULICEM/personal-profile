# Sérgio Pulice – scientific profile website: working notes

Compact record of the build, so a new chat only needs `index.html` plus this file.

## Files
- `index.html` – the whole site (one self-contained file: HTML, CSS, JavaScript, portrait embedded as base64). Open it in any browser or upload it as-is to any web host. Only external dependency: Google Fonts (Noto Sans), with system-font fallbacks.
- Published copy: https://claude.ai/artifact/CzQhJM9pXgsboQMMfEF3ap

## Design and behaviour
- Visual design: Terrestres design system (https://claude.ai/code/artifact/001654af-c221-43c8-bd6a-3132352f0137). Flat colours only: azul #4A96D2, laranja #EC6730, preto #000000, cinza #E0DFDA, branco; square corners; no tints or gradients. The hero graph box is black (preto) with white labels, blue links, orange theme nodes and blue method nodes. The 'Read the publications' button sits under the graph in the right panel, with an orange border and black text, pushed to the bottom of the panel so it aligns with the Lattes CV / ORCID / ResearchGate row on the left. Everything stays on the five brand colours. Noto Sans for text and Bogue for titles (Bogue has no font file in the system, so titles fall back to Noto Sans Bold). Text is always preto on branco/cinza/azul/laranja and branco/cinza on preto. The system's asterisk marks every section title, and the 'conectivo' line pattern fills the orange hero panel (the preto network box sits over it, so no text lies on the lines). Previous dark design saved as a backup in the build session only.
- British English throughout (article titles keep the journals' own spelling). Page copy stays in English even though the Terrestres README suggests Portuguese for its own materials.
- Section order: top (portrait, name, headline, text, links, network graph) → Main areas of interest (the six theme cards) → Background → Active projects → Publications → Beyond academia → Get in touch.
- Text under the photo and the Main-areas cards alternate between two versions continuously every 25 s with a 1.6 s cross-fade; the loop never pauses (not on hover, focus or touch). With reduced motion on, both versions are shown without animation.
- Network graph (the drawing is fitted to its box at load, so on desktop the black box runs from the top of the panel down to the 'Read the publications' button): Fruchterman–Reingold layout computed in the browser (250 seeded runs, fewest crossings and label overlaps wins). 9 nodes; every node links to its research-theme card (method nodes link to the Research themes section). Gentle drifting motion.
- Publications list (no filters; the 2022 chapter links to the open-access USP book page): newest first, with type labels (Book, Book chapter, PhD thesis, Master's dissertation), DOI links, citation counts.

## Content decisions (latest state)
- Hero: the photo's height matches only the name + headline block (Postdoctoral researcher / Cemaden / MCTI, funded by FAPESP / São José dos Campos, Brazil); the intro paragraph runs full width underneath.
- Main areas of interest (cards): Transition to sustainability; Climate policy and governance; Water, food and energy; Disaster risk reduction; Resilient cities; Hydropower and local development. Graph nodes use the same names; methods nodes: Network science, Indicators, Socio-environmental analysis.
- Active projects only (order): CCD Carbon Neutral Cities, COPE, BridgingVALUES. Earlier projects (Cerrado/Caatinga nexus, Paraíba do Sul, COMPON, ANPPEA) were removed from the page. No "Coordinator" tags. Links: FAPESP grants 24/01115-0 (CCD), 25/13377-2 and 26/12936-0 (CCD), 22/02891-9 (COPE), BridgingVALUES INPE site.
- Background: highlighted cards for current positions (Visiting researcher at Edinburgh Napier with project title and FAPESP grant 26/12936-0; Visiting researcher at IPT; Postdoctoral researcher at Cemaden with title and FAPESP grant 25/13377-2), then one Education paragraph (PhD, MSc, BSc), then Research groups (UNSEEL, LADIS linked, PLANGEA).
- Beyond academia: Policy and practice; Public knowledge. ANPPEA line: "contributed to the ANPPEA national network (2015–2019)".
- Sources: Lattes CV (3 Nov 2026), FAPESP BV pages supplied by the author, publisher/indexing pages for DOIs. ResearchGate could not be read (blocks automated access).

## Open items
- *Visioni LatinoAmericane* 2026 article: DOI not confirmed (links to the OpenstartS record instead).
- Napier internship starts 1 Oct 2026 per FAPESP, while the Background entry says "2026 – present".
- FAPESP lists fellowship 25/13377-2 as "Interrompido" (not shown on the page).
- The Research-themes intro line ("…bridging environmental and policy process and policy analysis sciences") is the author's wording; a smoother alternative was offered.
- BridgingVALUES INPE link could not be opened during the build; please click-test it.
- No email address on the page yet.

## Fonts
- Bogue (titles: name, section headings, card titles, years, position titles) and Noto Sans (all text; Light, Regular, SemiBold, Bold, ExtraBold, Black, with italics) are embedded in index.html as Latin-subset WOFF2 (about 0.5 MB), so the page needs no external font service. The font files supplied by the author were used; embedding on a website needs a web-font licence for Bogue.
- Safety net: if the embedded fonts cannot load, text falls back to Noto Sans from Google Fonts, then to the system sans-serif.
- The `fonts/` folder in this zip holds the same subset WOFF2 files for reuse; index.html does not need them.

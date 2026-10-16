# SHADEPROOF · NAT

**National U.S. court form-rule reference and draft helper** (browser-only).

Companion to the district-specific **Shadeproof WDWA** build. NAT covers federal districts, bankruptcy courts, circuits, and state baselines with local depth where rules were sourced into the coverage pack.

## What it does

- Pick a **venue** (state / federal district / bankruptcy / circuit).
- See **rules on file** for margins, fonts, spacing, paper, e-file size caps, redaction notes, and related form constraints.
- If a court has no rule for a key, the UI says **NO RULE ON FILE** — it does not invent one.
- **Export DOCX draft** with paper size, margins, font size, and line spacing taken from the resolved rules, plus caption fields and body text you provide.
- **Optional PDF view / stamp** when online (loads pdf.js and pdf-lib from CDNs). Core checking and DOCX work without that.

## What it is not

- **Not legal advice.**
- **Not a substitute for the court’s own rules, clerk instructions, or local forms.**
- Rules are **machine-sourced** from public materials and are **not human-confirmed** for every jurisdiction.
- **Not a filing portal** — you still e-file through the court.

## Privacy

See [privacy.html](./privacy.html). Short version: static site, no Shadeproof server, drafts stay in your browser; optional CDN only for PDF features.

## Use

1. Open the site (GitHub Pages or local static server).
2. Choose venue.
3. Read the rules panel; verify anything critical with the court.
4. Fill case / title / attorney and draft body → **Export DOCX draft**.
5. When finalizing a PDF, use stamp only if the PDF libraries loaded and you still verify the result.

## Local / dashboard embedding

The app listens for a host `postMessage` handoff (`cmd: 'handoff'`) and supports `SHADEPROOF_HINT` / `SHADEPROOF_STORAGE_ADAPTER` when embedded. Framed embeds skip CDN loads unless explicitly allowed. See `BRIDGE.md` in the development coverage tree if you maintain the full project.

## Accuracy

Coverage is broad but uneven: high-volume courts are deeper; many courts correctly show thin or empty local form sets. Treat every number as a starting point to confirm.

## License

**Apache License 2.0** — see [LICENSE](./LICENSE) and [NOTICE](./NOTICE).

- Compliance logic, coverage structures, and source form may be used, modified, and redistributed under Apache-2.0 with attribution.
- **Evanscira Labs** name, SHADEPROOF / SRC-D branding, and the product look are not licensed as trademarks; do not imply endorsement.
- Court rules remain the courts’; this tool is not legal advice.

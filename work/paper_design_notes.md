# Paper design notes (ML-11)

How the deployed paper (`docs/index.html`) was shaped, and why.

## What I looked at
- **Distill-style web research articles** (Hohman et al., *Communicating with Interactive Articles*, Distill 2020): readers skim, so the page has to work for someone who reads only headings, figures and captions.
- **Figure and table guidance** (Editage, *Tips on effective use of tables and figures*): each figure stands on its own, with a specific title and a caption that states the takeaway; label axes and units.
- **Model Cards for Model Reporting** (Mitchell et al., 2019): state intended use, out-of-scope uses, and the evaluation procedure next to the results.

## What I chose, and why
| Choice | Reason |
|---|---|
| Single static HTML page, no framework, served from `/docs` on GitHub Pages | Free and fast; nothing to break; anyone can open the source. |
| Five-sentence abstract + a "Key findings" box at the top | Most readers stop there; they should still leave with the result *and* its limits. |
| Contents line linking to each section | Long page; lets a reviewer jump to Methods or Limits. |
| Numbered figures with "Figure N — takeaway" captions | Captions carry the message for skimmers. |
| Intended-use / not-intended-for block (model-card style) | Decision-support work must say what it must not be used for. |
| Negative warehouse result reported in Results | Honest reporting; it is the clearest base-rate lesson in the work. |
| Serif body, sans headings, ~70-character lines, dark-mode support, no horizontal scroll at 390px | Readable on phones; checked at 390px and 1200px. |
| No interactive charts | Three static charts answer the questions; interactivity would add load without new information. |

## Public-safety pass (20 Oct 2026)
- No client names, domains, URLs, page titles, queries, or pseudonymous row IDs on the page.
- Only outbound links: the repo and https://flyrank.ai.
- No tokens anywhere in the repo; no datasets committed.
- Claim language checked for "proves / causes / will increase / predicts Google": none.

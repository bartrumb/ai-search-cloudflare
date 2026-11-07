# Build Smarter Search with AI on Cloudflare's Edge

Slides from my OPO Startups Tech Talk at Confluence Tech Hub in St. Charles, Missouri, on July 1, 2026: AI-powered hybrid search and agentic assistants built entirely on Cloudflare, with a live demo of [Shepherd](https://shepherd.shopdawg.app), the production AI platform I built for e-bike repair shops.

**[View the slides](https://bartrumb.github.io/ai-search-cloudflare/)**, or [download the PDF](AI-Powered%20Hybrid%20Search%20%26%20Agentic%20Assistants%20on%20Cloudflare%20%E2%80%94%20OPO%20Startups.pdf).

This is the talk as I gave it. Shepherd has kept changing since; the current numbers are on [brett.bartrum.family](https://brett.bartrum.family).

## What the talk covers

30 slides, in this order:

- **Why I built it:** it starts at a bike shop's workbench. Traditional search infrastructure bills you every month whether or not anyone searches; the edge changes that math.
- **The search stack, explained like a shop:** find the right aisle with Vectorize (semantic search), pick off the shelf with D1 and Meilisearch (faceted search), and scan the barcode with D1's FTS5 (keyword search), then merge keyword and vector results.
- **Documents:** a PDF pipeline (OCR, extract, optimize), why chunk context matters, and contextual retrieval.
- **Agents:** from RAG to agentic AI, a Durable Object per user (Cloudflare's Project Think), offloading bulk work to cheap sub-agents, and query-aware compression.
- **When retrieval isn't enough:** a hand-built diagnostic knowledge graph, why it beat LLM extraction, and walking from a symptom to a diagram live.
- **Running it:** observability in one pane of glass, real-world scale, and a cost comparison with a traditional search stack.
- **Lessons from production**, then two ways to build it yourself: Cloudflare's managed AI Search to start, or the same primitives for full control.

## How to use it

Open `ai-search-cloudflare.html` in a modern browser, or use the link above. The file is self-contained and works offline: reveal.js, its notes plugin and the three typefaces are inlined, so there's nothing to build or install.

| Key | Action |
|-----|--------|
| `→` / `Space` | Next slide |
| `←` | Previous slide |
| `Esc` | Slide overview |
| `S` | Speaker notes |
| `M` | Slide menu and table of contents |
| `H` | Keyboard shortcuts |
| `F` | Fullscreen |

**Print or save as PDF:** press `M`, then **Print / Export PDF**. In Chrome, choose Save as PDF with a custom paper size of 13.333 × 7.5 in. Adding `?print-pdf` to the address gives the same one-slide-per-page layout.

## How it's built

| Part | What |
|------|------|
| Slides | [reveal.js 5.1.0](https://revealjs.com) (MIT), inlined, with the notes plugin |
| Typefaces | Inter, Playfair Display and JetBrains Mono (SIL OFL), embedded |
| Charts and diagrams | Hand-written inline SVG with CSS animations; no charting library |
| Build step | None: one HTML file |

Print mode turns the animations off, so every chart prints in its final state.

## About me

I'm Brett Bartrum, a platform and AI infrastructure engineer in St. Louis. I've spent 20 years keeping enterprise production running, and I built Shepherd on my own. More, including my 2023 talk [Show-Me Artificial Intelligence](https://www.youtube.com/watch?v=lweCB1GMzbg), is at [brett.bartrum.family](https://brett.bartrum.family). Email: [brett@bartrum.family](mailto:brett@bartrum.family).

Layout, diagrams and copy were iterated with Claude (Anthropic) in [Claude Code](https://claude.ai/code).

### Cloudflare resources from the talk

- [D1](https://developers.cloudflare.com/d1)
- [Vectorize](https://developers.cloudflare.com/vectorize)
- [Workers AI](https://developers.cloudflare.com/workers-ai)
- [Cloudflare for Startups](https://www.cloudflare.com/startups/)
- [Blog: the AI Search primitive](https://blog.cloudflare.com/ai-search-agent-primitive/)
- [Blog: Project Think](https://blog.cloudflare.com/project-think/)

## License

Presentation content © 2026 Brett Bartrum / Shop DAWG. reveal.js is MIT licensed.

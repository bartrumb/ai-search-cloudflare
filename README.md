# AI Search on Cloudflare — Conference Deck

Self-contained reveal.js presentation for **"AI Search on Cloudflare"** — a talk given at OPO Startups (July 2026) by Brett Bartrum, founder of Shop DAWG / Shop Shepherd.

## What this is

A 28-slide technical conference deck covering the design, implementation, and lessons learned from building a production AI-powered search and repair assistant ([shepherd.shopdawg.app](https://shepherd.shopdawg.app)) entirely on Cloudflare's serverless stack.

Topics covered:

- **Cloudflare stack** — Workers, D1, KV, R2, Vectorize, Workers AI, Durable Objects
- **Search architecture** — FTS5 hybrid search, vector embeddings, progressive relaxation, MiniSearch
- **RAG pipeline** — Contextual Retrieval (Kimi K2.6 context summaries), Voyage rerank-2.5, structural reranking (Gemini)
- **Pre-agent / intent classification** — Cerebras Qwen-3-235B query optimizer running before every turn
- **Diagnostic knowledge graph** — 757 nodes, 1,739 edges, probability-ranked fault isolation
- **Mini-agents** — Cerebras GPT-OSS-120B and Kimi K2.6 for tool-output compression
- **Cost comparison** — 25× cheaper than the traditional Elastic + Pinecone + EC2 stack
- **Production lessons** — what bit us in order of impact

## How to use

Just open `ai-search-cloudflare.html` in a modern browser. No build step, no dependencies to install.

### Navigation

| Key | Action |
|-----|--------|
| `→` / `Space` | Next slide |
| `←` | Previous slide |
| `Esc` | Slide overview |
| `S` | Speaker notes |
| `M` | Slide menu / table of contents |
| `H` | Keyboard shortcuts help overlay |
| `F` | Fullscreen |

### Print / Export PDF

1. Press `M` to open the menu, then click **⎙ Print / Export PDF**
2. In Chrome: Print → Destination: Save as PDF → Paper: Custom 13.333 × 7.5 in
3. Or append `?print-pdf` to the URL and use Chrome's print dialog

The `?print-pdf` URL parameter activates the multi-page print layout (one PDF page per slide, 720px × 1280px each).

## Tech stack

| Component | Technology |
|-----------|------------|
| Slide framework | [reveal.js 5.1.0](https://revealjs.com) (MIT) |
| Typefaces | Inter, Playfair Display, JetBrains Mono (SIL OFL) |
| Charts & diagrams | Hand-authored inline SVG + CSS animations |
| Syntax highlighting | highlight.js (bundled in reveal.js) |
| Build step | None — single self-contained HTML file |

Every chart, bar graph, and diagram is hand-authored SVG with CSS keyframe animations (`@keyframes gdGrow`). No charting library. Print mode freezes animations via `animation: none !important` on `html.print-pdf-active`.

## Credits

Designed and built by **Brett Bartrum** ([brett@shopdawg.app](mailto:brett@shopdawg.app))  
Layout, diagrams, and copy iterated with **Claude** (Anthropic) in [Claude Code](https://claude.ai/code).

### Cloudflare resources mentioned

- [developers.cloudflare.com/d1](https://developers.cloudflare.com/d1)
- [developers.cloudflare.com/vectorize](https://developers.cloudflare.com/vectorize)
- [developers.cloudflare.com/workers-ai](https://developers.cloudflare.com/workers-ai)
- [cloudflare.com/startups](https://www.cloudflare.com/startups/)
- [blog: AI Search primitive](https://blog.cloudflare.com/ai-search-agent-primitive/)
- [blog: Project Think](https://blog.cloudflare.com/project-think/)

## License

Presentation content © 2026 Brett Bartrum / Shop DAWG. reveal.js is MIT licensed.

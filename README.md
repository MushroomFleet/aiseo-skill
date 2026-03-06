# 🤖 AISEO Skill — AI-Friendly SEO for Claude

A Claude skill that performs a full site audit and implements AI-friendly SEO across any static HTML website in a single pass. Generates `sitemap.xml`, `robots.txt`, `llms.txt`, `llms-full.txt`, Open Graph metadata, JSON-LD structured data, `security.txt`, and `humans.txt` — with ready-to-use code at every step.

---

## ✨ What It Does

When triggered, AISEO:

1. **Audits your site** — scans all HTML files, classifies pages (index / collection / detail / utility), and detects what's missing
2. **Reports gaps** — prints a concise summary of what needs to be added before touching anything
3. **Outputs actionable steps** — numbered instructions with exact code blocks, ready to copy-paste or execute directly

### The 8-Phase Implementation

| Phase | Output |
|---|---|
| 1 | Enhanced HTML metadata (canonical, Open Graph, Twitter Card, theme-color, robots) |
| 2 | `sitemap.xml` — all non-utility pages with priority and lastmod |
| 3 | `robots.txt` — allows all crawlers including GPTBot, Claude-Web, PerplexityBot |
| 4 | `llms.txt` — concise AI directory (llmstxt.org spec) |
| 5 | JSON-LD structured data — WebSite, CollectionPage, Article schemas |
| 6 | `llms-full.txt` — extended content index for AI agents |
| 7 | `security.txt` — RFC 9116 security contact file |
| 8 | `humans.txt` — credits and tech stack |

All injected content is wrapped in comment markers, making re-runs fully idempotent — existing content is never destroyed, only enhanced.

---

## 🚀 How to Use

### Trigger Phrase

```
we can use the aiseo skill to [describe your site or paste HTML/file tree here]
```

### Example

```
we can use the aiseo skill to implement full AI-friendly SEO on my site.

Site directory: ./web
Base URL: https://mushroomfleet.github.io/my-project
```

Claude will audit the provided HTML or codebase, print a gap report, then output all implementation steps with complete code.

---

## 📦 Installation

### Option 1 — Claude.ai (Web / Mobile)

1. Download `aiseo.skill` from the [Releases](https://github.com/MushroomFleet/aiseo-skill/releases) page
2. Open [claude.ai](https://claude.ai) → **Settings** → **Skills**
3. Upload `aiseo.skill`
4. The skill is now available in all conversations

### Option 2 — Claude Code CLI

Unzip `aiseo.skill` directly into your Claude Code commands directory:

```bash
unzip aiseo.skill -d ~/.claude/commands/
```

The skill folder will be placed at `~/.claude/commands/aiseo/` and Claude Code will detect it automatically on next launch.

> **Note:** `aiseo.skill` is a standard zip archive — you can inspect or modify its contents before installing.

---

## 📁 Skill Contents

```
aiseo/
├── SKILL.md                              # Skill instructions and phase templates
└── references/
    └── SEO-metadata-AI-friendly-plan.md  # Full source plan (edge cases, SPA/SSG/CMS adaptations)
```

---

## 🔧 Requirements

- Claude Sonnet or Opus (any version with skill support)
- A static HTML website, codebase, or website plan to provide as input
- `BASE_URL` and `SITE_DIR` (Claude will ask if it can't detect them)

---

## 📚 Citation

### Academic Citation

If you use this codebase in your research or project, please cite:

```bibtex
@software{aiseo_skill,
  title = {AISEO Skill: AI-Friendly SEO Implementation for Claude},
  author = {[Drift Johnson]},
  year = {2025},
  url = {https://github.com/MushroomFleet/aiseo-skill},
  version = {1.0.0}
}
```

### Donate:

[![Ko-Fi](https://cdn.ko-fi.com/cdn/kofi3.png?v=3)](https://ko-fi.com/driftjohnson)

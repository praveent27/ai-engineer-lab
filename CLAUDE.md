# AI Engineer Lab — Project Context

## What This Is
A GitHub Pages site documenting a 28-week journey from Data Engineer to AI Engineer, aligned to Microsoft AI-102 certification. Each week has a notes page (HTML), Jupyter notebooks, cheat sheets, and 20 self-assessment flashcards.

## Site URL
https://praveent27.github.io/ai-engineer-lab/

## Structure
```
├── index.html                      # Landing page — 28-week roadmap, GPU guide, process
├── CLAUDE.md                       # This file
├── README.md
└── weeks/
    └── week-XX/
        ├── index.html              # Notes page: day summaries, concepts, cheat sheet, flashcards
        ├── Day1_Topic.ipynb        # Jupyter notebooks (one per study day)
        └── ...
```

## Design System (MUST follow for consistency)
- Dark theme: bg `#0a0e17`, surface `#111827`, border `#1e293b`
- Fonts: DM Serif Display (headings), IBM Plex Mono (labels/code), Source Sans 3 (body)
- Loaded via Google Fonts CDN
- Accent: `#f59e0b` (amber). Blue: `#3b82f6`. Green: `#22c55e`. Purple: `#a78bfa`. Cyan: `#22d3ee`
- All HTML is static — no build tools, no frameworks. Pure HTML/CSS/JS.
- Copy the exact CSS from `weeks/week-01/index.html` for new week pages

## Key Components in Week Pages
1. **Day sections**: concept cards (`.concept`), key takeaways (`.takeaways`), ML mapping tables (`.ml-map`)
2. **Cheat sheet**: tables with `.cheat-table` class
3. **Flashcards**: 20 click-to-reveal cards (`.flashcard`) with topic tags and score counter
4. **Notebook links**: `.notebook-link` badges

## When Creating a New Week
1. Create `weeks/week-XX/` directory
2. Copy CSS/structure from week-01 `index.html` as template
3. Update: week number, phase, title, day content, concepts, takeaways, cheat sheet, flashcards
4. Generate .ipynb notebooks (JSON format, nbformat 4, nbformat_minor 5)
5. Update `index.html` landing page: mark new week as `.active`, previous week remove `.active` class and remove `.locked` class

## Notebook Format
- Raw JSON .ipynb files (nbformat 4)
- Each cell needs unique `id` field
- Markdown cells: `cell_type: "markdown"`, source as array of lines
- Code cells: `cell_type: "code"`, source as array of lines, `execution_count: null`, `outputs: []`
- Include explanatory markdown between code cells
- End each notebook with exercises + solutions

## Git Workflow
- Branch naming: `feat/week-XX-topic-name`
- Commit message: `feat: add Week XX — Topic Name`
- Always create feature branch, never commit directly to main
- PR title: `feat: Week XX — Topic Name`

## Identity Rules
- Author: Praveen Kumar Thumati
- NEVER mention KPMG
- NEVER use "Data Architect" as a role — use "Data Engineer" instead
- Portfolio link: https://praveent27.github.io

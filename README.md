# Co4Pilot

> **4P Framework for Academic Research** — People · Project · Paper · Patent

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-blueviolet)](https://claude.ai)
[![Skills](https://img.shields.io/badge/Skills-53-green)](./skills/)

## What is Co4Pilot?

**Co4Pilot** is an AI-powered toolkit that covers the complete academic research lifecycle through four pillars:

| Pillar | What it covers | Skills |
|--------|---------------|--------|
| **👥 People** | Student mentoring, teaching, career development | 13 |
| **📋 Project** | Proposals, execution, data management | 12 |
| **📝 Paper** | Literature, writing, peer review, academic impact | 14 |
| **💡 Patent** | Mining, disclosure, drafting, office actions | 4 |
| **🔧 Domains** | Domain-specific extensions (AD Safety, ...) | 10 |

Built on [Claude Code](https://claude.ai), each skill contains actionable frameworks, templates, checklists, and prompt templates — sourced from MIT, Stanford, Harvard, CMU and other top universities' best practices.

## The 4P Architecture

```
Co4Pilot/
│
├── skills/
│   ├── people/                    👥 People (13 skills)
│   │   ├── mentoring/               Student supervision
│   │   │   ├── undergrad-thesis       28-week undergraduate thesis guide
│   │   │   ├── master-program         2-3 year master's roadmap
│   │   │   ├── phd-program            4-5 year PhD lifecycle (IDP, milestones)
│   │   │   ├── research-direction     Gap identification, feasibility matrix
│   │   │   └── progress-tracking      Milestone tables, early warning system
│   │   ├── teaching/                Course design & delivery
│   │   │   ├── course-design          Backward design (Wiggins & McTighe)
│   │   │   ├── syllabus               Learning-centered syllabus design
│   │   │   ├── exam-design            Bloom's taxonomy, rubric creation
│   │   │   └── teaching-reform        SoTL framework, teaching portfolio
│   │   └── career/                  Academic career development
│   │       ├── cv-maintenance         13-section academic CV structure
│   │       ├── citation-tracking      H-index, altmetrics, alert setup
│   │       └── talent-program         杰青/优青/长江 application prep
│   │
│   ├── project/                   📋 Project (12 skills)
│   │   ├── proposal/                Grant & project proposals
│   │   │   ├── proposal-writing       Universal framework for any funder
│   │   │   ├── provincial-fund        Provincial/local funding landscape
│   │   │   ├── industry-project       Industry contracts, IP negotiation
│   │   │   └── defense-prep           ACE framework, Q&A strategies
│   │   ├── execution/               Project management
│   │   │   ├── midterm-report         Risk assessment, progress tracking
│   │   │   ├── final-report           Impact assessment, sustainability
│   │   │   ├── budget-management      8 categories, compliance essentials
│   │   │   └── audit-prep             Documentation checklist, self-audit
│   │   └── data/                    Research data management
│   │       ├── data-collection-plan   FAIR principles, DMP template
│   │       ├── annotation-guide       IAA metrics, 8 annotation tools
│   │       ├── dataset-release        Datasheets framework, 8 licenses
│   │       └── data-agreement         DUA/DTA/MTA/NDA templates
│   │
│   ├── paper/                     📝 Paper (14 skills)
│   │   ├── literature/              Literature research
│   │   │   ├── literature-search      PICO, 12 databases, Boolean syntax
│   │   │   ├── literature-review      PRISMA 2020, 5-stage workflow
│   │   │   ├── paper-reading          Keshav three-pass method
│   │   │   └── reference-management   Zotero advanced + BibTeX
│   │   ├── writing/                 Paper composition
│   │   │   ├── research-paper         SPJ + Widom + IMRAD + ABT
│   │   │   ├── review-paper           7 review types, PRISMA methodology
│   │   │   ├── conference-paper       Page budget, CCF ranking, conversion
│   │   │   ├── cover-letter           Section-by-section template
│   │   │   ├── rebuttal               CALM method, diplomatic language
│   │   │   └── revision               Triage system, latexdiff guide
│   │   ├── review/                  Peer review
│   │   │   ├── review-writing         Structured review template
│   │   │   └── editor-communication   Email templates, appeal strategy
│   │   └── impact/                  Academic dissemination
│   │       ├── wechat-article         Content strategy, headline formulas
│   │       ├── linkedin-post          Algorithm, hook patterns
│   │       ├── invited-talk           Assertion-Evidence slides, Q&A
│   │       └── media-interview        Message triangle, bridging
│   │
│   └── patent/                    💡 Patent (4 skills)
│       ├── patent-mining              5 mining methods, portfolio strategy
│       ├── disclosure                 Timing rules, TTO process
│       ├── patent-drafting            Claims, specification, PCT strategy
│       └── office-action              US/CN/EP rejection responses
│
│   └── domains/                 🔧 Domain Extensions (10 skills)
│       └── ad-safety/             AD Safety (Dr. Wang Cheng, RoboSafe-Lab)
│           ├── ad-safety-research   Orchestrator for AD safety research
│           ├── ad-scenario-analysis Scenario analysis, ODD, HARA, STPA
│           ├── ad-standards-navigator ISO 26262, ISO 21448, UL 4600
│           ├── ad-literature-review AD-specific venue search (IV, ITSC, T-ITS)
│           ├── ad-paper-writing     AD safety paper conventions
│           ├── ad-experiment-design CARLA, SUMO, CommonRoad experiments
│           ├── ad-dataset-analysis  FARS, GIDAS, SHRP2, crash data
│           ├── ad-behavior-modeling Trajectory prediction, interaction models
│           ├── ad-foundation-models VLAs, E2E driving, LLM safety
│           └── ad-generative-models World models, diffusion, 3DGS for AD
│
├── agents/                        11 composite agents
├── workflows/                     5 end-to-end workflows
├── install.sh                     Append-only installation
└── LICENSE                        MIT
```

## Domain Extensions

The 4P framework provides universal academic skills. **Domain extensions** layer discipline-specific expertise on top:

| Domain | Skills | Contributor | Focus |
|--------|--------|------------|-------|
| **AD Safety** | 10 | [Dr. Wang Cheng](https://github.com/RoboSafe-Lab) (Northumbria University) | SOTIF, scenario testing, safety assurance, V&V, foundation models for AD |

See [skills/domains/README.md](skills/domains/README.md) for the full list and contribution guide.

### Contributing Domain Extensions

Are you an expert in medical research, legal analysis, social science, materials science, or another field? You can contribute a domain extension:

1. Create `skills/domains/your-domain/` with skill files following the Co4Pilot template
2. Each skill should contain: overview, frameworks, templates, prompt templates, references
3. Submit a PR — see [skills/domains/README.md](skills/domains/README.md) for details

Your domain expertise + Co4Pilot's AI framework = powerful research tools for your entire field.

## Quick Start

```bash
git clone https://github.com/zyx312/Co4Pilot.git
cd Co4Pilot
./install.sh
```

Your existing dev environment stays untouched — everything installs with an `academic-` prefix. Uninstall: `./install.sh --uninstall`

## Why "4P"?

Academic researchers juggle four distinct types of work every day. Most AI tools treat research as a monolith. Co4Pilot recognizes that **mentoring a PhD student** requires fundamentally different skills than **responding to reviewer comments** or **drafting a patent claim** or **writing a midterm project report**.

The 4P framework ensures nothing falls through the cracks:

- **People** — Who are you developing? (students, yourself, your team)
- **Project** — What are you delivering? (proposals, reports, data)
- **Paper** — What are you publishing? (papers, talks, articles)
- **Patent** — What are you protecting? (inventions, IP, disclosures)

## Content Quality

Every skill file contains 200-500 lines of substantive content:
- **Actionable frameworks** from MIT, Stanford, Harvard, CMU, Oxford
- **Step-by-step templates** you can use immediately
- **Claude prompt templates** for AI-assisted workflows
- **Quality checklists** to catch common mistakes
- **Tool recommendations** with specific setup guides

Total: **53 skill files (43 core + 10 domain), 18,900+ lines of content.**

## Roadmap

- [x] Phase 1: Core skills (paper writing, rebuttal, literature review, PhD mentoring, patent mining)
- [x] Phase 2: All 43 skills with deep content
- [x] Phase 3: GitHub open-source best practices integration (gpt_academic, awesome-phd-advice, etc.)
- [ ] Phase 4: 11 agent system prompts
- [ ] Phase 5: 5 end-to-end workflow automation
- [ ] Phase 6: Community contributions

## Inspired By & Credits

This project was inspired by [automotive-claude-code-agents](https://github.com/theja0473/automotive-claude-code-agents) by Thejeswarareddy R (Bosch), which demonstrated how domain-specific knowledge can be systematically integrated into AI coding assistants.

**Domain Extension Contributors:**
- **Dr. Wang Cheng** ([RoboSafe-Lab](https://github.com/RoboSafe-Lab), Northumbria University) — AD Safety domain extension (10 skills covering SOTIF, scenario analysis, standards navigation, behavior modeling, foundation models, generative models, and more). A collaborator of Prof. Zhang Yuxin on autonomous driving safety research.

**Paper Writing Enhancement Sources:**
- [Research-Paper-Writing-Skills](https://github.com/Chen-Qifeng/Research-Paper-Writing-Skills) (Chen Qifeng Lab, HKUST) — Backward reasoning logic map, method three-element framework, introduction template patterns, figure design principles.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). PRs welcome — especially for:
- Discipline-specific skills (medical, legal, social science)
- Language-specific writing guides (German, Japanese, Korean academic conventions)
- Tool integration guides (Overleaf, Zotero, VOSviewer workflows)

## Author

**Yuxin Zhang** — Professor at Jilin University, School of Automotive Engineering. Research: autonomous driving safety, SOTIF, scenario-based testing.

## License

MIT — use freely in academic and commercial contexts.

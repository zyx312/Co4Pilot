# Co4Pilot

> **AI-powered copilot for the 4Ps of academic life: People . Project . Paper . Patent**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-blueviolet)](https://claude.ai)
[![Skills](https://img.shields.io/badge/Core_Skills-45-green)](./skills/)

## What is Co4Pilot?

**Co4Pilot** is an AI-powered copilot that covers the complete academic research lifecycle through four pillars -- the **4P Framework**. Built on [Claude Code](https://claude.ai), it provides 45 actionable skill files with frameworks, templates, checklists, and prompt templates sourced from MIT, Stanford, Harvard, CMU, and other top universities' best practices.

## The 4P Framework

| Pillar | Subcategories | Skills | What it covers |
|--------|--------------|--------|---------------|
| **People** | mentoring (5), teaching (4), career (3), team management (1) | **13** | Student supervision, course design, career development, lab management |
| **Project** | proposal (4), execution (4), data management (4) | **12** | Grant writing, project reports, budgets, research data |
| **Paper** | literature (4), writing (6), review (2), impact (4) | **16** | Literature research, paper composition, peer review, dissemination |
| **Patent** | mining, disclosure, drafting, office action | **4** | Invention mining, IP protection, patent prosecution |
| | | **45 total** | |

## Architecture

```
Co4Pilot
|
+-- skills/
|   +-- people/                       People (13 skills)
|   |   +-- mentoring/                  Student supervision
|   |   |   +-- undergrad-thesis          28-week undergraduate thesis guide
|   |   |   +-- master-program            2-3 year master's roadmap
|   |   |   +-- phd-program               4-5 year PhD lifecycle
|   |   |   +-- research-direction        Gap identification, feasibility matrix
|   |   |   +-- progress-tracking         Milestone tables, early warning system
|   |   +-- teaching/                   Course design & delivery
|   |   |   +-- course-design             Backward design (Wiggins & McTighe)
|   |   |   +-- syllabus                  Learning-centered syllabus design
|   |   |   +-- exam-design               Bloom's taxonomy, rubric creation
|   |   |   +-- teaching-reform           SoTL framework, teaching portfolio
|   |   +-- career/                     Academic career development
|   |   |   +-- cv-maintenance            13-section academic CV structure
|   |   |   +-- citation-tracking         H-index, altmetrics, alert setup
|   |   |   +-- talent-program            National talent program application prep
|   |   +-- team-management             Lab culture, roles, conflict resolution
|   |
|   +-- project/                      Project (12 skills)
|   |   +-- proposal/                    Grant & project proposals
|   |   |   +-- proposal-writing          Universal framework for any funder
|   |   |   +-- provincial-fund           Provincial/local funding landscape
|   |   |   +-- industry-project          Industry contracts, IP negotiation
|   |   |   +-- defense-prep              ACE framework, Q&A strategies
|   |   +-- execution/                   Project management
|   |   |   +-- midterm-report            Risk assessment, progress tracking
|   |   |   +-- final-report              Impact assessment, sustainability
|   |   |   +-- budget-management         8 categories, compliance essentials
|   |   |   +-- audit-prep               Documentation checklist, self-audit
|   |   +-- data/                        Research data management
|   |       +-- data-collection-plan      FAIR principles, DMP template
|   |       +-- annotation-guide          IAA metrics, 8 annotation tools
|   |       +-- dataset-release           Datasheets framework, 8 licenses
|   |       +-- data-agreement            DUA/DTA/MTA/NDA templates
|   |
|   +-- paper/                        Paper (16 skills)
|   |   +-- literature/                  Literature research
|   |   |   +-- literature-search         PICO, 12 databases, Boolean syntax
|   |   |   +-- literature-review         PRISMA 2020, 5-stage workflow
|   |   |   +-- paper-reading             Keshav three-pass method
|   |   |   +-- reference-management      Zotero advanced + BibTeX
|   |   +-- writing/                     Paper composition
|   |   |   +-- research-paper            SPJ + Widom + IMRAD + ABT
|   |   |   +-- review-paper              7 review types, PRISMA methodology
|   |   |   +-- conference-paper          Page budget, CCF ranking, conversion
|   |   |   +-- cover-letter              Section-by-section template
|   |   |   +-- rebuttal                  CALM method, diplomatic language
|   |   |   +-- revision                  Triage system, latexdiff guide
|   |   +-- review/                      Peer review
|   |   |   +-- review-writing            Structured review template
|   |   |   +-- editor-communication      Email templates, appeal strategy
|   |   +-- impact/                      Academic dissemination
|   |       +-- wechat-article            Content strategy, headline formulas
|   |       +-- linkedin-post             Algorithm, hook patterns
|   |       +-- invited-talk              Assertion-Evidence slides, Q&A
|   |       +-- media-interview           Message triangle, bridging
|   |
|   +-- patent/                       Patent (4 skills)
|   |   +-- patent-mining                 5 mining methods, portfolio strategy
|   |   +-- disclosure                    Timing rules, TTO process
|   |   +-- patent-drafting               Claims, specification, PCT strategy
|   |   +-- office-action                 US/CN/EP rejection responses
|   |
|   +-- domains/                      Domain Extensions
|       +-- ad-safety/                    AD Safety (10 skills)
|
+-- agents/                           9 composite agents
+-- workflows/                        5 end-to-end workflows
+-- install.sh                        Append-only installation
+-- LICENSE                           MIT
```

## Domain Extensions

The 4P framework provides universal academic skills. **Domain extensions** layer discipline-specific expertise on top:

| Domain | Skills | Contributor | Focus |
|--------|--------|------------|-------|
| **AD Safety** | 10 | [Dr. Cheng Wang](https://github.com/RoboSafe-Lab) (Heriot-Watt University) | SOTIF, scenario testing, safety assurance, V&V, foundation models for AD |

See [skills/domains/README.md](skills/domains/README.md) for the full list and contribution guide.

### Contributing Domain Extensions

Are you an expert in medical research, legal analysis, social science, materials science, or another field? You can contribute a domain extension:

1. Create `skills/domains/your-domain/` with skill files following the Co4Pilot template
2. Each skill should contain: overview, frameworks, templates, prompt templates, references
3. Submit a PR -- see [skills/domains/README.md](skills/domains/README.md) for details

**Example**: The [ad-safety-research-skills](https://github.com/RoboSafe-Lab) extension by Dr. Cheng Wang adds 10 specialized skills for autonomous driving safety research (SOTIF, scenario analysis, standards navigation, behavior modeling, foundation models). Your domain expertise + Co4Pilot's AI framework = powerful research tools for your entire field.

## Quick Start

```bash
git clone https://github.com/zyx312/Co4Pilot.git
cd Co4Pilot
./install.sh
```

Your existing dev environment stays untouched -- everything installs with a `co4pilot-` prefix. To uninstall:

```bash
./install.sh --uninstall
```

## Why "4P"?

Academic researchers juggle four distinct types of work every day. Most AI tools treat research as a monolith. Co4Pilot recognizes that **mentoring a PhD student** requires fundamentally different skills than **responding to reviewer comments** or **drafting a patent claim** or **writing a midterm project report**.

The 4P framework ensures nothing falls through the cracks:

- **People** -- Who are you developing? (students, yourself, your team)
- **Project** -- What are you delivering? (proposals, reports, data)
- **Paper** -- What are you publishing? (papers, talks, articles)
- **Patent** -- What are you protecting? (inventions, IP, disclosures)

## Content Quality

Every skill file contains 200-500 lines of substantive content:
- **Actionable frameworks** from MIT, Stanford, Harvard, CMU, Oxford
- **Step-by-step templates** you can use immediately
- **Claude prompt templates** for AI-assisted workflows
- **Quality checklists** to catch common mistakes
- **Tool recommendations** with specific setup guides

Total: **45 core skills + 10 domain skills = 55 skill files.**

## Credits

This project was inspired by [automotive-claude-code-agents](https://github.com/theja0473/automotive-claude-code-agents) by Thejeswarareddy R (Bosch), which demonstrated how domain-specific knowledge can be systematically integrated into AI coding assistants.

Co4Pilot also incorporates insights from:
- [academic-research-skills](https://github.com/) -- General academic research methodology
- [AI-Research-SKILLs](https://github.com/) -- AI-assisted research workflows
- [Research-Paper-Writing-Skills](https://github.com/Chen-Qifeng/Research-Paper-Writing-Skills) (Chen Qifeng Lab, HKUST) -- Backward reasoning logic map, method three-element framework, introduction template patterns, figure design principles
- [ad-safety-research-skills](https://github.com/RoboSafe-Lab) -- AD safety domain extension by Dr. Cheng Wang

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). PRs welcome -- especially for:
- Discipline-specific domain extensions (medical, legal, social science, materials)
- Language-specific writing guides (German, Japanese, Korean academic conventions)
- Tool integration guides (Overleaf, Zotero, VOSviewer workflows)

## Author

**Yuxin Zhang** -- Professor at Jilin University, School of Automotive Engineering. Research: autonomous driving safety, SOTIF, scenario-based testing.

## License

MIT -- use freely in academic and commercial contexts.

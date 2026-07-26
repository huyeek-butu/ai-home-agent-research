# AI Home Agent / Open-Source Continual Learning — Research Series

> A curated knowledge base on **AI home agents** and **open-source continual learning**: 9 research notes plus multi-channel publishing assets (Zhihu draft / WeChat draft / PDF / PPT) for 6 in-depth reports.
> 中文版：[README.md](README.md)

---

## 1. Overview

This repository is maintained by an independent researcher (不土老师 / "Butu") to **permanently archive** a series of studies on AI home agents and open-source continual learning as searchable, reusable, and distributable content assets.

- **Research scope**: industry trends, technical roadmap, and spillover effects on business/industry of AI home agents; how open-source continual learning reshapes large-model capability evolution.
- **Content forms**: raw research notes (Markdown) + in-depth reports (with external authoritative citations) + multi-channel publishing assets per report.
- **Channels**: Zhihu (primary, clickable external links), industry-media submissions, WeChat Official Account, and GitHub (primary archive).
- **Principle**: archive-first; publish on Zhihu and industry media in batches rather than all at once.

---

## 2. Content Index

### 2.1) Research notes ([`sources/`](sources/))

12 source files in three categories:

| Category | Title | Note |
|---|---|---|
| KB original framework | [AI Home Agent — Seven Trends](sources/AI家庭智能体七大趋势.md) | Original, no external citations |
| KB original framework | [AI Home Agent — Three-Stage Evolution Path](sources/AI家庭智能体三阶段路径.md) | Original, no external citations |
| KB original framework | [AI Home Agent — Industry & Investment Map](sources/AI家庭智能体产业与投资图谱.md) | Original, no external citations |
| KB original framework | [Open-Source Continual Learning Reshaping Home Agents](sources/开源持续学习重塑家庭Agent.md) | Original, no external citations |
| KB original framework | [Open-Source Continual Learning Reshaping Industry & Business](sources/开源持续学习重塑工业商业.md) | Original, no external citations |
| In-depth (cited) | [AI Home-Butler Agent Trend Study](sources/AI家庭管家Agent趋势研究报告.md) | IDC / 36Kr citations |
| In-depth (cited) | [Seven Trends — In-Depth Research](sources/AI家庭智能体七大趋势深度调研报告.md) | Authoritative data |
| In-depth (cited) | [Three-Stage Path — In-Depth Research](sources/AI家庭智能体三阶段路径深度调研报告.md) | Authoritative data |
| In-depth (cited) | [Impact on Industry & Business](sources/AI家庭智能体对工商业的影响深度调研报告.md) | Authoritative data |
| In-depth (cited) | [Open-Source Continual Learning Reshaping Home Agents — In-Depth](sources/开源持续学习重塑家庭Agent深度调研报告.md) | Authoritative data |
| In-depth (cited) | [LLM Technical Ontology & Industry/Business Deployment Observations](sources/开源持续学习的大模型技术本体与工业商业落地观察.md) | Authoritative data |
| Archive only (unpublished) | [Open-Source Continual Learning × Self-Organizing Hardware Evolution](sources/开源持续学习自组织硬件演化.md) | Personal note, forward-looking |

> KB notes have their Obsidian `[[wikilinks]]` stripped before publishing; in-depth reports carry external authoritative citations (IDC / NIST / 36Kr / QbitAI, etc.).

### 2.2) Multi-channel assets for in-depth reports ([`articles/`](articles/))

Each of the 6 in-depth reports ships 5 publishing assets (see [Section 4](#4-asset-format-reference)):

| # | Title | Directory | Assets |
|---|---|---|---|
| 01 | AI Home-Butler Agent Trend Study | `articles/trend-report/` | clean / Zhihu / WeChat / PDF / PPT |
| 02 | Seven Trends — In-Depth Research | `articles/seven-trends/` | clean / Zhihu / WeChat / PDF / PPT |
| 03 | Three-Stage Path — In-Depth Research | `articles/three-stage/` | clean / Zhihu / WeChat / PDF / PPT |
| 04 | Impact on Industry & Business | `articles/industry-impact/` | clean / Zhihu / WeChat / PDF / PPT |
| 05 | Open-Source Continual Learning Reshaping Home Agents | `articles/open-source-cl/` | clean / Zhihu / WeChat / PDF / PPT |
| 06 | LLM Technical Ontology & Industry/Business Deployment | `articles/tech-ontology/` | clean / Zhihu / WeChat / PDF / PPT |

---

## 3. Read Online

- **GitHub Pages site** (portal + 9 web versions): https://huyeek-butu.github.io/ai-home-agent-research/
- Article pages (root `*.html` in the repo):
  - `01-seven-trends.html` Seven Trends (KB)
  - `02-trend-report.html` Trend Study (in-depth)
  - `03-seven-trends-deep.html` Seven Trends — In-Depth
  - `04-three-stage.html` Three-Stage Path (KB)
  - `05-three-stage-deep.html` Three-Stage Path — In-Depth
  - `06-industry-map.html` Industry & Investment Map (KB)
  - `07-oss-home-agent.html` Open-Source Reshaping Home Agents (KB)
  - `08-oss-industry.html` Open-Source Reshaping Industry & Business (KB)
  - `09-self-org-hardware.html` Self-Organizing Hardware Evolution (archive only)

---

## 4. Asset Format Reference

Each in-depth report directory contains 5 file types (example `01-trend-report.*`):

| File | Purpose |
|---|---|
| `<NN>-<name>.clean.md` | Clean body with internal markers / wikilinks removed; ready for reuse |
| `<NN>-<name>.zhihu.md` | Zhihu draft: external links kept, paste-ready |
| `<NN>-<name>.wechat.md` | WeChat draft: in-body links stripped, reference URLs kept; fits 秀米 / 135 editor |
| `<NN>-<name>.pdf` | A4-typeset PDF with clickable TOC and links |
| `<NN>-<name>.pptx` | 12-slide deck for talks / sharing |

---

## 5. Repository Structure

```text
ai-home-agent-research/
├── README.md                 # Chinese version
├── README_EN.md              # This file (English)
├── index.html                # Pages portal
├── 01~09-*.html              # 9 web article pages
├── .nojekyll                 # Enable static Pages site
├── sources/                  # 12 research-note sources (6 KB + 6 in-depth + 1 archive)
└── articles/                 # 6 in-depth reports × 5 assets = 30 files
    ├── trend-report/
    ├── seven-trends/
    ├── three-stage/
    ├── industry-impact/
    ├── open-source-cl/
    └── tech-ontology/
```

---

## 6. Publishing Status

| Channel | Status | Note |
|---|---|---|
| GitHub repo | ✅ Done | Content archived |
| GitHub Pages | ✅ Done | Site live |
| Zhihu | 🔶 1/6 published | First piece (Trend Study) published; 5 pending |
| WeChat Official Account | ⏳ Pending | `articles/**/*.wechat.md` ready |
| Industry media | ⏳ Pending | Suggest submitting investment / open-source pieces to 36Kr / 机器之心 |
| Self-Organizing Hardware | 🔒 Archive only | Not public |

> **Published (Zhihu)**: ① AI Home-Butler Agent Trend Study (No.01) → https://zhuanlan.zhihu.com/p/2064666382520825199

---

## 7. Roadmap

1. **Distribute & launch**: actually publish the 6 in-depth report assets (suggested order: Trend → Seven Trends → Three-Stage → Industry → Open-Source Home Agent → Technical Ontology); recycle reads / likes / followers to refine topics.
2. **Complete KB assets**: strip wikilinks from the remaining 4 KB notes and run the same pipeline, forming an 8-piece complete set, then package as IP (e-book / column / mini-course).
3. **Productize & community**: standardize production via the archived Skill; ship lightweight products (maturity checklist / reference architecture); explore new topics (safety / privacy / standardization).

---

## 8. License & Disclaimer

- Copyright belongs to the original author. Attribution and source link required for republication.
- Content is for research reference only and **does not constitute investment advice**.
- For commercial or reprint permissions, contact the author via repository Issues.

---

## 9. Related Resources

- Repo: https://github.com/huyeek-butu/ai-home-agent-research
- Site: https://huyeek-butu.github.io/ai-home-agent-research/
- Multi-channel asset Skill: `md-deep-report-multichannel` (user-level WorkBuddy Skill)

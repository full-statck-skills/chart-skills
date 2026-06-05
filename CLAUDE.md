# CLAUDE.md — chart-skills

Chart and data visualization Agent Skills for AI coding agents.
Part of the [Full Stack Skills](https://github.com/partme-ai/full-stack-skills) ecosystem, maintained by PartMe.AI.
Licensed under Apache 2.0.

## Skills (2)

| Skill | Library | Platform |
|-------|---------|----------|
| `lime-echart` | ECharts wrapper for UniApp/UniAppX | H5, mini-programs, App |
| `ucharts` | uCharts (`@qiun/ucharts`) | uni-app, WeChat Mini Program, H5, APP |

## Directory Structure

```
chart-skills/
├── .claude-plugin/plugin.json    # Plugin manifest (name, version, skill paths)
├── skills/
│   ├── lime-echart/
│   │   ├── SKILL.md              # Skill definition (YAML frontmatter + body)
│   │   ├── api/                  # Component, methods, events, options API docs
│   │   ├── examples/             # getting-started/, charts/, advanced/
│   │   ├── templates/            # basic-chart, advanced-chart, chart-with-data
│   │   └── LICENSE.txt
│   └── ucharts/
│       ├── SKILL.md              # Skill definition (YAML frontmatter + body)
│       ├── api/                  # chart-api, options-api, data-api, events-api, methods-api
│       ├── examples/             # guide/, charts/, features/
│       ├── templates/            # installation, basic-chart, configuration
│       └── LICENSE.txt
├── README.md                     # Bilingual (EN + zh-CN)
├── LICENSE                       # Apache 2.0
└── .gitignore
```

## SKILL.md Authoring Conventions

- **YAML frontmatter** (required): `name`, `description`, `license`
- **Body sections**: When to Use, How to Use, Examples/Templates, API Reference, Best Practices, Resources, Keywords
- **Bilingual UI keywords** in the body (e.g., "Line chart/折线图") to match user input in both EN and ZH
- **Doc mapping comment** links each section to the upstream official docs (e.g., uCharts `https://www.ucharts.cn/v2/#/`)
- **File references** use relative paths from the skill root (e.g., `examples/charts/line-chart.md`)
- **Templates** in `templates/` provide scaffolding; **examples** in `examples/` are tutorial material

## Key Files

| File | Purpose |
|------|---------|
| `.claude-plugin/plugin.json` | Registers skills with the plugin system |
| `skills/<name>/SKILL.md` | Entry point loaded on-demand by AI agents |
| `skills/<name>/api/` | API reference (loaded as needed by SKILL.md instructions) |
| `skills/<name>/examples/` | Example-driven how-to guides (loaded as needed) |

# Skills

![skills](https://img.shields.io/badge/skills-29-4d6bfe?style=flat-square)
![format](https://img.shields.io/badge/format-markdown-0d0d0d?style=flat-square)
![works with](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Cursor%20%7C%20Windsurf%20%7C%20Codex-6b7280?style=flat-square)
![license](https://img.shields.io/badge/license-MIT-16a34a?style=flat-square)

> One folder per job. Drop it in, and the agent stops guessing.

A library of markdown skills for AI coding agents. Every folder is a `SKILL.md` plus the reference files it needs, written so a model can pick it up mid-task and already know the patterns, the traps, and how the thing is actually built.

No frameworks. No install script. No plugin runtime. Just markdown a model reads before it writes code.

---

## Why this exists

Ask an agent for an Angular component and you get something plausible. Ask for an NgRx store and you get something plausible that fights the reducer. Ask for a chaos experiment and you get a YAML file that would take prod down.

Plausible is the problem. These skills replace guessing with specifics: the folder layout, the flag order, the query that actually uses the index, the thing you only learn after breaking it once.

They're not documentation for people. They're instructions for machines — short enough to load, opinionated enough to matter.

---

## The catalogue

### Design & frontend

| Skill | What it covers |
|---|---|
| [`accessibility`](accessibility/SKILL.md) | WCAG 2.1, screen readers, keyboard nav, focus management, ARIA. The checklist that stops you shipping something pretty and unusable. |
| [`design-systems`](design-systems/SKILL.md) | Design tokens, component libraries, type scales, colour theory, spacing systems. |
| [`angular-architect`](angular-architect/SKILL.md) | Angular 17+ standalone components, signals, NgRx, RxJS, routing, TestBed. Five reference files deep. |
| [`ai-elements`](ai-elements/SKILL.md) | AI chat UI primitives — streaming text, tool approval modals, message rendering. |
| [`animation`](animation/SKILL.md) | The 12 principles, keyframing, procedural motion, blend trees, export. |
| [`cross-platform`](cross-platform/SKILL.md) | React Native and Flutter conventions, native modules, shared state. |
| [`android-development`](android-development/SKILL.md) | Kotlin, Compose, MVVM, Hilt, Material 3, Play Store submission. |
| [`dashboard-builder`](dashboard-builder/SKILL.md) | Next.js dashboards on top of proxy APIs. Design by reference, verify with screenshots. |

### APIs & architecture

| Skill | What it covers |
|---|---|
| [`api-design`](api-design/SKILL.md) | REST conventions, response shapes, error envelopes, validation at the boundary. |
| [`api-designer`](api-designer/SKILL.md) | Full API architecture: OpenAPI 3.1, pagination strategies, versioning, RFC 7807 errors. |
| [`api-documentation`](api-documentation/SKILL.md) | Swagger/OpenAPI standards, interactive docs, SDK and cURL examples. |
| [`api-discovery`](api-discovery/SKILL.md) | Capture a site's traffic, work out how it delivers data, build a typed proxy for it. Includes session-harvest and rate-limit playbooks. |
| [`architecture-designer`](architecture-designer/SKILL.md) | ADRs, pattern trade-offs, NFR checklists, database selection, system design templates. |
| [`cloud-architect`](cloud-architect/SKILL.md) | AWS Well-Architected, landing zones, migration paths, cost and DR planning. |

### Data & databases

| Skill | What it covers |
|---|---|
| [`data-engineering`](data-engineering/SKILL.md) | Batch vs streaming, Lambda and Kappa, ETL/ELT, storage choice, data quality. |
| [`database-optimizer`](database-optimizer/SKILL.md) | Execution plans, index strategy, PostgreSQL and MySQL tuning, monitoring queries. |

### DevOps & reliability

| Skill | What it covers |
|---|---|
| [`devops-engineer`](devops-engineer/SKILL.md) | Dockerfiles, GitHub Actions, GitLab CI, Kubernetes, Terraform, releases, incident response. |
| [`ci-cd-pipelines`](ci-cd-pipelines/SKILL.md) | Pipeline design across GitHub Actions, GitLab, Jenkins, Azure DevOps. Deployment patterns. |
| [`ci-check`](ci-check/SKILL.md) | Run CI locally, then read the remote run and fix what actually broke. |
| [`chaos-engineer`](chaos-engineer/SKILL.md) | Hypothesis-driven failure injection, blast radius control, game days, post-mortems. |

### Languages & tooling

| Skill | What it covers |
|---|---|
| [`csharp-developer`](csharp-developer/SKILL.md) | .NET 8, Minimal APIs, EF Core, Blazor, `Span<T>`, Native AOT. |
| [`cli-developer`](cli-developer/SKILL.md) | Argument parsing, prompts, progress, shell completions — in Node, Python and Go. |
| [`debugging-wizard`](debugging-wizard/SKILL.md) | Systematic root-cause work. Binary search, git bisect, known bug patterns, three-fix threshold. |
| [`debug-logs`](debug-logs/SKILL.md) | Iterative `DEBUG()` logging: hypothesise, add logs, narrow, fix, clean up. |
| [`atlassian-mcp`](atlassian-mcp/SKILL.md) | Jira and Confluence over MCP. JQL, CQL, sprints, issue linking, auth. |

### Building & creative

| Skill | What it covers |
|---|---|
| [`app`](app/SKILL.md) | Turn a one-line idea into a working app: clarify, explore, build the API, build the dashboard. |
| [`brainstorming`](brainstorming/SKILL.md) | Ask before building. Turns a vague request into a real design doc, with an optional visual companion. |
| [`blender`](blender/SKILL.md) | Modelling, sculpting, rigging, Grease Pencil, export pipelines to Unity and Unreal. |
| [`asset-optimization`](asset-optimization/SKILL.md) | Poly reduction, LODs, texture compression, draw calls, per-platform budgets. |

---

## How a skill is built

```
angular-architect/
├── SKILL.md                # the rules the agent reads first
└── references/
    ├── components.md       # deep dives, loaded only when needed
    ├── ngrx.md
    ├── routing.md
    ├── rxjs.md
    └── testing.md
```

`SKILL.md` stays short and states the constraints — the things you must do and the things you must not. The `references/` files hold the long material: query patterns, manifests, runbooks, code skeletons.

That split is the whole trick. A model always reads the top file; it only pulls a reference when the task actually needs it. Keeps context small and keeps the rules sharp.

### The front matter

```yaml
---
name: angular-architect
description: Angular 17+ standalone components, signals, NgRx, RxJS, routing, testing.
---
```

The description is what decides whether the skill gets picked up at all. Write it in the words someone would actually type — the framework name, the version, the problem.

Some skills add a `metadata` block with triggers and a version. Nice to have, not required.

---

## Using them

**Claude Code**

```bash
git clone https://github.com/AxlZero21/Skills.git
cp -r Skills/* ~/.claude/skills/
```

**Cursor / Windsurf**

Copy the folder you need into the editor's rules directory, or paste `SKILL.md` into a project rule.

**Anything else**

`SKILL.md` is plain markdown with front matter. Drop it into the system prompt, the agent's context, or whatever your harness calls it. If the model can read, it can use this.

**Using one at a time** is the sane default. Installing all 29 means the model wades through 29 descriptions to find the one it needs. Copy what fits the project.

---

## Writing your own

1. Name the folder after the job, not the tool. `database-optimizer`, not `sql-helper`.
2. Put the hard rules in `SKILL.md` — the constraints that stop bad output.
3. Move anything long into `references/` and link to it by name.
4. Write imperatives. "Use `EXPLAIN (ANALYZE, BUFFERS)` before optimising" beats "it's good practice to consider performance."
5. Include one real code block. A pattern beats a paragraph describing the pattern.

---

## Credits

Several skills are adapted from [Jeffallan's claude-skills](https://github.com/Jeffallan/claude-skills) (MIT) — Angular Architect, API Designer, Architecture Designer, Atlassian MCP, Chaos Engineer, CLI Developer, C# Developer, Database Optimizer, Debugging Wizard, DevOps Engineer, Game Developer.

The `brainstorming` and `debugging-wizard` systematic-debugging material draws on [obra/superpowers](https://github.com/obra/superpowers) (MIT).

Everything else is written for this repo.

---

## License

MIT — see [LICENSE](LICENSE).

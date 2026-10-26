# Skills

![skills](https://img.shields.io/badge/skills-100%2B-4d6bfe?style=flat-square)
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
| `accessibility` | WCAG 2.1, screen readers, keyboard nav, focus, ARIA. The checklist that stops you shipping something pretty and unusable. |
| `design-systems` | Design tokens, component libraries, type scales, colour, spacing. |
| `angular-architect` | Angular 17+ standalone components, signals, NgRx, RxJS, routing, TestBed. |
| `react-expert` | React 19, Server Components, hooks, state management. |
| `nextjs-gen-ui` | Generative UI with Server Components and streaming AI responses. |
| `r3f-best-practices` | React Three Fiber — the `useFrame` and Zustand traps. |
| `ai-elements` | AI chat UI primitives — streaming text, tool approval modals. |
| `vercel-next-best-practices` | Next.js 15+ App Router, RSC boundaries, async params. |
| `animation` | The 12 principles, keyframing, procedural motion, blend trees. |
| `cross-platform` | React Native and Flutter conventions, native bridges. |
| `android-development` | Kotlin, Compose, MVVM, Hilt, Material 3. |
| `ios-development` | Swift, SwiftUI, async/await, App Store submission. |
| `flutter-expert` | Flutter 3, Riverpod, GoRouter, DevTools profiling. |
| `react-native-expert` | RN + Expo, list performance, navigation. |
| `swift-expert` | Swift 5.9+, `@Observable`, actors, protocol-oriented design. |
| `javascript-pro` | ES2023+, async, ESM, memory leaks. |
| `dashboard-builder` | Next.js dashboards on proxy APIs — design by reference, verify with screenshots. |

### Backend & APIs

| Skill | What it covers |
|---|---|
| `api-design` | REST conventions, response shapes, validation at the boundary. |
| `api-designer` | Full API architecture: OpenAPI 3.1, pagination, versioning, RFC 7807. |
| `api-documentation` | Swagger/OpenAPI standards, interactive docs, SDK examples. |
| `graphql-architect` | Schema design, Apollo Federation, DataLoader, subscriptions. |
| `csharp-developer` | .NET 8, Minimal APIs, EF Core, Blazor, `Span<T>`, AOT. |
| `java-architect` | Spring Boot 3.x, JPA, WebFlux, Security. |
| `spring-boot-engineer` | Spring Boot REST, Security 6, Actuator, migrations. |
| `python-pro` | Python 3.12+, typing, async, packaging. |
| `golang-pro` | Idiomatic Go, concurrency, `pprof`. |
| `rust-engineer` | Ownership, lifetimes, traits, Tokio. |
| `php-pro` | PHP 8.3+, Laravel, Symfony, PHPStan 9. |
| `rails-expert` | Rails 7+, Active Record, Hotwire, Sidekiq. |
| `orleans` | Microsoft Orleans virtual actors for distributed .NET. |
| `atlassian-mcp` | Jira and Confluence over MCP — JQL, CQL, sprints. |

### Architecture & workflow

| Skill | What it covers |
|---|---|
| `architecture-designer` | ADRs, pattern trade-offs, NFR checklists, system design. |
| `cloud-architect` | AWS Well-Architected, landing zones, migration, cost. |
| `api-discovery` | Capture a site's traffic, work out its transport, build a typed proxy. |
| `app` | Turn a one-line idea into a working app. |
| `brainstorming` | Ask before building. Vague request → real design doc. |
| `spec-miner` | Extract precise specifications from vague requests. |
| `subagent-driven-development` | Delegate well-scoped work and integrate results. |
| `requesting-code-review` / `receiving-code-review` | Get useful feedback, handle it without defensiveness. |
| `finishing-a-development-branch` | Close out a branch cleanly before merge. |
| `team-conventions` / `fullstack-conventions` / `gamedev-conventions` | Shared conventions, enforced not suggested. |
| `instruction-tuning` / `instruction-dashboard-tuning` | Write system instructions that actually stick. |
| `technical-writing` | Clear docs for developers, users, stakeholders. |

### Data & databases

| Skill | What it covers |
|---|---|
| `data-engineering` | Batch vs streaming, ETL/ELT, storage choice, data quality. |
| `database-optimizer` | Execution plans, index strategy, PostgreSQL/MySQL tuning. |
| `postgres-pro` | `EXPLAIN`, JSONB, GIN, replication, VACUUM. |
| `sql-pro` | Window functions, CTEs, query-plan analysis. |
| `pandas-pro` | Vectorized DataFrame work, no `iterrows()`. |
| `spark-engineer` | PySpark, shuffle tuning, structured streaming. |
| `statistical-analysis` | Hypothesis testing, A/B tests, time series. |

### DevOps & reliability

| Skill | What it covers |
|---|---|
| `devops-engineer` | Dockerfiles, CI/CD, Kubernetes, Terraform, incident response. |
| `ci-cd-pipelines` | Pipeline design across GitHub Actions, GitLab, Jenkins, Azure DevOps. |
| `ci-check` | Run CI locally, then read the remote run and fix what broke. |
| `infrastructure-as-code` / `terraform-engineer` | Remote state, modules, multi-env. |
| `chaos-engineer` | Hypothesis-driven failure injection, blast radius control. |
| `sre-engineer` | SLOs, error budgets, golden signals, postmortems. |
| `performance-testing` | Load, stress, spike, soak, volume testing. |

### Testing & quality

| Skill | What it covers |
|---|---|
| `test-driven-development` | Red → green → refactor, short loop. |
| `test-master` | Unit, integration, E2E, performance, security strategy. |
| `test-automation` | Framework choice, CI integration, flake handling. |
| `test-frameworks` | Jest, Vitest, pytest, JUnit, RSpec patterns. |
| `playwright-expert` | Role-based selectors, POM, trace viewer. |
| `systematic-testing` | Bottom-up validation for multi-layer architectures. |
| `quality-metrics` | Coverage, complexity, defect density, quality gates. |

### Debugging & security

| Skill | What it covers |
|---|---|
| `debugging-wizard` | Systematic root-cause work. Binary search, git bisect, three-fix threshold. |
| `systematic-debugging` | The iron law: no fixes without root cause. |
| `debug-logs` | Iterative `DEBUG()` logging: hypothesise, add logs, narrow, fix, clean up. |
| `trailofbits-static-analysis` | CodeQL + Semgrep + SARIF, merged and deduplicated. |
| `security-reviewer` | Audit code and infra, structured CVSS reports. |
| `secure-coding` / `secure-code-guardian` | OWASP Top 10, auth, parameterized queries, secrets. |
| `fullstack-guardian` | Security-focused full-stack implementation. |
| `reverse-engineer-anything` | Understand an unfamiliar system from observable behaviour. |

### Building & creative

| Skill | What it covers |
|---|---|
| `blender` | Modelling, sculpting, rigging, Grease Pencil, export pipelines. |
| `rigging` | Armatures, weight painting, IK/FK, deformation. |
| `texturing` | UV mapping, PBR materials, texture baking. |
| `asset-optimization` | Poly reduction, LODs, texture compression, draw calls. |
| `game-developer` | Unity/Unreal systems, ECS, physics, networking. |
| `godot` | Godot nodes, signals, resources, GDScript conventions. |
| `omniverse` | NVIDIA Omniverse, USD, Kit extensions. |

### Documents & content

| Skill | What it covers |
|---|---|
| `anthropics-pptx` | Create, edit, QA PowerPoint decks with real design rules. |
| `seo-best-practices` | On-page SEO, technical SEO, schema markup. |
| `prompt-engineer` | Design, optimize, evaluate LLM prompts. |
| `rag-architect` | Production RAG — chunking, embeddings, retrieval eval. |
| `firecrawl-build` | Wire Firecrawl into an app: scrape, search, interact. |

### Repo maintenance

| Skill | What it covers |
|---|---|
| `rea-analysis-optimization` | Baseline, find the bottleneck, measure before/after. |
| `rea-changelog-update` | Keep a changelog users can read. |
| `rea-ci-tests-audit` | Audit CI for gaps and waste. |
| `rea-tool-design` | Design tools people actually use. |

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

**Installing a subset is the sane default.** 100+ skills means 100+ descriptions to wade through. Copy what fits the project.

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

The `brainstorming`, `systematic-debugging`, and workflow skills draw on [obra/superpowers](https://github.com/obra/superpowers) (MIT).

Everything else is written for this repo.

---

## License

MIT — see [LICENSE](LICENSE).

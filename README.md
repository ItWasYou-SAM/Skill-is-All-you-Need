<p align="center">
    <img src="assets/readme/logo.svg" width="480" alt="Skill is All you Need — logo, showing the skill chip mark beside the wordmark"/>
</p>

<p align="center">
    <b>Expert skills for AI agents</b>
</p>

<p align="center">
    <a href="https://github.com/ItWasYou-SAM/Skill-is-All-you-Need">
        <img src="https://img.shields.io/github/last-commit/ItWasYou-SAM/Skill-is-All-you-Need.svg?style=flat&color=blue" alt="Last commit"/>
    </a>
    <a href="https://github.com/ItWasYou-SAM/Skill-is-All-you-Need/issues">
        <img src="https://img.shields.io/github/issues/ItWasYou-SAM/Skill-is-All-you-Need.svg?style=flat&color=success" alt="Issues"/>
    </a>
    <a href="https://github.com/ItWasYou-SAM/Skill-is-All-you-Need/stargazers">
        <img src="https://img.shields.io/github/stars/ItWasYou-SAM/Skill-is-All-you-Need?style=flat&color=blue" alt="Stars"/>
    </a>
    <a href="https://github.com/ItWasYou-SAM/Skill-is-All-you-Need/network/members">
        <img src="https://img.shields.io/github/forks/ItWasYou-SAM/Skill-is-All-you-Need?style=flat&color=success" alt="Forks"/>
    </a>
    <a href="LICENSE">
        <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="MIT licensed"/>
    </a>
</p>

Skill is All you Need is a curated library of **249 production-grade skills** that turn generic AI agents into domain experts — covering design, frontend engineering, video, quality, research and more.

![architecture](assets/readme/architecture.svg)

The key component of the library is a skill: a self-contained instruction folder with a `SKILL.md` that tells the agent what the skill does, when to activate, the process to run and the output format to return. Read the descriptions of installed skills and the agent decides which to use for each request — no slash commands, no configuration.

This foundation gives your agent expert checklists, taste and guardrails built from real usage instead of trial and error. Build polished frontends, review PRs, ship video and run deep research — all with deterministic quality, every run.

Summary of library features:

- 🧠 **249 skills across 13 domains** — from anti-slop UI design to OWASP-grade code review
- 🪄 **Auto-invoked** — skills load themselves from natural language, exactly when needed
- 🎯 **Deterministic quality** — explicit checklists and output formats instead of vibes
- 🛡️ **Production guardrails** — the mistakes real projects paid for, encoded and enforced
- 📄 **Markdown-native** — every skill is a readable, editable `SKILL.md`, no lock-in
- 🔌 **Works everywhere** — Claude Code, OpenCode, Cursor, Codex; copy skills anywhere
- 🔋 **Batteries included** — 500+ trigger phrases indexed in [COMMANDS.md](COMMANDS.md)
- 🧩 **Composable** — skills chain together, like `code-review` + `security-and-hardening`

Skill is All you Need is open-source under an MIT license, and is built on top of [Claude Code](https://claude.ai), [Agent Skills](https://github.com/anthropics/agent-skills), [Open Design](https://github.com/nexu-io/open-design), [HyperFrames](https://github.com/heygen/hyperframes), [fal.ai](https://fal.ai) and [GSAP](https://greensock.com).

> [!NOTE]
>
> Every skill here is a plain markdown instruction set — portable to any agent that supports the skills format. If a skill improves quality, reduces variance, encodes preferred structure or prevents repeat mistakes, it earns its place.

## Why skills?

![why](assets/readme/h-why.svg)

Agents re-learn taste and process in every session without structure. Why install a skill library?

![demo](assets/readme/value.svg)

- Installed in minutes — clone once, copy once:
```bash
git clone https://github.com/ItWasYou-SAM/Skill-is-All-you-Need.git
cp -r Skill-is-All-you-Need/* ~/.claude/skills/
```
- Auto-invoked from plain speech — the same request now triggers a checklist:
```
"Review this PR for security issues"
→ code-review + security-and-hardening
→ severity-ranked findings with fix suggestions
```
- Run local — plain markdown files, nothing leaves your machine
- Low footprint — install one category or one skill when you don't want it all
- Browse everything — [COMMANDS.md](COMMANDS.md) indexes every skill and trigger phrase

## Skill categories

The library is organized into 13 categories, from creative production to engineering rigor.

<div align="center">
  <img src="assets/readme/headliners.svg" alt="Six headliner skills with one-line pitches" width="100%"/>
</div>

### Build

Frontend, UI/UX and motion skills that push an agent's output from "generated" to "designed".

| Skill  | What it does  | Trigger |
|:------:|:--------------|--------:|
| `design-taste-frontend` | Anti-slop marketing sites, heroes and brand pages | "build a landing page" |
| `ui-ux-pro-max` | 50+ styles, 161 palettes, 99 UX guidelines across 10 stacks | "design this screen" |
| `gsap-*` | 8-module GSAP animation suite with scroll triggers | "animate this section" |

### Ship

Media production skills that go from prompt to finished asset.

<div align="center">
  <img src="assets/readme/workflow.svg" alt="A request auto-loads skills and returns structured output" width="100%"/>
</div>

| Skill  | What it does  | Trigger |
|:------:|:--------------|--------:|
| `hyperframes` | Complete video pipeline: script, storyboard, motion, render | "make a launch video" |
| `fal-generate` | Image generation across 12 fal.ai modules | "generate product images" |
| `ecommerce-image-workflow` | Studio product imagery: edit, upscale, try-on | "make my catalog" |

### Operate

Quality, workflow and research skills that keep output honest.

| Skill  | What it does  | Trigger |
|:------:|:--------------|--------:|
| `code-review` | Severity-ranked reviews with fix suggestions | "review this PR" |
| `security-and-hardening` | OWASP Top 10 and dependency traps, pre-flagged | "harden this service" |
| `deep-research` | Multi-agent, cited research reports | "research my competitor" |
| `bug-debugging` | Systematic root-cause debugging | "debug this failing test" |

## Installation

![install](assets/readme/h-install.svg)

The easiest way is clone and copy

```
git clone https://github.com/ItWasYou-SAM/Skill-is-All-you-Need.git
cp -r Skill-is-All-you-Need/* ~/.claude/skills/    # Claude Code
```

Also supported: `~/.agents/skills/` (OpenCode) and `.cursor/skills/` (Cursor). To cherry-pick categories or single skills:

```
cp -r Skill-is-All-you-Need/06-code-quality/* ~/.claude/skills/
```

## Skill guide

See the table below for recommended first installs. Every skill earns its place by improving quality, reducing variance or preventing mistakes.

| Domain                                                                     | Skill(s)                                                                 |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| [Design & Frontend](./01-ui-ux-design)                                     | [design-taste-frontend](./01-ui-ux-design), [ui-ux-pro-max](./01-ui-ux-design) |
| [Code Quality](./06-code-quality)                                          | [code-review](./06-code-quality), [bug-debugging](./06-code-quality)      |
| [Security](./07-development-workflow)                                      | [security-and-hardening](./07-development-workflow)                      |
| [Video](./04-video-production)                                             | [hyperframes](./04-video-production), [captions](./04-video-production)  |
| [Images](./05-image-media)                                                 | [fal-generate](./05-image-media), [fal-upscale](./05-image-media)        |
| [Research](./09-research-analysis)                                         | [deep-research](./09-research-analysis)                                  |
| [Agents](./08-agent-skills)                                                | [brainstorming](./08-agent-skills), [agent-evals](./08-agent-skills)     |
| [Docs](./10-document-content)                                              | [documentation-generator](./10-document-content)                         |
| [Workflow](./07-development-workflow)                                      | [spec-driven-development](./07-development-workflow), [ship](./07-development-workflow) |

Skills are plain folders on disk. Not sure where to start? Install `06-code-quality` first — quality skills pay for themselves on the first review.

## Powered by the community

Built on top of these open-source projects:

| Project  | What the library uses  |
|:------------ |:-------------|
| [Agent Skills](https://github.com/anthropics/agent-skills) | Base skill format and concept |
| [Open Design](https://github.com/nexu-io/open-design) | 157 design skills |
| [HyperFrames](https://github.com/heygen/hyperframes) | Video production pipeline |
| [fal.ai](https://fal.ai) | Image and media model hosting |
| [GSAP](https://greensock.com) | Animation modules |
| [Promptfoo](https://github.com/promptfoo) | LLM evaluation reference |
| [Superpowers](https://github.com/superpowers) | Development workflows |

## Further reading

![further](assets/readme/h-further.svg)

- [COMMANDS.md](COMMANDS.md) — every skill and trigger phrase in one file
- [Hero visual source](assets/readme/hero.svg) — the full library as a skill index
- [Workflow visual source](assets/readme/workflow.svg) — how auto-invoke works
- [Project README history](https://github.com/ItWasYou-SAM/Skill-is-All-you-Need/commits/)

## Contributing

For those who would like to contribute a skill, see the rubric below. One skill, one job — no knowledge dumps.

<details>
<summary>Skill rubric</summary>
<br>

- **Differentiation** — is this skill unique?
- **Reliability** — does it work consistently?
- **Specificity** — is it actionable, with triggers?
- **Operational value** — does it save time and effort?
- **Cost** — is it worth the tokens?

Template: `name` · *"Use this skill when…"* description · 3–5 step process · defined output format.

</details>

## License

This library is open-source under the [MIT license](LICENSE).

<p align="center">
  <a href="https://github.com/oil-oil/beautify-github-readme"><img src="assets/readme/signature.svg" width="300" alt="README made with beautify-github-readme" /></a>
</p>

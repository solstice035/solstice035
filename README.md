# Nick Solly

I lead enterprise technology programmes for banks, mostly in risk, compliance and controls. I've spent twelve years in capital markets technology consulting, currently as a Senior Manager, running engagements from scoping through to delivery. Before that I was a project manager on RBS's OTC clearing programme, and before that a British Army officer for five years, with service in Iraq and Afghanistan and latterly as a regimental signals officer.

Most of what's public here comes from one question: how much real work can agents do, and what does it take to run them properly? In my experience the model is rarely the hard part. The hard parts are the ones delivery people already know: a budget, a clear contract between stages, acceptance criteria, and someone accountable for what ships.

## Built by my agents

A lot of the code on this profile was written by agents I run, and the commit history says so. That's deliberate. The system is the thing I built.

### [the-foundry](https://github.com/solstice035/the-foundry)

An autonomous overnight build pipeline. A Claude Haiku scout reads developer pain points on Hacker News and Reddit, a Sonnet agent picks one and writes the spec, and aider driving Sonnet builds an MVP and pushes it before I'm up.

- One model per stage, priced to the job. The first end-to-end build cost $0.47.
- A JSON schema on every hand-off between agents
- Versioned prompts, acceptance criteria for every epic, and a validation gate before the nightly cron went live

I commissioned it, approved each phase and reviewed what it shipped. Between 18 February and 4 April 2026 it built 19 repos. Eight are public:

| Repo | What it does |
|:--|:--|
| [tool-lint](https://github.com/solstice035/tool-lint) | Lints MCP, OpenAI and Anthropic tool definitions |
| [deptox](https://github.com/solstice035/deptox) | Finds AI-hallucinated phantom npm packages in lockfiles |
| [vibe-check](https://github.com/solstice035/vibe-check) | Security scanner for AI-generated projects |
| [gh-prompt-shield](https://github.com/solstice035/gh-prompt-shield) | Scans GitHub issues and PRs for prompt injection aimed at AI coding tools |
| [agent-safe](https://github.com/solstice035/agent-safe) | Credential proxy for AI coding agents |
| [mcp-slim](https://github.com/solstice035/mcp-slim) | CLI proxy that cuts MCP token usage |
| [ctx-handoff](https://github.com/solstice035/ctx-handoff) | Packs a repo's context into a handoff document for AI assistants |
| [pdf-privacy-tools](https://github.com/solstice035/pdf-privacy-tools) | Browser-only PDF toolkit, and the Foundry's first build |

### [openclaw-agent-swarm](https://github.com/solstice035/openclaw-agent-swarm)

Spawns Claude Code agents into isolated git worktrees, each on its own branch in its own tmux session. Failed agents are retried, CI has to pass before a PR is marked ready, and anything running over an hour without a PR gets flagged.

### [jeeves-architecture](https://github.com/solstice035/jeeves-architecture)

An interactive map of the agent estate behind all of this: a hub agent, persistent specialists, on-demand workers and the Foundry.

## Built by me, with Claude Code

### [controls-clustering](https://github.com/solstice035/controls-clustering)

Groundwork for grouping financial controls by what they do rather than which organisation wrote them. It pulls different firms' control libraries into one schema, standardises their vocabulary against ISO 20022, FIBO and FATF, and starts stripping out each firm's fingerprints. It's a 2025 prototype: the clustering itself isn't built yet, and the README lists what doesn't work. This is the closest thing here to my day job.

## Elsewhere

[LinkedIn](https://www.linkedin.com/in/nicksolly)

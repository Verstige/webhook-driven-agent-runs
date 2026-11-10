# Webhook-Driven Agent Runs: Turn Events Into Work

> Turn an incoming event into work your agent actually does. Subscription lifecycle, signature verification, idempotent delivery and the retry behaviour that stops duplicate runs.

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg) ![Claude Code](https://img.shields.io/badge/Claude_Code-skill-blueviolet.svg) [![Available on Agensi](https://img.shields.io/badge/Agensi-%246.75-ff5a5f.svg)](https://agensi.io/skills/webhook-driven-agent-runs-turn-events-into-work)

## What it does

Trigger agent runs from webhooks: subscribe to events, verify the signature, and run an agent against each event.

Create dynamic webhook subscriptions so external services (GitHub, GitLab, Stripe, CI/CD, IoT sensors, monitoring tools) can trigger Hermes agent runs by POSTing events to a URL.

## The failure it prevents

Working this by hand means rediscovering the same edge cases every time. They are written down here instead, with the fix for each one.

## When to use it

- turn an incoming event into work your agent does
- verify a webhook signature before acting
- stop duplicate deliveries running the job twice

## What's inside

```
plugins/
└── webhook-driven-agent-runs/
    ├── .claude-plugin/plugin.json
    └── skills/webhook-driven-agent-runs/
        ├── SKILL.md
```

## Install

Add this repo as a Claude Code marketplace, then install the skill:

```bash
claude plugin marketplace add Verstige/webhook-driven-agent-runs
claude plugin install webhook-driven-agent-runs@webhook-driven-agent-runs
```

Or copy the skill straight into your skills directory:

```bash
git clone https://github.com/Verstige/webhook-driven-agent-runs.git
cp -R webhook-driven-agent-runs/plugins/webhook-driven-agent-runs/skills/webhook-driven-agent-runs ~/.claude/skills/
```

## Usage

The skill activates on the work it describes. Ask for the outcome, and it
supplies the method:

```
> "turn an incoming event into work your agent does"
```

## License

MIT. See [LICENSE](LICENSE).

---

**Also available as a paid skill on Agensi** — $6.75. Install it with one command, no clone required:

[agensi.io/skills/webhook-driven-agent-runs-turn-events-into-work](https://agensi.io/skills/webhook-driven-agent-runs-turn-events-into-work)

Part of the [Verstige](https://github.com/Verstige) skills portfolio. More at [github.com/Verstige](https://github.com/Verstige).

<h1 align="center">/whathappened</h1>

<p align="center">
  <a href="https://docs.x.ai/build/overview"
    ><img
      alt="Requires Grok Build"
      src="https://img.shields.io/badge/Grok%20Build-required-black?style=flat-square"
  /></a>
  <a href="https://github.com/1jehuang/jcode"
    ><img
      alt="Jcode grok-build"
      src="https://img.shields.io/badge/Jcode-grok--build-black?style=flat-square"
  /></a>
  <a href="https://agentskills.io"
    ><img
      alt="Agent Skills"
      src="https://img.shields.io/badge/Agent%20Skills-package-blue?style=flat-square"
  /></a>
  <a href="LICENSE"
    ><img
      alt="License"
      src="https://img.shields.io/badge/license-MIT-green?style=flat-square"
  /></a>
  <a href="https://x.com/kunchenguid"
    ><img
      alt="X"
      src="https://img.shields.io/badge/X-@kunchenguid-black?style=flat-square"
  /></a>
  <a href="https://discord.gg/Wsy2NpnZDu"
    ><img
      alt="Discord"
      src="https://img.shields.io/discord/1439901831038763092?style=flat-square&label=discord"
  /></a>
</p>

<h3 align="center">What just happened on X - and what is the room actually saying?</h3>

<p align="center"><strong>Requires Grok Build’s native X tools.</strong> Runs in <a href="https://docs.x.ai/build/overview">Grok Build</a> directly, or in <a href="https://github.com/1jehuang/jcode">Jcode</a> with <code>--provider grok-build</code>. Other agents and non-Grok providers can install the package, but cannot run the X queries.</p>

Something drops. A model ships. A founder posts. A product melts down.

You open X and get dunks, screenshots, quote-tweet chains, and three conflicting "official" takes - none of them in one place.

**whathappened** is an [Agent Skill](https://agentskills.io) for [Grok Build](https://docs.x.ai/build/overview) and [Jcode](https://github.com/1jehuang/jcode) (`--provider grok-build`) that turns that firehose into a short neutral briefing: what happened, where the conversation is, the opinion map, the live debates, and the receipts.

- **X-first** - public conversation from X, not a blog roundup. One optional web lookup only to resolve *who/what* the topic is.
- **Adaptive window** - breaking stories use minutes or hours; quieter ones widen only when the story is incomplete. Freshness wins by default.
- **Opinion map + debates** - camps, rough sample shares, steelman vs critique, with real post links - not a vibes paragraph.

## Quick Start

```sh
# install globally
$ npx skills add kunchenguid/whathappened -g
# or copy skills/whathappened → ~/.grok/skills/whathappened (Grok Build)
# or copy skills/whathappened → ~/.jcode/skills/whathappened (Jcode)

# in Grok Build
/whathappened Kimi K3

# in Jcode (requires Grok Build login + --provider grok-build)
$ jcode login --provider grok-build
$ jcode --provider grok-build
/whathappened Kimi K3
```

Example output from a real run on launch day (edited only for README length; structure is what the skill produces):

```markdown
# /whathappened: Kimi K3

**Window:** last ~24h · mode Same-day · as of 2026-07-16 ~22:30 UTC
**X sample:** ~60+ posts · Top + Latest + Semantic + first-party · 4 threads · confidence high (event) / medium-high (opinion; day-0)
**Entity resolve:** none (X user search → official @Kimi_Moonshot)

## What happened

Moonshot’s Kimi account launched Kimi K3 today as “Open Frontier Intelligence”: a 2.8T-parameter, 1M-context, native multimodal model for long-horizon agentic coding, live on Kimi product surfaces and API, with full weights promised by July 27, 2026.

The official thread also stresses architecture (Kimi Delta Attention, Attention Residuals, sparse MoE) and demos (kernel optimization, vision-in-the-loop game/UI work).

Independent and community scoreboards moved quickly: Arena Frontend Code Arena #1 (over Claude Fable 5), Text Arena roughly top-10, and Artificial Analysis Intelligence Index ~57 (near Opus 4.8 / GPT-5.5, behind Fable 5 and GPT-5.6 Sol).

## Where the conversation is

- Dominant frame: open weights (or soon-to-be) at near-frontier quality, especially coding/frontend - often cast as a milestone for open models.
- Secondary frames: API price/latency vs closed flagships; China vs US competitive pressure; policy/safety backlash expected next.
- Who is loud: Moonshot first-party; eval accounts (Arena, Artificial Analysis); coding-agent vendors (e.g. Cline); AI Twitter builders; a thinner but clear skeptic lane on cost/speed/real-work gaps.

## Public opinion map

Shares are rough qualitative judgment from this X sample, not polling.

| Camp | Share (rough) | Core claim | Representative voices |
|------|---------------|------------|------------------------|
| Open-frontier bulls | ~50% | Near Fable/Sol on many axes; #1 frontend; open weights change the game | @cline, @arena, @TheAhmadOsman |
| Nuanced practitioners | ~25% | Very strong (esp. frontend), not undefeated overall; slow / thinks hard / API not “cheap open” | @goodworse, @DimitriGilbert, @runzhuotao, @jaminball |
| Geopolitics / policy | ~15% | “Sputnik” for the US; fear of open-model bans; cycle of China/safety rhetoric | @MTSlive (quoting Amp CEO), @Dan_Jeffries1, @haider1 |
| Maximal hype | ~10% | AGI-adjacent language, “mogs everything” | e.g. @dedene |

## The live debates

1. **Is it frontier, or “almost frontier”?**
   Side A: same ballpark as GPT-5.6 / Fable 5, #1 frontend. Side B: AA puts it behind Fable/Sol overall; some real-workload tests put it nearer Opus 4.8 / GPT-5.5.

2. **Cheap open win vs expensive reasoning tax**
   Side A: $3/$15 per MTok framed as Sonnet-like value. Side B: “thinks a lot → costs a lot,” slower than hoped, pricier than prior Kimi models.

3. **Competition catalyst vs regulatory panic**
   Side A: healthy race, progress accelerates. Side B: expect essays, China-hawk policy, open-weight restrictions.

4. **“Open” today vs weights on July 27**
   API/product is live; weights are scheduled, not yet downloadable.

## Notable posts (receipts)

- @Kimi_Moonshot - origin: official launch specs + July 27 weights
- @arena - scoreboard: Frontend Code Arena #1 over Fable 5
- @ArtificialAnlys - independent eval: AA ~57; agentic gains; cost/task framing
- @cline - builder frame: largest open-weight class model, near Fable/GPT-5.6, Sonnet-like API price
- @synthwavedd - receipt: “drops at 57 on Artificial Analysis, just behind Fable and Sol”
- @goodworse - steelman critique: frontend strength vs real-world closer to Opus 4.8/GPT-5.5; slow; pricier than K2.7
- @DimitriGilbert - hands-on: “really good… only downside, it thinks a LOT… and therefore costs a LOT”
- @theo - ecosystem: practical “which harness?” question, not pure scoreboard talk

## Gaps / caveats

- Day-0 recency bias: likes and quotes still forming; Top lane is announcement-heavy.
- Weights not out yet: open-weight celebration is partly forward-looking (July 27).
- English/AI-Twitter skew; capacity/noise on Latest.
- What would change the read: multi-day coding failures, weights delayed, or closed labs shipping clear counters.
```

## Runtime requirement (Grok Build or Jcode `--provider grok-build`)

This skill is **not** a general-purpose web research product. It depends on Grok Build’s native X stack:

- `x_keyword_search`
- `x_semantic_search`
- `x_thread_fetch`
- `x_user_search`

Supported hosts:

- **Grok Build** directly.
- **Jcode** with `--provider grok-build` (Grok Build subscription via the authenticated Grok CLI ACP transport).

If those native X tools are missing in the active session, the skill **refuses** rather than faking an X briefing from web search. Installing into Claude Code, Cursor, Codex, or running Jcode on non-Grok providers (Claude, OpenAI, Gemini, or a plain `--provider xai` API key) will not give you a working run.

## Install

**Global (recommended)** via `npx skills`:

```sh
npx skills add kunchenguid/whathappened -g
```

**Project-local:**

```sh
npx skills add kunchenguid/whathappened
```

**Direct into Grok Build’s user skills dir:**

```sh
git clone https://github.com/kunchenguid/whathappened.git
mkdir -p ~/.grok/skills
cp -R whathappened/skills/whathappened ~/.grok/skills/whathappened
# or: ln -s "$(pwd)/whathappened/skills/whathappened" ~/.grok/skills/whathappened
```

**Direct into Jcode’s user skills dir:**

```sh
git clone https://github.com/kunchenguid/whathappened.git
mkdir -p ~/.jcode/skills
cp -R whathappened/skills/whathappened ~/.jcode/skills/whathappened
# or: ln -s "$(pwd)/whathappened/skills/whathappened" ~/.jcode/skills/whathappened
```

Both Grok Build and Jcode also discover skills under `.agents/skills/` (global `~/.agents/skills/` and project-local `.agents/skills/`), and Jcode also loads project-local `.jcode/skills/`. Prefer `~/.grok/skills/` or `~/.jcode/skills/` when you want the host-native path explicitly.

**Running in Jcode:**

```sh
# authenticate Grok Build in Jcode (uses the authenticated Grok CLI ACP transport)
jcode login --provider grok-build

# launch Jcode on the grok-build provider
jcode --provider grok-build
```

Then run `/whathappened <topic>` inside Jcode (or switch to `grok-build` in an existing interactive session with `/model`). Running `/whathappened` in Jcode on any non-`grok-build` provider will stop at the host check because Grok’s native X tools are not available.

**List skills in this package without installing:**

```sh
npx skills add kunchenguid/whathappened --list
```

## How It Works

```
topic
  │
  ▼
┌─────────────────┐
│ optional web x1 │  resolve entity only (name / handle)
└────────┬────────┘
         ▼
┌─────────────────┐
│ pulse (Latest)  │  measure velocity → commit window mode
└────────┬────────┘
         ▼
┌─────────────────┐
│ search lattice  │  Top · Latest · Semantic · from: · debate
└────────┬────────┘
         ▼
┌─────────────────┐
│ thread fetch    │  origin · official · camps · steelman
└────────┬────────┘
         ▼
┌─────────────────┐
│ rank + cluster  │  engagement × freshness × on-entity
└────────┬────────┘
         ▼
      briefing
```

- **Modes:** Breaking (hours) → Same-day → Story (days) → Background (longer only if needed) - shortest window that still explains the story.
- **Soft web rule:** at most one lookup for identity. Sentiment stays X-only.
- **No discovery mode in v1:** you must name a topic (`/whathappened` alone asks for one).

## Usage

| Invoke | Example |
| ------ | ------- |
| Slash | `/whathappened Kimi K3` |
| Natural language | "what are people on X saying about the OpenAI board drama" |

The agent should auto-invoke when the description matches (launch reaction, X/Twitter sentiment, "what happened with…").

## Package layout

```
skills/whathappened/
  SKILL.md                 # agent contract (pipeline + output template)
  references/
    query-patterns.md      # X advanced search recipes
    failure-modes.md       # thin sample, bots, entity collisions, …
```

Ships as an [`npx skills`](https://github.com/vercel-labs/skills) package (`skills/<name>/SKILL.md`) for install convenience. Runtime still requires Grok Build’s native X tools (Grok Build directly, or Jcode with `--provider grok-build`).

## Development

```sh
# edit the skill
$EDITOR skills/whathappened/SKILL.md

# smoke-test discovery locally
npx skills add ./ -l

# install from this checkout for Grok Build or Jcode
npx skills add ./ -g -y
# or symlink into ~/.grok/skills/whathappened or ~/.jcode/skills/whathappened
```

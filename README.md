# RunDrill Soft Skills for Engineers

Your personal **soft-skills coach** inside your AI agent — get better at the communication that
actually decides engineering careers: **asking the unblocking question**, **giving and taking
feedback**, **negotiating scope and estimates**, **writing async and across cultures**, **influencing
teams that don't report to you**, and **leading** in incidents, 1-on-1s, and mentoring. Short targeted
drills, an honest picture of where you are, and mistake memory that resurfaces what you got wrong. Your
level and progress live on the RunDrill MCP server (`mcp.rundrill.com`), synced across machines — not
in a local file.

**Why this course is different.** Communication has no compiler and **no single right wording** — what
matters is that *you* can say the hard thing clearly. When an AI will happily draft your Slack message,
your PR comment, your RFC, the real risk is that you never build the muscle. So this course makes you
**produce the communication yourself** and trains you to **review a flawed message** like you'd review
code — the **signature drill hands you a plausible, professional-looking message with a planted failure
mode** (it buries the answer, reads as a command across cultures, gives a date as a promise, says
"impossible" instead of a tradeoff) and asks you to find it, name it, and rewrite it — plus
**role-plays** the hard conversation, where the coach plays the tech lead, PM, or stakeholder and you
have to handle it live. The coach never writes it for you.

The course climbs seven rungs, junior → staff/lead — **Foundations** (asking good questions,
clarifying ambiguity, saying "I don't know", meeting participation) → **Feedback** (SBI, receiving
feedback in the moment, closing the loop) → **Communication** (Pyramid/answer-first, BLUF status
updates, technical→non-technical) → **Negotiation** (crucial conversations, trade-off framing, scope,
estimation language) → **Async & Global** (async context protocol, high/low-context, cross-cultural
feedback, CIS↔Western recalibration) → **Influence** (without authority, RFC/design docs, managing up,
org politics) → **Leadership** (incident communication, 1-on-1s, mentoring). It is grounded in
canonical sources — the Center for Creative Leadership's SBI model, Barbara Minto's *Pyramid
Principle*, *Crucial Conversations*, Erin Meyer's *The Culture Map*, *The Staff Engineer's Path*, *The
Manager's Path*, and Lara Hogan's *Resilient Management*.

**Learn in your language.** Engineering teams often work in English, but you don't have to study only
in English: set your native language and the coach explains in it, keeping any English team message in
English and giving each framework term as *native (English original)* — so you reason naturally and
still recognise the real terms on the job.

## One plugin, three hosts

The coaching skill (`skills/soft-skills-coach/SKILL.md`) and `.mcp.json` are shared; each host reads
its own manifest and ignores the rest.

| Host | Reads |
|---|---|
| Claude Code / Claude Desktop | `.claude-plugin/plugin.json` + `.mcp.json` |
| OpenAI Codex | `.codex-plugin/plugin.json` + `.mcp.json` |
| Google Antigravity | `plugin.json` + `mcp_config.json` (+ `rules/`) |

The MCP endpoint is `https://mcp.rundrill.com/skills/soft-skills` — the skills-course host, passing
`subject: "soft-skills"`. The server routes on the `/skills` segment and ignores the course name; the
name makes this register as its own MCP server in your agent. On first use the host opens a browser tab
for the OAuth handshake, then closes it — no API key to paste.

## Install

- **Claude Code / Desktop** — via the RunDrill marketplace:
  ```
  /plugin marketplace add rundrill/rundrill
  /plugin install rundrill-soft-skills@rundrill
  ```
  Then run `/soft-skills-coach`.
- **OpenAI Codex** — `codex plugin marketplace add rundrill/rundrill`, then install `rundrill-soft-skills`.
- **Google Antigravity** — drop this folder into `~/.gemini/config/plugins/rundrill-soft-skills/`
  (global) or `<workspace>/.agents/plugins/rundrill-soft-skills/` (workspace-scoped).

## License & attribution

© RunDrill. Licensed under **Creative Commons Attribution-NonCommercial-NoDerivatives 4.0
International (CC BY-NC-ND 4.0)** — full text in [LICENSE](LICENSE). You may view, run, and share this
plugin unchanged, non-commercially, with attribution; you may not use it commercially or publish
modified/derivative versions. For other licensing, contact **hello@rundrill.com**.

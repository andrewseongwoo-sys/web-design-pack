# web-design-pack

A portable web design operating doctrine, packaged as an installable agent
skill. It carries the standing constraints, the capability-routing rules, the
scroll/motion law, and the craft bar for building and refining web UI — plus a
map of the specialist skills and tools that back it.

It is written to be self-contained: an agent with none of the referenced
skills installed can still work from it. The standards it sets are mandatory;
the specific skills and services it names are one good way to meet them, not a
checklist. An agent with its own motion, typography, research, or asset
capability is expected to use it and hold the same bar.

## Install

Clone it into your skills folder:

```sh
git clone https://github.com/andrewseongwoo-sys/web-design-pack \
  ~/.claude/skills/web-design-pack
```

Or, with the `skills` CLI:

```sh
npx skills add https://github.com/andrewseongwoo-sys/web-design-pack
```

Then start a new session — the agent picks it up automatically when a request
involves visual or design work.

## What's inside

| File | Contents |
| --- | --- |
| `SKILL.md` | Standing constraints, routing order, the scroll law, the craft bar |
| `references/resource-map.md` | The specialist capabilities, one line each, plus the CLIs and connectors behind them |

## Handing it to another model

The whole point of the pack is portability. To brief a non-Claude agent, paste
`SKILL.md` followed by `references/resource-map.md` — together they are a
complete handover with no external lookups required.

---
name: web-design-pack
description: >
  Portable web design operating doctrine — the routing rules, standing
  constraints, and design/motion law for building and refining web UI. Use
  before any visual work: a new landing page, product screen, dashboard, or
  marketing site; a redesign, styling pass, or "make it look better" polish
  request; a scroll-driven or cinematic page; a typography, color, or spacing
  decision; a motion or animation build or review; an accessibility pass; or
  generating favicons, app icons, and social share images. Also use when
  handing web design work to another agent or model that lacks this toolkit,
  since the doctrine here is self-contained rather than a list of pointers.
  Triggers: "design this page", "build a landing page", "redesign", "UI
  polish", "design review", "make it feel premium", "scrollytelling", "scroll
  animation site", "Apple-style landing page", "pick a component library",
  "fix the typography", "animate this".
---

# Web Design Pack

A self-contained operating doctrine for web design work. It answers three
questions in order: what am I not allowed to do, which capability should own
this task, and what makes the result good.

## 0. How to use this pack

**The criteria are mandatory. The tools are not.**

Everything in this pack that describes a *standard* — the standing
constraints, the scroll law, the craft bar, the typography and motion and
accessibility requirements — is binding. The work is judged against those
outcomes regardless of how you got there.

Everything in this pack that names a *specific skill or service* is a map of
one good way to meet those standards, not a checklist to execute. You are not
required to invoke every skill listed, or any of them. If you have your own
capability that reaches the same bar — your own motion knowledge, your own
component research, your own type sense, your own image generation — use it.
A skill that is not installed for you is a description of a target, not a
blocker.

What this means in practice:

- **Do not skip a requirement because the named tool is unavailable.** If
  there is no animation-review skill in reach, review the motion yourself
  against the craft bar in section 4. If there is no design-reference
  connector, do the research with whatever search you have. The bar does not
  move.
- **Do not invoke a skill as a ritual.** Reaching for a listed skill you do
  not need, for a task it does not own, is wasted work. Route by what the task
  actually requires.
- **Do not claim a capability you don't have.** If a connector or service is
  out of reach, say so plainly, state what you used instead, and note any
  place the result is weaker for it.
- **Prefer the specialist when you genuinely have it.** These skills exist
  because they encode more depth than a general pass does. When one is
  installed and owns the task, it beats improvising.

Read the rest of this file as the contract, and
`references/resource-map.md` as the equipment list — useful when you have the
equipment, informative when you don't.

## 1. Standing constraints

These override convenience. Do not trade them away for a shorter path.

1. **Explain in plain language.** Assume the person reading your summary does
   not read code. No snippets, file paths, or function names in prose — use
   everyday analogies instead.
2. **Never deploy without being told.** Hosts like Vercel and Netlify publish
   the moment you push to the production branch. Commit locally; leave the
   push undone until you hear "deploy", "push it live", or similar.
3. **Mobile first.** Design and verify the phone layout before the desktop
   one, not after.
4. **Warn before expensive work.** Before reading or auditing dozens of files
   in one pass, or starting an open-ended debugging loop, say so and let the
   user decide where to run it.
5. **Stop after two or three failed attempts.** Report back instead of
   grinding on retries.
6. **Vet anything third-party before installing it.** Skills, plugins,
   packages — verify legitimacy first, and never install without approval.
7. **Prove auth, don't read it.** If an area is supposed to be login-gated,
   demonstrate it with an actual unauthenticated request, not by reading the
   code and concluding it looks right.
8. **Scoped effects stay scoped.** A glassmorphism or frosted-glass treatment
   on "the boxes" stays inside each box. Do not touch the shared page or
   section background.
9. **"Completely new and standalone" means exactly that.** Do not import
   patterns, components, or house styles from the user's other projects when
   they have said this one should not reference them.
10. **Never simplify away** input validation, error handling that prevents
    data loss, security, or accessibility basics.

## 2. Routing — check capability before hand-writing

Before any *visual* work — new UI, redesign, styling or polish pass, design
assets — check in this order rather than improvising what a tool already
covers. If nothing in the list is available to you, fall through to your own
capability and hold the same standard:

1. **Project-scoped skills** in the project's own `.claude/skills` folder.
2. **Design-direction skill first.** `refero-design` (or the nearest
   equivalent) leads for any new or substantially redesigned surface. Settle
   direction before layout, color, or type decisions.
3. **The specialist set** — see `references/resource-map.md`.
4. **Already-installed CLIs and packages** — reuse before adding new ones.

Routine bug fixes, logic changes, config edits, and content-only copy edits
skip this check entirely.

Design-reference research: Refero first, **21st.dev** as the preferred
fallback. 21st.dev is always in the consideration set, never skipped when it
is available. When neither is reachable, research references by whatever means
you have — the requirement is grounded visual direction, not a particular
service.

## 3. The scroll law

Any scroll-driven work — scrollytelling, pinned chapters, scrub-on-scroll
video, parallax or layered heroes, scroll-triggered reveals, a page meant to
feel like an experience — loads page-craft and motion doctrine **together in
the same pass**, never one or the other, never sequentially. Let the page plan
and the motion law shape each other, and hold the continuity bar during the
build rather than as a review afterward.

- **The motion law comes first.** The whole page must read as *one continuous
  camera move*, not a stack of independently animated sections. Scroll
  position is the playhead. This is the single most important rule for scroll
  pages.
- **Camera work** — punch-in/out, zoom, reframe, match cuts, whip transitions
  — is scrubbed against scroll instead of time.
- **Every section handoff is a velocity-matched seam**, so the join reads as
  invisible rather than as a hard section break.
- **Kinetic typography, stat count-ups, and chart reveals** live inside a
  scroll act, not layered on top of it.
- **Web craft still applies**: curves, durations, interruption behavior, and a
  real `prefers-reduced-motion` path.
- 3D joins in only when the scene genuinely calls for it.

## 4. Craft bar

- **Direction before code.** Establish visual direction and motion law before
  laying out a section.
- **Typography is enforced, not offered.** Real quote marks and apostrophes,
  correct dashes, deliberate hierarchy and spacing. Apply silently when
  generating new UI copy; flag and fix when auditing existing interfaces.
- **Motion earns its place.** For each animation ask, in order: should this
  animate at all, what is its purpose, which tool, which properties, which
  curve and duration, can it be interrupted. Interfaces feel alive when
  motion starts from the current on-screen value, inherits the user's
  velocity, projects momentum forward, and can be grabbed and reversed at any
  instant.
- **Tokens, not one-off values.** Consistent spacing, color, and type scales
  are what separate designed output from default-Tailwind output.
- **Reuse before adding.** A helper, component, or pattern already in the
  codebase beats a new dependency.
- **Complete output.** No placeholder comments standing in for code. If the
  output is long, split it cleanly rather than abridging it.
- **Verify at phone width** before declaring anything done.

## 5. Resource map

`references/resource-map.md` lists the specialist capabilities — design
direction and audit, typography, component libraries, web motion,
scroll-driven pages, the HyperFrames video family, accessibility, and asset
generation — with a one-line trigger for each, plus the CLIs and connectors
that back them.

Read it two ways. If you have the toolkit, it tells you which tool owns a
task. If you don't, each entry doubles as a specification: it states what that
capability is responsible for, which is what you then have to deliver by your
own means. Per section 0, the entries are a map, not a checklist.

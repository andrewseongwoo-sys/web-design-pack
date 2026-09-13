# Resource map

The specialist capabilities behind the doctrine in SKILL.md, with a one-line
trigger for each. Where a skill is installed locally it lives at
`~/.agents/skills/<name>/SKILL.md` or `~/.claude/skills/<name>/SKILL.md` —
read that file for full depth. Where it is not installed, the description
here is enough to know what to build or which equivalent to reach for.


### Design direction and audit
- **refero-design** — primary/default skill for new or substantially
  redesigned UI surfaces: product design, web design, landing pages,
  dashboards, product screens, design systems, anti-AI-slop work. Start here.
- **design-audit** — premium UI/UX audit and refinement. Systematic visual
  audit of an existing app producing a phased, implementation-ready design
  plan. Purely visual; touches no logic. Triggers: "design review", "make it
  look better", "UI polish", "visual refinement", "audit design".
- **apple-design** — Apple's approach to interface design: fluid, physical
  motion translated to the web. An interface feels alive when motion starts
  from the current on-screen value, inherits the user's velocity, projects
  momentum forward, and can be grabbed and reversed at any instant. Use for
  gesture-driven UI, spring animations, drag/swipe/sheet interactions.
- **emil-design-eng** — Emil Kowalski's philosophy on UI polish, component
  design, animation decisions, and the invisible details that make software
  feel great.
- **frontend-design-tokens** — use whenever building or styling any UI.
  Ensures consistent, polished, non-generic output instead of default
  Tailwind / AI-generated look.
- **prototype** — build multiple genuinely different versions of a UI piece,
  rendered behind a visual picker so the user flips through them live and
  promotes the one that feels right.

### Typography
- **ui-typography** — timeless typographic correctness that LLMs get wrong:
  proper quote marks, dashes, spacing, hierarchy, layout. ENFORCEMENT MODE:
  when generating new user-facing UI copy or layout, apply every rule silently
  — do not ask, do not explain. AUDIT MODE: when reviewing existing
  interfaces, flag violations and provide fixes.
- **font-recommendations** — curated typeface catalog with weights, licensing,
  and ready-to-use CSS. Sans: Inter, Roboto, Open Sans, Proxima Nova, Graphik,
  Futura, Lato, IBM Plex Sans. Serif: Merriweather, EB Garamond, Crimson Pro,
  Alegreya.

### Component and library choices
- **pick-ui-library** — curated, opinionated picks per frontend task: number
  and OTP inputs, charts, command menus, virtualization, drag-and-drop,
  toasts, state, styling.
- **ask-sonner** — the Sonner toast library: install, wire up the Toaster,
  pick the right `toast()` call, promise/loading toasts, updating, dismissing,
  styling.
- **vercel-react-best-practices** — React and Next.js performance guidelines
  from Vercel Engineering.
- **vercel-composition-patterns** — React composition patterns at scale; use
  when refactoring components with boolean-prop proliferation or building
  component APIs.

### Motion and animation (web)
- **animate** — build an animation from scratch, making the decisions in the
  order that determines whether it feels right: should this animate at all,
  what is its purpose, which tool, which properties, which curve and duration,
  can it be interrupted.
- **review-animations** — reviews animation code against a high craft bar.
  Defaults to flagging; approval is earned.
- **improve-animations** — surveys a codebase's motion as a senior motion
  advisor and produces a prioritized audit plus self-contained implementation
  plans. Read-only on source.
- **find-animation-opportunities** — finds places in a UI that don't animate
  but should, and rejects everything that shouldn't. Proposes exact values,
  does not implement.
- **animation-vocabulary** — reverse-lookup glossary turning a vague
  description into the exact term ("the bouncy thing when a popover opens" →
  Pop-in; "the iOS rubber-band scroll" → Rubber-banding).

### Scroll-driven pages
- **scroll-craft** — premium scroll-driven landing pages for service, product,
  food and drink brands. Plans the visitor journey, page grammar, emotional
  peak, and a bespoke signature move. Dimensional heroes with independent
  visual planes, restrained motion, and a separate mobile composition.
  Verifies desktop, mobile, and reduced-motion scroll states visually.
- **motion-doctrine** — the gateway; load FIRST. The high-level motion law
  that makes a multi-scene sequence feel like one continuous camera move.
- **cut-the-curve** — the technique catalog: five velocity-matched seams
  (zoom-through, inverse zoom-through, cut-the-curve, waterfall cut,
  rack-focus blur-cut) plus in-scene techniques like staggered arrival
  cascades.
- **seam-craft** — render-correctness doctrine for scene-to-scene seams; the
  prerequisites that make transitions composite correctly on a master
  timeline.
- **motion-graphics** — short design-led motion where the motion *is* the
  message: kinetic typography, stat count-ups, chart/data-viz hits, logo
  stings, lower-thirds, animated maps, animated headlines, UI animation.
- **web3d-integration-patterns** — Three.js, GSAP ScrollTrigger, React Three
  Fiber, Motion, and React Spring combined for complex 3D web experiences.
- **oversized-cursor** — house-style oversized macOS cursor technique for
  cursor-led / pointer-led scenes.

### Video and composition (HyperFrames family)
- **hyperframes** — mandatory entry point for any request to make, create,
  edit, animate, or render a video, animation, or motion graphic. Resumes
  project state, selects the owning workflow, routes domain capabilities.
- **hyperframes-core** — the composition contract: structure, `data-*` timing
  attributes, tracks, sub-compositions, variables, deterministic media.
- **hyperframes-keyframes** — punch-in/out, zoom, reframe, Ken Burns, camera
  moves, match/whip handoffs, seek-safe 2D/3D keyframes; GSAP, CSS keyframes,
  Anime.js, WAAPI, FLIP, paths, masks, SVG morph/draw, text trails, 3D depth.
- **hyperframes-animation** — all animation knowledge: atomic motion rules,
  multi-phase scene blueprints, scene transitions, and seven runtime adapters
  (GSAP default, plus Lottie, Three.js, and others).
- **hyperframes-creative** — non-animation creative direction: design spec
  handling, palettes, typography, narration, beat planning, audio-reactive
  visuals, brand style.
- **hyperframes-audio** — mixing audio already placed in a composition:
  fades, crossfades, gain, ducking, voiceover carve, EQ/compression/reverb,
  automation envelopes, submix buses.
- **hyperframes-cli** — the dev loop: init, add, catalog, capture, lint,
  check, snapshot, compare, preview, play, present, render, publish, cloud,
  doctor, upgrade. Also for diagnosing build and render failures.
- **hyperframes-registry** — install, discover, and wire registry blocks and
  components into compositions.
- **media-use** — the media OS: resolve BGM, SFX, images, icons, brand logos,
  voice, color grades and LUTs into frozen local file paths plus a ledger
  record.
- **figma** — import Figma content into a composition: rendered assets, brand
  tokens, components, storyboard sections reconstructed as motion.
- Supporting: **slideshow**, **captions-overlay**, **embedded-captions**,
  **general-video**, **changelog-video**, **pr-to-video**,
  **product-launch-video**, **faceless-explainer**, **music-to-video**,
  **talking-head-recut**, **remotion-to-hyperframes**.

### Accessibility
- **accessibility-audit** — whole-site WCAG 2.2 audit following WCAG-EM
  methodology: defines scope, samples representative pages and flows, runs the
  automated tier.
- **accessibility-scan** — one page, automated tier: run the a11y rule engine
  against a live page to find mechanically detectable violations.
- **accessibility-fix** — remediation only: repair violations to the WCAG 2.2
  baseline, edit, loop.
- **accessibility-diff** — regression check: diff a live page's violations
  against a baseline, by default comparing uncommitted changes.
- **accessibility-inspect** — hands-on screen-reader inspection of one screen.

### Assets
- **web-asset-generator** — favicons, app icons (PWA), and Open Graph / social
  meta images for Facebook, X, WhatsApp, LinkedIn, generated from logos or
  text slogans.

### Output discipline
- **full-output-enforcement** — enforces complete code generation, bans
  placeholder patterns like "// rest of the code here", handles token-limit
  splits cleanly. Apply to any task needing exhaustive, unabridged output.

## Tools

**Command line** — check what is actually installed before assuming:
- `vercel` — Vercel CLI. Remember constraint 2: never deploy unprompted.
- `21st` — the 21st.dev CLI for component search and registry work.
- `codegraph explore "<symbols or question>"` — in any repo with a
  `.codegraph/` folder, answers code-location questions in one call instead
  of a grep-and-read loop.

**Connector / MCP based.** If the running agent does not have these, say so
plainly and fall back to what it does have — do not pretend to have used
them:
- **Refero** — design reference search: screens, flows, styles, similar
  screens. The primary visual research source.
- **21st.dev** — component search, logo search, inspiration, themes,
  templates, registry publishing. The preferred fallback to Refero.
- **Fonts** — font recommendation service driven by natural-language briefs.
- **Canva** — design generation, editing, export, brand kits, templates.
- **Higgsfield** — image, video, audio, and 3D generation; website builder.
- **Chrome control / Chrome DevTools** — live page navigation, clicking,
  screenshots, console and network reading, Lighthouse audits, performance
  traces, device emulation.
- **Vercel** — projects, deployments, build logs, runtime errors, analytics,
  domains, deployment protection.


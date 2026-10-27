# designlang

A Claude plugin that bundles the `designlang` slash commands and the
`extract-design` skill. Point it at a public URL and it extracts that site's
design language — palette, typography, spacing, shadows, motion and component
patterns — then turns it into W3C DTCG tokens, Tailwind/shadcn themes, Figma
variables, graded report cards, remixes and brand-guideline books. The
commands wrap the `designlang` CLI (`npx designlang <url>`): in Claude Code and
Cowork they run locally, while in claude.ai chat they load as skills and
guidance. The plugin only reads the public pages you ask about and writes
output files locally; it sends no data to any third-party service.

## Install from a marketplace

In claude.ai (web or desktop): **Customize → Plugins → Add → Add marketplace →
Add from a repository**, then enter `osa822630-droid/design-extract` (the
repository URL works too). Add the `designlang` plugin from that marketplace.

In Claude Code: `/plugin marketplace add osa822630-droid/design-extract`, then
`/plugin install designlang@designlang`.

This folder is the plugin source referenced by
[`../../.claude-plugin/marketplace.json`](../../.claude-plugin/marketplace.json).
It intentionally contains only the manifest, `commands/`, `skills/`, README and
LICENSE: a top-level `bin/` directory makes claude.ai and Cowork refuse to
install a plugin, so the CLI and the rest of the repository stay outside it.

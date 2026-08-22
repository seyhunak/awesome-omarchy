# Contributing to Awesome Omarchy

Thanks for helping keep this guide useful. Corrections and removals are as welcome as additions — a curated list rots quietly, and your fix is a high-value contribution.

## What belongs here

This list is **production-first** and **hands-on**. An entry should be something an Omarchy user would realistically install, configure, theme, or study to make their Arch + Hyprland desktop better.

**Accepted:**

- Actively maintained Omarchy themes (naming `omarchy-<name>-theme`, with `colors.toml` + `preview.png` + `backgrounds/`)
- Quickshell plugins with `manifest.json` (`schemaVersion:1`, `id`, `kinds`, `entryPoints`) and at least one working kind (`bar-widget`, `bar`, `panel`, `service`, etc.)
- Hyprland/Omarchy dotfiles and hardware recipes that are daily-driven (note hardware + Omarchy version)
- Shell tools, TUIs, GUI apps, and fonts that integrate cleanly with Omarchy's theme pipeline
- Substantive learning resources: manuals, deep-dives, hardware guides, video walkthroughs
- Fixes to primers, keybindings, CLI groups, or architecture tables where facts have shifted (e.g., v4 Quattro changes)

**Not accepted:**

- Abandoned themes/plugins (no meaningful activity in ~12 months, or archived)
- Thin forks that add no distinct palette, widget, or hardware support
- Marketing pages, waitlists, and unreleased hardware preorders
- Paid-only themes without a free preview or install path
- Duplicate entries already listed under another section

## Entry checklist

Before opening a pull request, confirm your entry:

1. **Is daily-driver relevant** — something a real Omarchy user on Framework / Dell / Beelink would use or study
2. **Is actively maintained** — recent commits, releases, or doc updates (or a stable theme with a clear palette)
3. **Is not already listed** — search the README (`Cmd+F` / `Ctrl+F`) first
4. **Uses the canonical link** — the GitHub repo or official docs, never an aggregator, redirect, or referral link
5. **Follows the table format** of the section you're adding to (same columns, same badge legend)
6. **Has a one-line, non-marketing description** — say what it does and which palette/hardware it targets
7. **Sits in the most specific applicable section** — don't add a new top-level section for a single theme variant

## Format

Every section uses Markdown tables. Match the columns of the section you are editing exactly.

```markdown
| [Omarchy Ash](https://github.com/bjarneo/omarchy-ash-theme) | minimal ash · `omarchy-theme-install https://github.com/bjarneo/omarchy-ash-theme.git` |
```

**Badge legend** (apply only where genuinely true):

| Badge | Meaning |
|---|---|
| ⭐ | Widely adopted default for its category |
| 🔓 | Open source |
| 💰 | Commercial / paid tier required |
| ☁️ | Managed / hosted service |
| 🆓 | Free to use |

Use ⭐ sparingly — it means "if you don't have an opinion, pick this one." Roughly one to three per section.

### Description style

- One line, no trailing period for fragments
- Describe capability + palette/hardware: "OLED inky black · `omarchy-theme-install …`" beats "amazing and beautiful"
- For themes, include the install one-liner where the pattern is `omarchy-theme-install <git-url>`
- For plugins, name the `kinds` it provides (`bar-widget`, `service`)
- Avoid copying the upstream tagline verbatim if it's pure marketing

## Ordering

Within a section, tables are ordered roughly by adoption / stars / relevance rather than alphabetically — put your entry where a reader would expect to find it, not automatically at the end. Community theme tables favor higher-star, better-documented entries near the top.

## Submitting

```bash
git clone https://github.com/<your-username>/awesome-omarchy.git
cd awesome-omarchy
git checkout -b add-my-theme
# edit README.md
git commit -am "Add <Theme> to Community Themes"
git push origin add-my-theme
```

### Automated checks

Every pull request runs a [lychee](https://github.com/lycheeverse/lychee) link check over the Markdown. If it fails, your link is unreachable — fix the URL rather than working around the check.

To run it before pushing:

```bash
# macOS
brew install lychee
# or: cargo install lychee

lychee --config lychee.toml --no-progress .
```

A handful of hosts (X/Twitter, LinkedIn, iso.org, salesforce.com, oracle.com, bloomberg.com, api.star-history.com, shields.io) block automated traffic and are listed in `.lycheeignore`. Add to that file only when a link genuinely works in a browser but cannot be verified by a bot — never to hide a dead link.

Then open a pull request. In the description, include:

- A link to the theme/plugin/dotfiles
- A preview screenshot URL or path to `preview.png` (for visual changes)
- One or two sentences on why it belongs here (palette, hardware, or daily use)
- Any disclosure of affiliation (see below)
- For hardware notes: the machine, Omarchy version, Wi-Fi/BT/suspend result

**One entry per pull request** where practical — it keeps review fast.

## Self-promotion and affiliation

You may submit your own theme or plugin. **Disclose the affiliation in the pull request.** Self-submitted entries are held to the same bar as everything else, and "actively maintained" is checked more carefully for repos with few external users.

## Reporting problems

[Open an issue](https://github.com/seyhunak/awesome-omarchy/issues/new) for:

- Dead or redirected links (theme repo moved, `omarchy-theme-install` URL changed)
- Themes that have been archived or no longer install via `omarchy-theme-install`
- Descriptions that are no longer accurate (palette changed, hardware note stale)
- A ⭐ that no longer reflects reality (e.g., default terminal switched Foot ↔ Alacritty)
- Keybindings, CLI groups, or install steps that are outdated for v4 Quattro vs v3.8.x

These are high-value contributions.

## Code of Conduct

Participation is governed by the [Code of Conduct](CODE_OF_CONDUCT.md).

## License

By contributing, you agree that your contributions are licensed under the [MIT License](LICENSE).

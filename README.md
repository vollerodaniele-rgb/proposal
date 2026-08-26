# Proposals

One repo, one proposal per folder, served from
`proposal.noiraunoir.com/<slug>/`. The root and any unknown address show
only the studio name, and every page is noindexed, so the domain gives
nothing away.

Addresses are deliberately unguessable rather than readable: a proposal
carries prices, and often a discount meant for one client only.

## How it is built

- `assets/styles.css` and `assets/proposal.js` are the only copies.
- `data/<slug>.json` holds one proposal: client, intro, packages,
  notes, process and terms.
- `<slug>/index.html` is copied verbatim from `_template/`. It is the
  same file for every proposal; the page reads which one it is from the
  folder in the URL.

## Choosing a package

Each package has a Choose button. It opens a small form asking for a
name and an optional note rather than firing on a single tap. Sending
posts to the relay, which files it as an issue labeled `accepted` and
`proposal:<slug>`, and pings Telegram with which package was chosen.

For that to work the relay's token needs this repo, and
`proposal.noiraunoir.com` has to be in the relay's allowed origins.

## Style

House style: pitch black, plain white, no colour. The recommended
package is marked with a brighter border and a filled button rather
than an accent colour. Printing inverts to black on white and hides
the buttons.

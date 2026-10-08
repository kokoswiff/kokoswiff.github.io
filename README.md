# tenflux.fr — the public site of TENFLUX

The public web presence for **TENFLUX**, served by GitHub Pages from the root of this user
site and published on the product's own domain, **`tenflux.fr`** (`CNAME`).

**Nothing in this repository is part of the game.** No source, no internal report, no key,
no build artefact. The application lives in a separate, private repository and stays there.

## Why the domain, and why it still has to be a user site

**The domain** (bought and wired to GitHub Pages in October 2026) is not cosmetic. The
pages served here are the product's legal documents — the privacy policy names the data
controller and the GDPR contact — and they were previously served from a URL that spelled
out the owner's personal GitHub account. A player reading the privacy policy could reach a
real name in two clicks. Every address on these pages is now the product's own.

**The user site** is what `app-ads.txt` requires. AdMob's verifier takes the **hostname**
from the developer website on the Play listing and **ignores the path**: it fetches
`https://<host>/app-ads.txt` and nowhere else. A project page would serve the file under a
repository path, which the crawler never looks at — and the failure is silent, so it would
simply never verify. A user site serves from the root, and the custom domain keeps that
property: `https://tenflux.fr/app-ads.txt` is the root of the host.

## Pages

| Path | What |
|---|---|
| `/` | Landing page |
| `/privacy/` | Politique de confidentialité (FR) |
| `/privacy/en/` | Privacy policy (EN) |
| `/support/` | Support and contact |
| `/delete-account/` | Data deletion procedure |
| `/app-ads.txt` | The one AdMob authorisation line, at the root |

## What is deliberately absent

* **Legal notices (`/legal/`)** — written, and **deliberately not in this repository**.
  The page needs the publisher's legal identity, address and registration; those are the
  owner's to decide, and a placeholder on a public legal page is worse than no page. The
  draft and its checklist live in the private repository (`docs/c21/`) until the fields are
  real, so nothing unpublished can be pushed here by accident.
* **Any tracker, analytics, cookie or third-party request.** The privacy policy hosted here
  says TENFLUX does not track anyone; a page pulling a font from someone else's CDN would
  hand the visitor's IP to a third party while saying otherwise. The one webfont is served
  from this origin, and its SIL Open Font License sits beside it in `assets/OFL.txt`.
* **A "Get it on Google Play" badge** — the app is not published publicly yet. A badge
  pointing nowhere is a false promise, and Google's own brand rules forbid it for an
  unpublished app.

## Contact

Three addresses, all on the domain, all routed to one mailbox:

| Address | For |
|---|---|
| `support@tenflux.fr` | players — the store listing and `/support/` |
| `privacy@tenflux.fr` | privacy, GDPR rights, deletion, abuse reports |
| `contact@tenflux.fr` | publisher and legal — for `/legal/`, once it exists |

The in-app report action (a player flagging an abusive pseudonym) also writes to
`privacy@tenflux.fr`.

# kokoswiff.github.io — TENFLUX

The public web presence for **TENFLUX**, served by GitHub Pages from the root of this
user site.

**Nothing in this repository is part of the game.** No source, no internal report, no key,
no build artefact. The application lives in a separate, private repository and stays there.

## Why a user site and not a project page

`app-ads.txt` decided it. AdMob's verifier takes the **hostname** from the developer
website on the Play listing and **ignores the path**: it fetches
`https://<host>/app-ads.txt` and nowhere else. A project page would serve
`kokoswiff.github.io/<repo>/app-ads.txt`, which the crawler would never look at — and the
failure is silent, so it would simply never verify.

A user site serves from the root. `github.io` is on the Public Suffix List, so
`kokoswiff.github.io` counts as its own registrable domain rather than a subdomain of
something we do not own.

## Pages

| Path | What |
|---|---|
| `/` | Landing page |
| `/privacy/` | Politique de confidentialité (FR) |
| `/privacy/en/` | Privacy policy (EN) |
| `/support/` | Support and contact |
| `/delete-account/` | Data deletion procedure |

## What is deliberately absent

* **`app-ads.txt`** — not published yet. The line must be copied verbatim from the AdMob
  console; an invented or placeholder line does not fail loudly, it fails **silently**, so
  the file is absent until the real value exists.
* **Any tracker, analytics, cookie or third-party request.** The privacy policy hosted here
  says TENFLUX does not track anyone; a page pulling a font from someone else's CDN would
  hand the visitor's IP to a third party while saying otherwise. The one webfont is served
  from this origin, and its SIL Open Font License sits beside it in `assets/OFL.txt`.
* **A "Get it on Google Play" badge** — the app is not published. A badge pointing nowhere
  is a false promise, and Google's own brand rules forbid it for an unpublished app.

## Contact

`swiffswiffer@gmail.com` — temporary, replaceable. It appears in the four HTML pages and in
this file; nothing depends on it structurally.

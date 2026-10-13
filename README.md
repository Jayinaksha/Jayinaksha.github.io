# jayinaksha.github.io

The front door for every project site by Jayinaksha Vyas, plus the two projects whose
source is private and so cannot publish a Pages site of their own.

| Path | What it is | Where it comes from |
| --- | --- | --- |
| `/` | The index of every project site, each with real footage | this repo |
| `/slate/` | Slate — the narrated demo with chapters, and how a document gets written | this repo |
| `/newsroom/` | Newsroom — the publishing ladder, live, ported line for line from `verify_claims.py` | this repo |
| `/portfolio/` | The portfolio | `Jayinaksha/portfolio` |
| `/Robocon-25_codes/`, `/agentic-bot/`, `/zerotouch/`, `/iron-overview/`, `/telenotes/` | Project sites | each project's own repo |

GitHub Pages serves this repo at the root of the host, and every other repo's Pages site
under its own path — so `robots.txt` and `sitemap.xml` here are the ones crawlers read for
the whole host. The sitemap lists every project site; `robots.txt` also points at the
portfolio's own sitemap.

If a repo named `slate` or `newsroom` ever turns on Pages, it will claim that path and
shadow the page here.

## Design

Every site uses **Plate**, the shared design system. `assets/plate/` is a vendored copy;
the source of truth is `design-system/` in the portfolio repo. Footage in `assets/media/`
is short muted loops cut from real recordings, each with a poster frame.

No build step: serve the directory with `python3 -m http.server`.

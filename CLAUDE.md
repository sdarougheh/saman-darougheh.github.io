# samandarougheh.com

Personal academic site. Jekyll, deployed via GitHub Pages from `git@github.com:sdarougheh/saman-darougheh.github.io.git` (branch `main`). `CNAME` → `www.samandarougheh.com`.

## Checkouts on this machine

- `~/Repositories/samandarougheh` — this one, cloned 2026-08-16. Use it.
- `~/Dropbox/public/site/resume-template` — older checkout of the same repo, behind `main` and with uncommitted work (`crosswalk_dk_us.md` staged but never committed, plus untracked PyCharm `.idea/` files). Don't edit here; reconcile or retire it.
- `~/Dropbox/public/site/backup` — third checkout, untouched since May 2024.
- `~/Dropbox/public/site/{online-cv,minimal-mistakes,myblog}` — upstream templates, not the live site.

## Build

`bundle install` is required on a fresh clone: the Gemfile pulls `jekyll-pdf` from a git source, and without it `bundle exec jekyll` dies with `Bundler::GitError`.

```
bundle exec jekyll build
bundle exec jekyll serve --host 127.0.0.1 --port 4000 --livereload
```

## Content structure

All papers live in `_data/*.yml`; `index.html` renders each list through `_includes/publications_meat.html`. Nothing is written in HTML by hand.

- `publications.yml` — published. Uses `linkname`/`link` (top-level) for the journal citation, which renders in the `<h4>` next to the title.
- `workingpapers.yml`, `workinprogress.yml`, `policy.yml` — unpublished. Use a `links:` list instead.

Per-paper fields: `title`, `authors` (raw HTML `<a>` tags), `conference` (comma-separated string), `images` (`link` + `caption`, files in `images/`), `summary` (block scalar), `links`.

**A `links` entry with no `url` renders as plain text** in the same bullet-separated row. That's the idiom for a non-link annotation — journal status is written this way, e.g.:

```yaml
links:
  - url: https://sdaro.s3.eu-central-1.amazonaws.com/public/real_wages/draft.pdf
    desc: draft
  - desc: R&amp;R (The Review of Economics and Statistics)
```

Escape `&` as `&amp;` in `desc` — the template interpolates it into HTML unescaped.

Drafts are hosted on S3 under `https://sdaro.s3.eu-central-1.amazonaws.com/public/<project>/`.

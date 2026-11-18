# CLAUDE.md

Personal academic website for Lena Wiśniewska, built on the [al-folio](https://github.com/alshedivat/al-folio) v1 Jekyll starter.
Theme runtime (layouts, includes, CSS) lives in versioned `al_*` gems pinned in `Gemfile`; this repo only holds config and content.
Theme internals: see `docs/ARCHITECTURE.md` and `docs/BOUNDARIES.md`.

## Where things live

- `_config.yml` — site name, URL (`https://lenawisniewska.github.io`, `baseurl` blank), feature flags
- `_pages/about.md` — homepage (intro paragraphs, profile photo settings)
- `_pages/research.md` — research tab (paper/slides links; commented-out placeholders for files not yet added)
- `_projects/*.md` — one page per ongoing project (`/projects/<name>/`), rendered by the local `_layouts/project.liquid` (key figure + key points + research design). Copy `_projects/TEMPLATE.md` (unpublished) for new ones; figures go in `assets/img/projects/`.
- `_pages/cv.html` — CV tab: instant redirect to `assets/pdf/Wisniewska_CV.pdf` (replace that file to update the CV)
- Photography tab: parked on the `photography-draft` branch (not on main). Restore with `git checkout photography-draft -- _pages/photography.md _data/fieldwork.yml assets/img/fieldwork` plus the `.photo-grid` styles from that branch's `_sass/_custom.scss`.
- Contact links: text line under the photo, set in `profile.more_info` in `_pages/about.md` (`_data/socials.yml` icons are turned off)
- `assets/img/prof_pic.jpg` — profile photo
- Styling: `assets/css/main.scss` (local override of the gem's file; sets the navy accent color) + `_sass/_custom.scss` (serif font, icon size). Font is loaded via `third_party_libraries.google_fonts` in `_config.yml`.

## Local dev

Requires Homebrew Ruby (system Ruby 2.6 is too old) and a UTF-8 locale (the `ś` in the name breaks the build otherwise):

```bash
export PATH=/opt/homebrew/opt/ruby/bin:$PATH LANG=en_US.UTF-8 LC_ALL=en_US.UTF-8
bundle install            # gems go to vendor/bundle (gitignored)
bundle exec jekyll serve  # http://localhost:4000/
```

`convert: command not found` warnings are harmless locally (ImageMagick responsive images; CI installs it).

## Deploy

Pushing to `main` runs `.github/workflows/deploy.yml`, which builds the site and pushes `_site` to the `gh-pages` branch.
GitHub Pages must be pointed at `gh-pages` (Settings → Pages) for the site to go live.

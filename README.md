# Chen Shao — Personal Website

A single-page academic website built with [Jekyll](https://jekyllrb.com/), based on
[Martin Saveski's template](https://github.com/msaveski/www_personal).

## Editing content

All content lives in `_data/` — edit these, not the HTML:

- `_data/main_info.yaml` — name, title, email, social links, profile picture
- `_data/publications.yaml` — papers (`selected: y` shows them under the "Selected" tab)
- `_data/projects.yaml` — project cards (each links to a page in `_projects/`)
- `_data/experience.yaml` — the CV timeline (`category: work` = left, `school` = right)

Project detail pages are Markdown files in `_projects/`.
Images live in `assets/` (profile picture, project thumbnails, and `assets/cv/cv.pdf`).

### Still to personalize

- Replace the `"#"` placeholders in `_data/main_info.yaml` (LinkedIn, Google Scholar).
- Swap the placeholder SVGs in `assets/profile-pics/` and `assets/projects/*/` for real images.
- Add your compiled CV as `assets/cv/cv.pdf` (currently linked from the Vitæ section).
- Set a Google Analytics ID in `main_info.yaml` if you want tracking (optional).

## Running locally

Requires a modern Ruby (system Ruby on macOS is too old to build Jekyll).

```bash
brew install ruby          # or use rbenv / asdf
gem install bundler
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## Deploying to GitHub Pages

- **User site:** push to a repo named `<username>.github.io` on the `main` branch.
  Keep `baseurl: ""` in `_config.yml`.
- **Project site:** push to any repo, enable Pages in Settings, and set
  `baseurl: "/<repo-name>"` in `_config.yml`.

GitHub Pages builds the site automatically on every push.

## Credits

Template by [Martin Saveski](https://github.com/msaveski/www_personal).
CSS: [Skeleton](http://getskeleton.com/), [Font Awesome](https://fontawesome.io/),
[Academicons](https://jpswalsh.github.io/academicons/).

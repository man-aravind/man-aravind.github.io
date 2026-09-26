# Manaoj Aravind’s website

This site uses al-folio v1. Personal content lives in `_pages/`, `_news/`, `_bibliography/papers.bib`, `_data/socials.yml`, and `assets/`.

To update a publication, edit `_bibliography/papers.bib`. Its `pdf` field names a file in `assets/pdf/`; `selected = {true}` displays it on the homepage. To update the CV, replace `assets/pdf/CV.pdf`. To update teaching or research, edit the corresponding Markdown page. The homepage is `_pages/about.md`.

Preview locally with `docker compose up`, or open a pull request and inspect the build check. Deployment runs from `master` after merge. Theme internals remain in pinned gems in `Gemfile`; avoid copying layouts or merging the al-folio upstream repository into this one.

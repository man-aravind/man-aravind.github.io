# Maintaining Manaoj Aravind's website

Live site: https://man-aravind.github.io

This is a **Jekyll static website using al-folio v1**. You can still edit its Markdown files in VS Code. Your content is in this repository; the theme's layouts and styles come from versioned Ruby packages listed in `Gemfile` and resolved in `Gemfile.lock`.

## Where to edit

| Change | File or folder |
| --- | --- |
| Homepage introduction and background | `_pages/about.md` |
| Research stories and methods | `_pages/research.md` |
| Teaching and mentoring | `_pages/teaching.md` |
| Online CV and PDF download link | `_pages/cv.md` |
| Publication records | `_bibliography/papers.bib` |
| Publication page settings | `_pages/publications.md` |
| Email, scholarly profiles, social links and CV icon | `_data/socials.yml` |
| News items | `_news/` |
| Portrait and future research images | `assets/img/` |
| CV and paper PDFs | `assets/pdf/` |
| Site-wide settings and navigation features | `_config.yml` |

The block between `---` lines at the top of each page is YAML metadata: its layout, title, URL and navigation order. Write normal Markdown below it. Preserve the metadata unless you mean to change page behaviour. The homepage has additional switches for news and selected papers.

## Everyday editing in VS Code

1. Open your local clone of `man-aravind/man-aravind.github.io`.
2. Check that your existing work is committed or safely stashed, switch to `master`, and pull the latest changes. Your old local checkout needs this pull to receive the migration.
3. Edit the appropriate Markdown, BibTeX or YAML file and save.
4. Review the changes in VS Code's Source Control view, commit with a descriptive message, and push to GitHub.
5. Open the repository's **Actions** tab and check **Deploy site**. A push to `master` builds the site and publishes generated files to `gh-pages`; GitHub Pages serves those files.
6. Check the live page after deployment. The site will not change if the build fails: inspect the failed Actions step before trying again.

For larger changes, use a branch and pull request. The deployment workflow builds pull requests to check them, but does not publish them or create an automatic visual preview URL. Merge after reviewing the content and passing build.

You can also make a small text edit using GitHub's file editor. No local Ruby installation is needed when GitHub builds the site.

## Preview locally (optional)

With Docker and Docker Compose installed and running, run from the repository root:

```sh
docker compose up
```

Wait for Jekyll to finish building, then open http://localhost:8080. Most content changes rebuild while it runs. Stop with Ctrl+C. The first run downloads an image and may install dependencies. This repository includes the configuration, but local Docker preview was not tested in the migration environment, where Docker is unavailable.

The alternative is a native Ruby/Bundler setup following `docs/INSTALL.md`. GitHub's deployment uses Ruby 3.3.5, Node 20, Python 3.13 and ImageMagick; changing those is not part of ordinary content editing.

## Add a publication

Add a BibTeX entry to `_bibliography/papers.bib` with a unique key, correct authors, title, journal, year and DOI. The publications page is generated from this file. Optional fields include:

- `selected = {true}` to include the paper on the homepage.
- `pdf = {filename.pdf}` for a file in `assets/pdf/`.
- `html = {https://doi.org/...}` for the publisher link.
- `code = {https://github.com/...}` for an actual project repository.
- `bibtex_show = {true}` to expose its citation.

Copy an existing entry as a starting point and check comma/bracket syntax. Do not add a second entry for an existing paper. The online publication list and the downloadable CV are maintained separately.

## Update the downloadable CV

1. Open the new PDF itself and confirm the contents and dates.
2. Add it to `assets/pdf/` under a new descriptive filename, for example `Manaoj_Aravind_CV_October_2026.pdf`. A different filename avoids old browser-cached downloads.
3. Update both `_pages/cv.md` and the `cv_pdf` entry in `_data/socials.yml`, including the visible date.
4. Update the online CV text separately where needed.
5. After deploying, download through the live site's link and open the PDF to verify it.

Current download: `assets/pdf/Manaoj_Aravind_CV_September_2026.pdf`. It is the original supplied PDF, not generated from the website. `assets/pdf/CV.pdf` remains a legacy URL; changing only that file does not update the current dated download link. Preserve old URLs when possible so existing links remain usable.

## Add news or an image

Copy an existing dated Markdown file in `_news/`, give it a new filename and date, and replace the text. Avoid publishing announcements about appointments before they are confirmed.

For an image you have permission to share, use a descriptive filename in `assets/img/`, add meaningful alternative text, and insert it into a page with Markdown:

```md
![Description of the experiment](/assets/img/experiment.jpg)
```

Resize large photos before uploading. Keep captions clear about whether an image shows an experiment, simulation, or schematic.

## Keep content and theme maintenance separate

Routine content edits do not require updating Ruby packages, copying layouts, or merging the upstream al-folio repository. The theme packages are pinned so upgrades can be deliberate. Handle dependency upgrades in a separate branch, review release notes, build and inspect the site before merging.

Do not edit `gh-pages` or `_site`: those are generated output and will be overwritten. Keep personal source content on `master`. Git history records changes and can be used to revert a mistaken edit; retain your original CV and image source files too.

The public pages describe completed research and verified contributions. Unpublished proposal details, private career discussions and prospective appointments do not belong in routine site updates.

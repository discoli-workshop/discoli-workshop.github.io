# DISCOLI Workshop website

Source of <https://discoli-workshop.github.io/>, the website of the DISCOLI workshop on DIStributed COLlective Intelligence.
It is a single [Jekyll](https://jekyllrb.com/) site (theme: [minima](https://github.com/jekyll/minima)) holding all the editions of the workshop.

## Structure

- `<year>/`: one folder per edition, served at `https://discoli-workshop.github.io/<year>/`
    - `index.md`: call for papers (edition home page)
    - `committees.md`: committees (its `permalink` must be `/<year>/committees/`)
    - `program.md`: workshop program
    - `weditions.md`: redirect to the editions history
    - `assets/`: edition-specific files (e.g., CfP PDFs)
- `_data/editions.yml`: list of all editions, newest first. It drives:
    - the title, navigation menu, and footer of each edition's pages
    - the list of editions on the home page and on `/history/`
    - the home page redirect, which points to the first (i.e., current) edition
- `index.markdown`: home page (redirects to the current edition)
- `history.md`: list of all editions (`/history/`)
- `_layouts/`, `_includes/`, `_sass/`, `assets/`: theme customisations shared by all editions

## Starting a new edition

1. Copy the folder of the previous edition, e.g. `cp -r 2027 2028`, and update its content (dates, venue, links, committees, program, ...).
   Remember to update the `permalink` in `2028/committees.md`.
2. Add an entry for the new edition at the top of `_data/editions.yml`.
   From then on, the home page redirects to the new edition.

## Local preview

```bash
bundle install
bundle exec jekyll serve
```

and open <http://localhost:4000/>.

## Deployment

The site is built and published by GitHub Pages from the `master` branch.

Before the editions were merged here, each edition (2022-2026) was published from its own repository (`discoli-workshop/<year>`).
Those repositories are kept for reference only: their GitHub Pages site must stay disabled,
otherwise it takes precedence over the `<year>/` folder of this repository.

# Matthijs van der Lende's website

This site uses the al-folio v1 starter and its default gem-owned design. Navigation contains About, Research, Publications, Teaching, and CV. Example pages, posts, and assets remain in the source repository but are excluded from the published site. Template maintenance workflows have been removed; the deployment workflow checks formatting and style ownership, builds the site, and deploys it. Pull requests build without publishing.

## Publish at https://matthjs.github.io

GitHub user sites require a repository named after the account: `matthjs.github.io`. The current repository, `matthjs/matthijsvanderlende.github.io`, must be renamed before deploying this root-site configuration.

1. In the repository's **Settings → General**, change the repository name to `matthjs.github.io`.
2. Update your local remote: `git remote set-url origin git@github.com:matthjs/matthjs.github.io.git`.
3. In **Settings → Pages → Build and deployment**, choose **GitHub Actions** as the source.
4. Commit and push these changes to `main`. The **Build and deploy site** action publishes the site. You can also run it manually from the Actions tab.

If the GitHub CLI reports an invalid token, sign in with `gh auth login --hostname github.com` before using CLI operations.

The site is configured with `url: https://matthjs.github.io` and `baseurl: ""`. Build without overriding `baseurl`. The `/al-folio` base URL in the starter's contributor instructions is for its demo site, not this personal user site. See [GitHub's repository naming requirements](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site) and [Pages workflow documentation](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages).

## Update content

- **News:** `_pages/about.md`. News appears below the profile and contact links. Headlines use the years supplied in your CV; exact dates were not provided.
- **Photo:** replace `assets/img/profile-placeholder.svg`, or add a real photo under `assets/img/`, change `photo` in `_pages/about.md`, and replace the image path in `_config.yml`'s `include` list. The `assets/img/` directory is otherwise excluded to avoid publishing demo photos.
- **Publications:** `_bibliography/papers.bib`. `selected = {true}` adds a paper to the homepage. Paper links use [PMLR](https://proceedings.mlr.press/v265/lende25a.html) and the current [arXiv record](https://arxiv.org/abs/2509.12934).
- **Research:** `_pages/research.md`, including selected publications rendered from BibTeX.
- **Teaching:** `_pages/teaching.md`.
- **CV:** `assets/pdf/Matthijs_van_der_Lende_CV.tex` and its compiled PDF beside it. The CV tab redirects immediately to the PDF through `_pages/cv.html`. Edit the LaTeX source, compile it with `pdflatex`, and replace the PDF. `_data/cv.yml` retains the structured CV data for reference; it is not used by the PDF.
- **Favicon:** `assets/img/favicon.svg`, an MvL monogram in the default theme accent color.
- **Social links:** `_data/socials.yml`.

The biography and CV reflect the supplied CV, including the current MSc and teaching assistant status. Review these facts before publishing. No custom layouts, includes, Sass, or theme overrides are used.

## Local validation

Use Ruby 3.3.5, Bundler 4.0.6 (as pinned in `Gemfile.lock`), and Node 20 or newer:

```bash
bundle install
npm ci
npm run lint:prettier
npm run lint:style-contract
bundle exec al-folio upgrade audit --no-fail
JEKYLL_ENV=production bundle exec jekyll build
bundle exec jekyll serve --no-watch
```

The local site is at `http://localhost:4000/`. Dependencies can be installed into an ignored directory with `BUNDLE_PATH=vendor/bundle bundle install`.

To recompile the CV with a LaTeX installation containing its packages:

```bash
pdflatex -output-directory=assets/pdf assets/pdf/Matthijs_van_der_Lende_CV.tex
pdflatex -output-directory=assets/pdf assets/pdf/Matthijs_van_der_Lende_CV.tex
```

Commit the `.tex` and `.pdf` files only; build logs and auxiliary files are not website assets.

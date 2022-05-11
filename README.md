# UIEU Website
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A website for the Urban Institute Employees Union built with [Quarto](https://quarto.org/docs/websites/#:~:text=Quarto%20Websites%20are%20a%20convenient,rendering%20options%2C%20and%20visual%20style.).


## Files

- `_quarto.yml`: Quarto website settings
- `index.qmd`: qmd for homepage
- `faq.qmd`: qmd for FAQ page
- `about.qmd`: qmd for About Us page
- `index.qmd`: qmd for Contact page
- `.nojekyll`: Needed to disable some processing of HTML files that GitHub Pages does by default
- `docs/`: Directory where final website files are written out to and the directory that GH pages hosts sites from

## Custom styling

We created two custom `.scss` files for use in our dark and light themes:

- `www/flatly_custom_urnan_union.scss`
- `www/darkly_custom_urnan_union.scss`

These contain some simple variable overrides so that the colors displayed on the website align with the Union's [color palette](https://coolors.co/1f3ca3-d4e6b5-4d8b31-cc6600-98c1d9). 


## Deploying to Github Pages:

Follow the instructions from the Quarto [docs](https://quarto.org/docs/websites/publishing-websites.html) for GH pages with one important addition. The default R `.gitignore` file contains the  `docs/` directory for pkgdown websites. if this is the case, you need to either remove the `docs/` directory from your gitignore or call the quarto `output-dir` something other than `docs`. We just removed `docs/` from the `.gitignore` file. If you do not do this, your GH Pages builds will fail. 
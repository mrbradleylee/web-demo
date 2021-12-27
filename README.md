# Demo Node Build

A demonstration node build using 11ty SSG and Tailwind CSS.
Tailored to Micro Focus ADM Product line.

## How to use this template

**Requirements:**

1. Eleventy (developed and tested with version 0.12.1)
2. Tailwind CSS

All other dependencies are either linked from a CDN or included in this repository.

**Setup:**

1. run `npm install`
2. run `npm run serve`
3. open a browser and go to `http://localhost:8080`

**Basic configuration:**

1. Eleventy -> `./.eleventy.js`
2. Tailwind -> `./tailwind.config.js`

CSS is built via PostCSS and based on `./src/_includes/css/_page.css`. Building CSS gets triggered by `./src/css/page.11ty.js` and Tailwind's config is set to JIT (see: [Tailwind docs](https://tailwindcss.com/docs/just-in-time-mode))

**Change Content:**

Page content is stored in

-   `./src/`
    -   `imprint.md`
    -   `privacy.md`
-   `./src/sections/`
-   `./src/_data/features.json`

**Change Templates/Layout:**

Page structure and templates are stored in `./src/_layouts/` and can be edited there.

`./layouts/base.njk` is how it all comes together - the page itself is constructed from partial templates stored in `./src/includes/` and each section has a corresponding template file (`section.**.njk`) stored there.

`index.njk` in `./src/` arranges everything, meaning that sections can be added/re-ordered/removed/... there.

**Change images:**

Images are stored in `./static/img/`

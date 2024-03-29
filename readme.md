# Gulp template

I hope it makes life easier and development faster.

## Running the project locally

- Install all dependencies

```bash
npm i
```

- Install plugin `fontforge` for fonts generation on your OS:
  - OS X:

  ```bash
  brew install fontforge
  ```

  - Linux Ubuntu:

  ```bash
  sudo apt install fontforge
  ```

- Generate fonts

```bash
npm run font:generate
```  

- Start your project
  
```bash
npm run dev
```

- Build your project
  
```bash
npm run build
```

- Archive current production version of your project
  
```bash
npm run archive:zip
```

## File structure

- `gulp` - where the magic is working
  - `gulpfile.js` - main gulp configure
  - `common` - configs and paths
  - `tasks` - describe task you want the gulp to do
  - `version.json` - created dynamically to avoid caching files during development (don't touch it)
- `src` - our project
  - `fonts`
  - `img`
  - `scss`
    - `utilities` - contains tools, helpers, variables, mixins etc.
    - `base` - contains boilerplate code for the project. This includes styles such as resets, typography etc.
    - `components` - contains all the smaller page components like separated into multiple smaller files like slider, carousel etc.
    - `layout` contains the layout styles, separated into several smaller files like header, footer etc.
    - `pages` - contains page-specific styles. For example, the home page and search results page typically looks very different.
    - `themes` - contains files that are theme specific, like alternate color schemes (if any).
    - `vendors` - contains third party code from external frameworks and libraries like jQueryUi, Bootstrap etc.
    - `main.scss` - it should ONLY contain the imports for the above files  
  - `js`
  - `html` - partials of html (header, footer, sidebar)
  - `example.html`
  - `index.html` - main endpoint
- `dist` - containing production version of your project (it doesn't exist firstly)
- `archive` - containing archived production version of your project

There is an example of Wikipedia page. When you start your project, don't forget to delete it in `src/fonts/*`, `src/img/*`, `src/scss/example.scss` and using this file in `main.scss`, `src/example.html` and `archive/*`.

Also take a look another version of my [gulp template](https://github.com/themse/gulp-starter).

## Tech stack

Here's a brief high-level overview of the tech stack:

- [Node.js v.16.13.1](https://nodejs.org/) - a JavaScript runtime built on Chrome's V8 JavaScript engine.
- [Gulp v.4.0.2](https://gulpjs.com/) - A toolkit to automate & enhance your workflow

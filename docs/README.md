# Posting Place 
> A place to keep up with ideas

### authorship + version

`@Firmerest` \| `2026-09-14` \| `GOLF`

### deployments, codebase, & repo features 

  resource                     link
  ---------------------------- ----------------------
  PROD codebase                [`main`](https://github.com/Firmerest/fullstack-posting-place) <br>
  PROD server                  [GCP](https://connor.barrycumbie.com/pages/auth.html) <br>
  DEV codebase                 [`dev`](https://github.com/Firmerest/fullstack-posting-place/tree/dev) <br>
  DEV server                   [Render](https://fullstack-posting-place.onrender.com/pages/auth.html) <br>
  docs                         [`docs/`](https://github.com/Firmerest/fullstack-posting-place/tree/main/docs/) <br>
  published docs               [GitHub Pages](https://firmerest.github.io/fullstack-posting-place/docs) <br>
  CI/CD workflow               [`deploy.yml`](https://github.com/Firmerest/fullstack-posting-place/blob/main/.github/workflows/deploy-main-to-gcp.yml) <br>
  successful PROD deployment   [GitHub Action](https://github.com/Firmerest/fullstack-posting-place/actions/workflows/another.yaml) <br>
  resolved GOLF issue          [issue \#1](https://github.com/Firmerest/fullstack-posting-place/issues/1) <br>

### user story

- **As a** burgeoning full-stack developer,
- **I want** a CI/CD infrastructure
- **so that** I can develop locally, manage my code in GitHub, and
    automatically deploy changes to DEV and PROD environments.

### narrative

This GOLF iteration of the project deploys using NodeJS on server/app.js to serve the pages in /public to the user. It has 3 deployments, with production on its own SSL-certified url (as seen above) through GCP, the dev branch hosted through Render, and the docs for the repository hosted through Github Pages. Github is used as the blueprint; the dev and production servers automatically update whenever their respective branches are committed to, with Github Pages doing the same.

### architecture

``` text
LOCAL
  │
  ▼
GitHub
  │
  ├── dev  ──► Render ─────────► DEV
  │
  └── main ──► GitHub Actions ─► GCP ──► PROD
```

### stack

`HTML/CSS/JS` \| `Node.js` \| `Express` \| `Git/GitHub` \| `Render` \|
`GCP` \| `Linux` \| `Nginx` \| `PM2` \| `Certbot` \| `GitHub Actions`

### project structure

``` text
repo/
├── .github/
│   └── workflows/
│       └── deploy-main-to-gcp.yml
├── docs/
│   └── README.md
├── public/
│   └── assets/
│		├── js/
│		│	├── main.js
│		│	└── script.js
│		└── css/
│			└── styles.css
├── server/
│	├── app.js
│	├── package-lock.json
│	└── package.json
└── .gitignore
```

### GCP

external IP: `34.118.169.254`\
Linux user: `firmestmoon43`\
instructor SSH public key installed: `yes`

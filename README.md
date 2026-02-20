# Ionic App GitHub Pages PWA

![Ionic](https://img.shields.io/badge/Ionic-3880FF?style=flat-square&logo=ionic&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)

Deploy any Ionic Angular app as a Progressive Web App (PWA) to GitHub Pages with a single workflow file. Works with both standalone and module-based apps.

**Live Demo:** [Ionic PWA Demo](https://danielcregg.github.io/ionic-app-github-pages-pwa/)

## Overview

This repository provides a GitHub Actions workflow that automatically builds, configures, and deploys any Ionic Angular application as a fully-featured PWA to GitHub Pages. The workflow handles PWA setup, service worker registration, icon generation, deep linking, and intelligent caching -- all with zero manual configuration required.

## Features

- **Zero Config** -- Works automatically with any Ionic Angular project structure
- **Full PWA Support** -- Service worker, offline mode, and installable app capabilities
- **Smart Detection** -- Finds your Ionic project whether in root or subdirectory
- **Auto PWA Configuration** -- Sets up manifest, service worker, and icons automatically
- **Icon Generation** -- Creates all required PWA icon sizes from a single source image
- **Deep Linking** -- Handles routing for both tabbed and non-tabbed apps
- **Intelligent Caching** -- Caches npm packages, Angular builds, Ionic artifacts, and more
- **Standalone and Module Support** -- Works with both Angular standalone and NgModule architectures

## Prerequisites

- A GitHub repository with an Ionic Angular project
- GitHub Pages enabled on the repository (Settings > Pages > Source: GitHub Actions)

## Getting Started

### Installation

Add the workflow file to your Ionic Angular repository:

```bash
mkdir -p .github/workflows
curl -o .github/workflows/deploy.yml https://raw.githubusercontent.com/danielcregg/ionic-app-github-pages-pwa/main/.github/workflows/deploy.yml
```

### Usage

1. Enable GitHub Pages in your repository:
   - Go to **Settings** > **Pages**
   - Select **GitHub Actions** as the source

2. Push your changes:
   ```bash
   git add .github/workflows/deploy.yml
   git commit -m "ci: add GitHub Pages PWA deployment workflow"
   git push
   ```

3. Your app will automatically deploy to:
   ```
   https://<username>.github.io/<repo-name>/
   ```

The workflow supports any of these project layouts:

```
# Root-level project
my-repo/
  src/
  angular.json
  ionic.config.json

# Subdirectory project
my-repo/
  my-app/
    src/
    angular.json
    ionic.config.json
```

## Tech Stack

- **Framework:** Ionic 8 with Angular 18 (standalone)
- **Language:** TypeScript
- **PWA:** Angular Service Worker
- **CI/CD:** GitHub Actions
- **Hosting:** GitHub Pages

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

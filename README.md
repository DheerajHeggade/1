<div align="center">

# DEXTRO — Creator Link Hub

### A custom-built glassmorphism landing page for DEXTRO

A premium, dark glassmorphism hub connecting DEXTRO's content, creative portfolio, professional profile, and community channels — designed and configured by **Dheeraj Heggade**.

[![Build](https://github.com/DheerajHeggade/dextro-link-hub/actions/workflows/build.yml/badge.svg)](https://github.com/DheerajHeggade/dextro-link-hub/actions/workflows/build.yml)

**Live repository:** https://github.com/DheerajHeggade/dextro-link-hub

</div>

---

## About DEXTRO

**DEXTRO** is a creator-focused technology brand built around:

- Kannada tech and AI content
- Video editing and creative production
- Tutorials, tools, and workflows
- Creator resources and community
- Client-facing creative work

This repository contains the complete website setup used for the DEXTRO link hub: branding, page configuration, theme styling, assets, build configuration, and GitHub Pages deployment workflow.

## Design & Brand Direction

The website was redesigned around a **dark premium glassmorphism** visual system.

### Core visual language

- Frosted translucent cards
- Backdrop blur and layered depth
- Thin glass borders and subtle highlights
- Near-black editorial background
- Restrained DEXTRO accent treatment
- Responsive mobile-first layout
- Clean typography and strong visual hierarchy
- Subtle interaction states instead of excessive effects

The goal is a polished creator/media experience rather than a generic link-in-bio page.

## What This Project Includes

### DEXTRO profile hub

The main page brings together the official DEXTRO destinations:

| Destination | Link |
|---|---|
| YouTube | https://www.youtube.com/@Dextrokannada |
| Video Editing Portfolio | https://dextro-portfolio.vercel.app/ |
| LinkedIn | https://www.linkedin.com/in/dheeraj-heggade-183002345/ |
| Discord Server | https://discord.gg/Wfs4unPZw9 |
| Telegram DM | https://t.me/dheerajheggade |

### Custom branding

The project includes the DEXTRO visual identity, including the supplied DEXTRO logo and customized page metadata/content.

### Configuration-driven content

The page content is managed through `config.yml`, making it easy to update:

- Profile information
- Link destinations
- Social links
- Footer text
- Site metadata
- Theme selection

### Theme system

The project uses a theme-based architecture so the visual layer can be evolved independently from the page content.

The DEXTRO implementation uses the `glassmorphism` visual direction as the foundation and customizes it for the brand.

### Build & deployment

The project uses a Ruby/Liquid build pipeline to generate the static website.

```text
config.yml
    ↓
Liquid / Ruby build
    ↓
_output/
    ↓
GitHub Actions
    ↓
GitHub Pages
```

A successful local build produces the deployable static output in `_output/`.

## Local Development

### Requirements

- Ruby
- Bundler
- Git
- A browser

Install the Ruby dependencies:

```bash
bundle install
```

Build the site:

```bash
bundle exec ruby ./scaffold.rb
```

The generated files will appear in:

```text
_output/
```

### Local preview

The included preview script can build and serve the generated website:

```bash
./preview.sh
```

Default address:

```text
http://localhost:8080
```

On Windows, Git Bash is recommended for running the Bash preview script.

If you prefer to serve the already-generated output manually:

```powershell
cd _output
ruby -run -e httpd . -p 8080
```

## Project Structure

```text
dextro_final/
├── .github/
│   └── workflows/
│       └── build.yml          # Automated build/deployment workflow
├── assets/                    # Shared assets
├── plugins/                   # Optional build-time plugins
├── scripts/                   # Development/build helper scripts
├── themes/
│   └── glassmorphism/         # Visual theme
├── _output/                   # Generated static website
├── config.yml                 # DEXTRO page configuration
├── scaffold.rb                # Static-site build engine
├── preview.sh                 # Local preview helper
├── deploy.sh                  # Deployment helper
├── Gemfile
└── Gemfile.lock
```

## Updating the DEXTRO Page

Most content changes can be made directly in:

```text
config.yml
```

After editing:

```bash
bundle exec ruby ./scaffold.rb
```

Preview locally, then commit and push:

```bash
git add -A
git commit -m "Update DEXTRO link hub"
git push
```

GitHub Actions then handles the deployment workflow.

## GitHub Pages

The repository is configured for GitHub Pages deployment.

The intended deployment flow is:

```text
Push to main
    ↓
GitHub Actions
    ↓
Build DEXTRO site
    ↓
Publish generated output
    ↓
GitHub Pages
```

For the repository version, configure GitHub Pages to use the deployment branch produced by the workflow.

## Credits & Project Foundation

The **DEXTRO experience, branding, configuration, content, and visual customization were created for DEXTRO by Dheeraj Heggade**.

This repository uses an existing open-source Linkyee project as its underlying static link-page/build foundation. The original upstream license and required copyright notice are retained in `LICENSE`.

The DEXTRO-specific work focuses on:

- Brand direction
- Glassmorphism redesign
- DEXTRO logo integration
- Content and links
- Configuration
- Page presentation
- Repository customization
- Deployment setup
- Creator-focused UX

## License

The underlying project is distributed under the license included in [`LICENSE`](./LICENSE).

DEXTRO-specific branding, logo assets, copy, and original design work remain associated with **DEXTRO / Dheeraj Heggade**.

---

<div align="center">

### DEXTRO

**Tech • AI • Editing • Creator**

Built and customized for the DEXTRO brand.

</div>

# AdGuard Knowledge Base Website

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

`master` branch is published automatically to https://kb-adg.pages.dev/.

## Overview

The AdGuard Knowledge Base is a comprehensive documentation platform that provides users with detailed information about AdGuard products, features, and troubleshooting guides. It supports multiple languages and uses Docusaurus for static site generation.

## Quick Start

### Prerequisites

Before you begin, ensure you have installed:

- [Git](https://github.com/git-guides/install-git) - Version control system
- [pnpm](https://pnpm.io/installation) - Fast, disk space efficient package manager (recommended over npm)

### Installation

1. **Clone the Repository**
   ```bash
   git clone git@github.com:AdguardTeam/KnowledgeBase.git
   cd KnowledgeBase
   ```

   Alternatively, use the [GitHub Desktop](https://desktop.github.com/) app for a GUI-based approach.

2. **Install Dependencies**
   ```bash
   pnpm install
   ```

## Development Guide

### Lint Markdown

Maintain code quality by linting your markdown files:

```bash
# Check for markdown errors
pnpm lint:md

# Auto-fix errors automatically
pnpm lint:md --fix
```

**Tip:** VSCode users should install the [markdownlint extension](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) to see errors in real-time while editing.

### Run Locally

Start the development server:

```bash
pnpm start
```

This command:
1. Lints markdown files
2. Starts a local development server
3. Opens the website in your browser
4. Live reloads on file changes (no restart needed)

### Build for Production

Generate static content for deployment:

```bash
pnpm build
```

Output is placed in the `build/` directory, ready for any static hosting service.

### Additional Commands

- **`pnpm serve`** - Serve the build locally to verify production output
- **`pnpm clear`** - Clear generated cache and build artifacts
- **`pnpm docusaurus`** - Run Docusaurus CLI directly
- **`pnpm swizzle`** - Customize Docusaurus theme components

## Internationalization (i18n)

The Knowledge Base supports 12 languages: English, Russian, German, Czech, French, Spanish, Italian, Portuguese (Brazil), Japanese, Korean, Chinese (Simplified), and Chinese (Traditional).

### Debugging Translations Locally

Localizations are generated on-the-fly and stored in the `i18n/` folder (which is in `.gitignore`).

1. **Download Latest Translations**
   ```bash
   CROWDIN_PERSONAL_TOKEN="YOUR_TOKEN" pnpm run crowdin download
   ```

2. **Run Docusaurus with Specific Language**
   ```bash
   pnpm run start -- --locale de  # Example: German
   pnpm run start -- --locale ja  # Example: Japanese
   ```

For more details, see the [Crowdin documentation](https://crowdin.com/documentation).

## How to Contribute

We welcome contributions to improve the Knowledge Base! 

**For detailed contribution guidelines**, visit [Updating the Knowledge Base](https://adguard.com/kb/miscellaneous/contribute/updating-knowledge-base/).

### Contribution Steps

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Make your changes and lint markdown (`pnpm lint:md --fix`)
4. Commit your changes (`git commit -m 'Add: your feature'`)
5. Push to your fork (`git push origin feature/your-feature`)
6. Open a Pull Request with a clear description

## Project Structure

```
.
├── docs/              # Documentation source files (Markdown)
├── i18n/             # Internationalization files (generated)
├── src/              # Custom components and styling
├── static/           # Static assets (images, logos, etc.)
├── .github/          # GitHub configuration and workflows
├── package.json      # Project dependencies and scripts
├── docusaurus.config.js  # Docusaurus configuration
└── sidebars.js       # Sidebar navigation structure
```

## Configuration

### Docusaurus Config

Edit `docusaurus.config.js` to customize:
- Website title and tagline
- Base URL and deployment settings
- Theme configuration
- Navigation and footer links
- Markdown linting rules

### Environment Variables

The build process supports these environment variables:

```bash
URL=https://custom-domain.com
BASE_URL=/docs/
SEARCH_COLLECTION=custom-collection
SEARCH_HOST=search-instance.typesense.net
SEARCH_API_KEY=your-api-key
```

## Search

The site uses [Typesense](https://typesense.org/) for fast, typo-tolerant search. Configure search settings in `search.config.json`.

## Deployment

The `master` branch automatically deploys to Cloudflare Pages at https://kb-adg.pages.dev/.

For manual deployments with Crowdin integration:
```bash
pnpm deploy  # Syncs translations and deploys
```

## Support & Resources

- 🌐 **AdGuard Website**: https://adguard.com
- 📚 **Official Documentation**: https://adguard.com/support
- 💬 **Community Discussions**: https://adguard.com/discuss.html
- 🐛 **Report Issues**: https://github.com/AdguardTeam/KnowledgeBase/issues
- 📝 **Contribute Translations**: [Help Us Translate](https://crowdin.com/project/adguard)

## License

© 2009–2026 Adguard Software Ltd. All rights reserved.

---

**Last Updated**: 2026-08-24  
**Maintained by**: AdGuard Team

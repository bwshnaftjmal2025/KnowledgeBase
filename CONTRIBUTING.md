# Contributing to AdGuard Knowledge Base

Thank you for your interest in contributing to the AdGuard Knowledge Base! This guide will help you get started.

## Getting Started

1. **Fork the Repository** - Create a personal copy of the repo
2. **Clone Your Fork** - `git clone https://github.com/YOUR-USERNAME/KnowledgeBase.git`
3. **Create a Branch** - `git checkout -b feature/your-feature-name`
4. **Make Changes** - Edit and improve the documentation
5. **Test Locally** - Run `pnpm start` to preview changes
6. **Lint** - Run `pnpm lint:md --fix` to ensure quality
7. **Commit** - Use clear, descriptive commit messages
8. **Push** - Push to your fork and create a Pull Request

## Documentation Standards

### Markdown Format

- Use clear, concise language
- Follow markdown best practices
- Check formatting with `pnpm lint:md`
- Use proper heading hierarchy (h1, h2, h3, etc.)
- Add code blocks with syntax highlighting:
  ```markdown
  ```bash
  your code here
  ```
  ```

### File Organization

- Place new docs in appropriate `docs/` subdirectories
- Update `sidebars.js` if adding new documentation sections
- Use descriptive filenames in kebab-case: `my-feature.md`

## Code Quality

### Before Submitting a PR

1. **Lint Markdown**
   ```bash
   pnpm lint:md --fix
   ```

2. **Preview Changes**
   ```bash
   pnpm start
   ```

3. **Build for Production**
   ```bash
   pnpm build
   ```

4. **Check Links** - Verify all internal and external links work

## Pull Request Process

1. **Create a descriptive title** - e.g., "docs: Add troubleshooting guide for macOS"
2. **Write a clear description** - Explain what was changed and why
3. **Reference issues** - Link to related issues if applicable
4. **Keep changes focused** - One feature or fix per PR
5. **Update related docs** - If you change functionality, update documentation
6. **Request review** - Tag maintainers for review

### PR Title Format

Use conventional commits:
- `docs:` - Documentation changes
- `fix:` - Bug fixes
- `feat:` - New features
- `style:` - Formatting/styling
- `chore:` - Maintenance tasks

Example: `docs: Update installation guide for Windows`

## Translation Contributions

The Knowledge Base uses [Crowdin](https://crowdin.com/project/adguard) for translations.

### To Help Translate

1. Visit [AdGuard Crowdin Project](https://crowdin.com/project/adguard)
2. Select your language
3. Translate strings in the interface
4. Your translations will be reviewed and merged

## Reporting Issues

Found a problem? Please report it!

1. **Check existing issues** - Avoid duplicates
2. **Use issue templates** - Provide structured information
3. **Include details** - Steps to reproduce, expected vs actual behavior
4. **Attach screenshots** - If relevant to UI/documentation issues
5. **Be respectful** - Follow our Code of Conduct

## Questions & Discussions

- 💬 **GitHub Discussions** - General questions and ideas
- 📧 **Email** - Contact AdGuard Team directly
- 🐦 **Social Media** - Follow @AdGuard for updates

## Code of Conduct

Please be respectful and constructive:
- ✅ Welcome all skill levels
- ✅ Provide helpful feedback
- ✅ Respect different opinions
- ❌ No harassment or discrimination
- ❌ No spam or promotional content

## Getting Help

Stuck? Here are resources:

- 📚 **Docusaurus Docs** - https://docusaurus.io/docs
- 🔍 **GitHub Issues** - Search for similar problems
- 💬 **Discussions** - Ask the community
- 📧 **AdGuard Support** - https://adguard.com/support

## Recognition

Contributors are recognized in:
- Pull Request reviews
- Release notes
- Contributors list on the website

Thank you for making AdGuard Knowledge Base better! 🎉

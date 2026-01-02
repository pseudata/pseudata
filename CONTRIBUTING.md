# Contributing to Pseudata

Thank you for your interest in contributing to Pseudata! This document provides a quick overview to help you get started.

## Full Contributing Guide

For comprehensive documentation, please visit our **[Contributing Guide](https://pseudata.dev/contributing/)** on pseudata.dev.

## Quick Start

**Choose your contribution type:**

- **[Add a New Model](https://pseudata.dev/contributing/add-new-model/)** - Define new data structures like `Person`, `Product`, or `Order`
- **[Add a New Primitive](https://pseudata.dev/contributing/add-new-primitive/)** - Implement methods like `email()`, `hexColor()`, or `phoneNumber()`
- **[Add a New Resource](https://pseudata.dev/contributing/add-new-resource/)** - Add locale-specific data files for realistic generation
- **[Add a New Locale](https://pseudata.dev/contributing/add-new-locale/)** - Support new countries/regions with culturally appropriate data
- **[Add a New SDK](https://pseudata.dev/contributing/add-new-sdk/)** - Implement full SDK support for a new programming language

## Development Setup

Pseudata uses **Dev Containers** to ensure consistent development environments:

1. Install [Docker](https://www.docker.com/products/docker-desktop) and [VS Code](https://code.visualstudio.com/)
2. Install the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
3. Clone the repository:
   ```bash
   git clone https://github.com/pseudata/pseudata.git
   cd pseudata
   ```
4. Open in VS Code and click **"Reopen in Container"**
5. Run tests:
   ```bash
   make test
   ```

## Contribution Standards

- **Conventional Commits** - Use structured commit messages ([guide](https://pseudata.dev/contributing/#commit-message-convention))
- **Fixture-Based Testing** - All changes must include tests that verify cross-language consistency
- **Documentation** - Update relevant docs for new features
- **Code Quality** - Follow language conventions and add doc comments

## Testing

All contributions must include fixture-based tests to ensure cross-language consistency:

```bash
make generate  # Generate code from TypeSpec definitions
make test      # Run all language tests
```

Read more in the [Testing Guide](https://pseudata.dev/contributing/testing/).

## Pull Request Process

1. Create a feature branch: `feature/your-feature` or `fix/your-fix`
2. Follow [Conventional Commits](https://www.conventionalcommits.org/) format
3. Update `CHANGELOG.md` for user-facing changes
4. Ensure all tests pass
5. Submit a PR with a clear description

## Additional Resources

- **[Code of Conduct](CODE_OF_CONDUCT.md)** - Our commitment to an inclusive community
- **[Testing Guide](https://pseudata.dev/contributing/testing/)** - Deep dive into fixture-based testing
- **[GitHub Issues](https://github.com/pseudata/pseudata/issues)** - Report bugs or request features
- **[GitHub Discussions](https://github.com/pseudata/pseudata/discussions)** - Ask questions and share ideas

## License

By contributing, you agree that your contributions will be licensed under the [Apache License 2.0](LICENSE).

---

**Need help?** Visit the [full contributing guide](https://pseudata.dev/contributing/) or start a [discussion](https://github.com/pseudata/pseudata/discussions).


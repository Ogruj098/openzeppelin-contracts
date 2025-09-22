# Quick Start: Creating Pull Requests with Modern Tools

This is a quick reference for contributing to OpenZeppelin Contracts using modern development tools. For detailed instructions, see [MODERN_DEVELOPMENT_WORKFLOWS.md](MODERN_DEVELOPMENT_WORKFLOWS.md).

## 🤖 GitHub Copilot Chat

1. **Setup**: Enable Copilot Chat in your IDE (VS Code, JetBrains)
2. **Clone**: `git clone https://github.com/OpenZeppelin/openzeppelin-contracts.git`
3. **Install**: `npm install`
4. **Code**: Use Copilot Chat for guidance, code review, and test generation
5. **Commit**: Create descriptive commits with AI assistance
6. **PR**: Push and create pull request with AI-generated descriptions

**Example prompts**:

- "Help me implement an ERC721 extension following OpenZeppelin patterns"
- "Review this smart contract for security vulnerabilities"
- "Generate comprehensive tests for this new utility function"

## 💻 IDE Workflows

### VS Code

1. Install extensions: GitHub Copilot, Solidity, GitLens
2. Open repository: `code openzeppelin-contracts`
3. Create branch: `git checkout -b feature/your-feature`
4. Develop with AI assistance
5. Push and create PR through GitHub integration

### JetBrains IDEs

1. Enable GitHub Copilot in settings
2. Use built-in Git integration
3. Leverage code completion for Solidity

## 🎯 Agentic Coding Tools (MCP Support)

### Cursor IDE

- Use `@codebase` for repository context
- Ask pattern-specific questions
- Request automated refactoring

### Claude with MCP

- Set up MCP tools for Git/filesystem access
- Use context-aware suggestions
- Generate documentation automatically

### Aider (CLI)

```bash
pip install aider-chat
cd openzeppelin-contracts
aider
# Use natural language to describe changes
```

## 🚀 Raycast (macOS)

1. Install Raycast and Git/GitHub extensions
2. **⌘+Space** → "Clone Repository"
3. **⌘+Space** → "Create Branch"
4. Make changes with your preferred tools
5. **⌘+Space** → "Create Pull Request"

**Useful commands**:

- `git status` - Check repository status
- `npm test` - Run test suite
- `github pr create` - Create PR

## 🛠️ GitHub CLI Integration

```bash
# Install and authenticate
brew install gh  # macOS
gh auth login

# Fork and clone
gh repo fork OpenZeppelin/openzeppelin-contracts --clone
cd openzeppelin-contracts

# Create branch and PR
git checkout -b feature/your-feature
# Make your changes...
gh pr create --title "Your Feature" --body "Description"
```

## ✅ Essential Commands

```bash
# Linting and testing
npm run lint          # Check code style
npm run lint:fix      # Fix style issues
npm test              # Run all tests
npm run test:generation  # Test code generation

# Changesets (required for PRs)
npx changeset         # Create changelog entry

# Build and validation
npm run compile       # Compile contracts
npm run coverage      # Generate coverage report
```

## 🔒 Security Checklist

- [ ] Review all AI-generated code for vulnerabilities
- [ ] Run full test suite: `npm test`
- [ ] Check gas efficiency of new code
- [ ] Follow OpenZeppelin security patterns
- [ ] Never commit secrets or private keys
- [ ] Validate against multiple Solidity versions

## 📚 Resources

- [Full Modern Workflows Guide](MODERN_DEVELOPMENT_WORKFLOWS.md)
- [Contributing Guidelines](../CONTRIBUTING.md)
- [Engineering Guidelines](../GUIDELINES.md)
- [Security Policy](../SECURITY.md)
- [OpenZeppelin Forum](https://forum.openzeppelin.com/)

---

_Need help? Check the [OpenZeppelin Forum](https://forum.openzeppelin.com/) or open an issue for tool-specific problems._

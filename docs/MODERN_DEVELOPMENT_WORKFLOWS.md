# Modern Development Workflows for OpenZeppelin Contracts

This guide covers how to contribute to OpenZeppelin Contracts using modern development tools and workflows, including AI-powered coding assistants, IDE integrations, and automated pull request creation.

## Overview

OpenZeppelin Contracts welcomes contributions through various modern development workflows. Whether you're using GitHub Copilot Chat, your favorite IDE with AI assistance, agentic coding tools with MCP support, or macOS-specific tools like Raycast, this guide will help you contribute effectively.

## Creating Pull Requests with Modern Tools

### 1. GitHub Copilot Chat Integration

GitHub Copilot Chat provides AI-powered assistance directly in your development environment. Here's how to use it effectively with OpenZeppelin Contracts:

#### Setting Up

1. Ensure you have GitHub Copilot Chat enabled in your IDE (VS Code, JetBrains, etc.)
2. Clone the repository: `git clone https://github.com/OpenZeppelin/openzeppelin-contracts.git`
3. Install dependencies: `npm install`

#### Creating a Contribution

1. **Start a conversation** with Copilot Chat about your intended change
2. **Ask for guidance** on OpenZeppelin patterns and best practices
3. **Request code reviews** before committing changes
4. **Use Copilot** to generate comprehensive tests for your changes

Example prompts:

```
"Help me implement an ERC721 extension for batch transfers"
"Review this smart contract for security issues"
"Generate tests for this new utility function"
"What's the best practice for access control in OpenZeppelin?"
```

#### Pull Request Creation

1. Use Copilot Chat to help write clear commit messages
2. Ask for assistance with pull request descriptions
3. Request help with changelog entries using Changesets

### 2. IDE-Based Workflows

#### Visual Studio Code

1. **Extensions to install:**

   - GitHub Copilot & Copilot Chat
   - Solidity
   - GitLens
   - Prettier - Code formatter

2. **Workflow:**

   ```bash
   # Open in VS Code
   code openzeppelin-contracts

   # Create a new branch
   git checkout -b feature/your-feature-name

   # Use Copilot to assist with development
   # Commit changes with descriptive messages
   git add .
   git commit -m "feat: add new feature description"

   # Push and create PR
   git push -u origin feature/your-feature-name
   ```

#### JetBrains IDEs (WebStorm, IntelliJ IDEA)

1. **Enable GitHub Copilot** in IDE settings
2. **Use built-in Git integration** for branch management
3. **Leverage code completion** and suggestions for Solidity development

### 3. Agentic Coding Tools with MCP Support

Model Context Protocol (MCP) enables AI agents to interact with development tools seamlessly. Here's how to contribute using MCP-supported tools:

#### Cursor IDE

1. **Open the repository** in Cursor
2. **Use @codebase** to reference the entire OpenZeppelin codebase
3. **Ask specific questions** about implementation patterns
4. **Request automated refactoring** while maintaining compatibility

Example commands:

```
@codebase How do I extend the AccessControl contract?
@codebase Generate a new ERC token implementation following OpenZeppelin patterns
@codebase Review this code for gas optimization opportunities
```

#### Claude with MCP

1. **Set up MCP tools** for Git and file system access
2. **Use context-aware suggestions** based on the entire repository
3. **Generate comprehensive documentation** for new features
4. **Automate testing workflows**

#### Aider and Other CLI Tools

```bash
# Install aider
pip install aider-chat

# Start aider in the repository
cd openzeppelin-contracts
aider

# Use natural language to describe changes
# Aider will automatically create commits and manage Git workflow
```

### 4. Raycast on macOS

Raycast provides quick access to development workflows through its command palette and extensions.

#### Setup

1. **Install Raycast** from the Mac App Store
2. **Install Git/GitHub extensions**
3. **Configure GitHub authentication**

#### Workflow

1. **⌘+Space** to open Raycast
2. **Type "Clone Repository"** and select the OpenZeppelin Contracts repo
3. **Use "Create Branch"** command for new features
4. **Use "Commit Changes"** with AI-generated messages
5. **Use "Create Pull Request"** command to open directly in GitHub

#### Useful Raycast Commands for Contributing

- `git status` - Check repository status
- `npm test` - Run OpenZeppelin test suite
- `git commit` - Commit with AI-suggested messages
- `github pr create` - Create pull request with templates

### 5. GitHub CLI (gh) Integration

GitHub CLI works seamlessly with all modern development tools:

```bash
# Install GitHub CLI
brew install gh  # macOS
# or
npm install -g @github/cli  # Cross-platform

# Authenticate
gh auth login

# Create a new branch and PR in one command
gh repo fork OpenZeppelin/openzeppelin-contracts --clone
cd openzeppelin-contracts
gh checkout -b feature/your-feature
# Make your changes...
gh pr create --title "Your Feature" --body "Description of changes"
```

## Best Practices for Modern Workflows

### 1. AI-Assisted Code Review

- Use AI tools to review code before committing
- Ask for security-focused reviews specific to smart contracts
- Request gas optimization suggestions

### 2. Automated Testing

- Leverage AI to generate comprehensive test cases
- Use tools to automatically run tests before commits
- Ask for edge case testing scenarios

### 3. Documentation Generation

- Use AI to generate inline documentation
- Create comprehensive README updates
- Generate API documentation automatically

### 4. Consistent Code Style

- Configure AI tools to follow OpenZeppelin conventions
- Use automated formatting and linting
- Ensure Solidity style guide compliance

## Security Considerations

When using AI-powered tools with OpenZeppelin Contracts:

1. **Review all AI-generated code** for security vulnerabilities
2. **Test thoroughly** using the existing test suite
3. **Follow established patterns** from the OpenZeppelin codebase
4. **Never commit secrets** or sensitive information
5. **Validate gas efficiency** of generated code

## Integration with Existing Workflows

All modern development workflows should integrate with OpenZeppelin's existing processes:

### Changesets

```bash
# Generate changeset for your changes
npx changeset
# Follow prompts to describe your changes
```

### Linting and Testing

```bash
# Run linting
npm run lint

# Run tests
npm test

# Run specific test files
npm test test/token/ERC20/ERC20.test.js
```

### Release Process

- Follow the existing [release documentation](../RELEASING.md)
- Ensure compatibility with the automated release workflow
- Test changes against multiple Solidity versions

## Troubleshooting Common Issues

### AI Tool Configuration

- Ensure tools have access to the full repository context
- Configure ignore patterns for `node_modules` and build artifacts
- Set up proper Git configuration for commit signing

### IDE Integration

- Install required extensions for Solidity development
- Configure proper syntax highlighting and IntelliSense
- Set up debugging configurations for smart contracts

### Git Workflow Issues

- Use consistent branch naming conventions
- Ensure proper upstream configuration
- Follow OpenZeppelin's commit message guidelines

## Getting Help

If you encounter issues with modern development workflows:

1. **Check the main [CONTRIBUTING.md](../CONTRIBUTING.md)** for general guidelines
2. **Visit the [OpenZeppelin Forum](https://forum.openzeppelin.com/)** for community support
3. **Open an issue** for tool-specific problems
4. **Join community discussions** about development best practices

## Contributing to This Guide

This documentation is community-maintained. If you discover new tools or improved workflows, please:

1. Test the workflow thoroughly
2. Document the steps clearly
3. Submit a pull request with your improvements
4. Include examples and best practices

---

_This guide is designed to evolve with the development ecosystem. As new tools and workflows emerge, we encourage community contributions to keep it current and comprehensive._

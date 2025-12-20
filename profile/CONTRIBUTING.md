# Contributing to KahitSan Solutions

Thank you for your interest in contributing to KahitSan Solutions. This guide outlines the general workflow and conventions we follow across all our projects.

---

## General Workflow

### 1. Fork and Branch

Always work from the latest default branch (usually `main` or `master`). Create feature branches using descriptive names:

```bash
git checkout main
git pull origin main
git checkout -b feat/your-feature-name
```

**Branch naming convention:**
- `feat/` - New features
- `fix/` - Bug fixes
- `docs/` - Documentation updates
- `refactor/` - Code refactoring
- `test/` - Test additions or updates
- `chore/` - Maintenance tasks

### 2. Commit Style

Keep commits small, focused, and descriptive. Follow the conventional commits format:

```
type: brief description

Examples:
feat: add user authentication
fix: resolve token expiration issue
docs: update setup instructions
refactor: simplify data fetching logic
```

**Commit message guidelines:**
- Use lowercase for the description
- Keep the summary line under 72 characters
- Use present tense ("add feature" not "added feature")
- Be specific but concise

### 3. Pull Requests

Open a pull request early, even as a draft if you're still working on it. This encourages collaboration and early feedback.

**PR Title:** Use plain English without prefixes
- Good: "Add user authentication"
- Bad: "feat: add user authentication"

**PR Description:** Provide context on the problem you're solving and your approach. Keep it casual and conversational.

Example:
```
Added user authentication using Supabase. Users can now log in with email/password
or phone/PIN.

Changed from the original plan to use Supabase RLS instead of manual permission
checks for better security and simpler code.
```

### 4. Code Review

Expect code review before merge. Be open to feedback and iterate on your changes. Reviews help maintain code quality and spread knowledge across the team.

---

## Repository-Specific Guidelines

**Each repository has its own README with specific setup instructions, architecture details, and contribution guidelines.**

### Before Contributing to a Repository:

1. **Read the repository's README.md**
   - Contains setup instructions
   - Explains the architecture and project structure
   - Lists available scripts and commands
   - Provides troubleshooting tips

2. **Check for repository-specific docs**
   - Some repos have additional documentation in a `docs/` folder
   - Look for ARCHITECTURE.md, TESTING.md, or other guides
   - Read any CLAUDE.md files for detailed context

3. **Set up your development environment**
   - Follow the prerequisites listed in the README
   - Install dependencies
   - Configure environment variables
   - Verify the setup works before making changes

### Key Repositories

**Note:** You'll only see and be able to contribute to repositories you have access to. Focus on the projects visible to you.

#### pillar
Frontend framework monorepo. Read the README for:
- Multi-app architecture and switching mechanism
- Git submodule workflow for pillar-ui components
- Deployment configuration
- Routing and auth patterns

**Prerequisites:** Node.js 20+, npm

#### pillar-api
Backend API server. Read the README for:
- Supabase setup and local development
- API endpoint documentation
- Testing requirements (80%+ coverage)
- Three-layer architecture (routes, actions, ops)

**Prerequisites:** Bun 1.2.22+, Supabase project

#### pillar-ui
Shared component library (git submodule). Read the README for:
- Component structure (base vs composite)
- Development workflow
- Styling approach

**Prerequisites:** Node.js 20+, npm

#### pillar-storybook
Component documentation. Read the README for:
- Storybook setup
- Component story patterns
- Testing with Vitest

**Prerequisites:** Node.js 20+, npm

---

## Code Quality Standards

### Testing

Write tests for your changes when applicable. Testing requirements vary by repository:
- **pillar-api:** 80%+ coverage required (Bun:test)
- **Other repos:** Follow existing test patterns or add tests for critical functionality

Run tests before submitting your PR:
```bash
# Check the repo's README for specific test commands
npm test
bun test
```

### Type Checking

Most projects use TypeScript with strict mode. Ensure your code passes type checking:
```bash
npx tsc --noEmit
```

### Linting

Follow the existing code style in each repository. When in doubt, match the surrounding code.

---

## Communication

### Getting Help

If you need help or have questions:
- Open an issue in the repository with `[Question]` in the title
- Provide context about what you're trying to accomplish
- Include relevant error messages or logs

### Reporting Bugs

When reporting bugs, include:
- Steps to reproduce the issue
- Expected vs actual behavior
- Environment details (OS, Node version, etc.)
- Error messages or logs

### Proposing Features

Before working on a major feature:
- Open an issue to discuss the idea
- Explain the problem you're solving
- Describe your proposed solution
- Wait for feedback before investing significant time

---

## Development Environment

### Common Prerequisites

Most projects require:
- **Node.js** 20+ (LTS recommended)
- **npm** or compatible package manager
- **Git** with SSH access
- **Bun** 1.2.22+ (for pillar-api)

### Repository Access

You may not have access to all repositories in the organization. This is normal. Focus on contributing to the projects you can see and have been granted access to.

If you believe you should have access to a repository but don't see it, contact the repository maintainers.

---

## Important Reminders

### Do:
- Read the repository's README before starting
- Follow existing code patterns and conventions
- Write clear, descriptive commit messages
- Test your changes locally
- Ask questions when you're unsure
- Be respectful and professional in all communications

### Don't:
- Make large architectural changes without discussion
- Commit directly to main/master branches
- Include sensitive information (API keys, passwords) in code
- Submit PRs with failing tests or type errors
- Bundle unrelated changes in a single PR

---

## Summary

The key to successful contribution is simple:

1. **Read the README** of the repository you want to contribute to
2. **Follow the setup instructions** and verify everything works
3. **Make your changes** following the patterns you see in the codebase
4. **Test thoroughly** before submitting
5. **Open a PR** with clear description of what you did and why

Each repository has its own specific requirements and patterns. This guide provides general principles, but always defer to repository-specific documentation when it exists.

Thank you for contributing to KahitSan Solutions. Your contributions help us build better tools for everyone.

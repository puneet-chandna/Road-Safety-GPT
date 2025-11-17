<div align="center">

# 🤝 Contributing to Road Safety Expert System

Thank you for your interest in contributing! This document provides guidelines and instructions for contributing to the project.

</div>

---

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Reporting Bugs](#reporting-bugs)
- [Suggesting Features](#suggesting-features)

---

## 📜 Code of Conduct

### Our Pledge

We are committed to providing a welcoming and inclusive environment for all contributors, regardless of:
- Experience level
- Gender identity and expression
- Sexual orientation
- Disability
- Personal appearance
- Body size
- Race
- Ethnicity
- Age
- Religion
- Nationality

### Our Standards

**Positive behavior includes:**
- ✅ Using welcoming and inclusive language
- ✅ Being respectful of differing viewpoints
- ✅ Gracefully accepting constructive criticism
- ✅ Focusing on what's best for the community
- ✅ Showing empathy towards others

**Unacceptable behavior includes:**
- ❌ Trolling, insulting, or derogatory comments
- ❌ Public or private harassment
- ❌ Publishing others' private information
- ❌ Other conduct which could reasonably be considered inappropriate

---

## 🚀 Getting Started

### Prerequisites

- Node.js 18.x or higher
- Git
- A GitHub account
- Google Gemini API key (for testing)

### Fork and Clone

```bash
# Fork the repository on GitHub
# Then clone your fork

git clone https://github.com/YOUR_USERNAME/road-safety-expert-system.git
cd road-safety-expert-system/frontend
```

### Setup Development Environment

```bash
# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env and add your GEMINI_API_KEY

# Verify setup
node test-setup.js

# Start development servers
npm run dev
```

### Create a Branch

```bash
# Create a new branch for your feature/fix
git checkout -b feature/your-feature-name

# Or for bug fixes
git checkout -b fix/bug-description
```

---

## 💻 Development Workflow

### 1. Make Your Changes

- Write clean, readable code
- Follow existing code style
- Add comments for complex logic
- Update documentation if needed

### 2. Test Your Changes

```bash
# Run the development server
npm run dev

# Test manually:
# - Submit various road safety issues
# - Verify AI responses
# - Test share functionality
# - Check PDF generation
# - Test on mobile (responsive design)

# Run linter
npm run lint

# Build to ensure no errors
npm run build
```

### 3. Commit Your Changes

```bash
# Stage your changes
git add .

# Commit with a descriptive message
git commit -m "feat: add new feature description"
```

### 4. Push and Create PR

```bash
# Push to your fork
git push origin feature/your-feature-name

# Go to GitHub and create a Pull Request
```

---

## 📝 Coding Standards

### JavaScript/React

**Style Guide:**
- Use ES6+ features
- Prefer functional components with hooks
- Use meaningful variable names
- Keep functions small and focused
- Add JSDoc comments for complex functions

**Example:**
```javascript
/**
 * Generates a shareable report link
 * @param {Object} reportData - The report data to encode
 * @returns {string} The shareable URL
 */
const generateShareLink = (reportData) => {
  const encoded = btoa(JSON.stringify(reportData));
  return `${window.location.origin}/report?data=${encoded}`;
};
```

### Component Structure

```javascript
import React, { useState, useEffect } from 'react';

/**
 * Component description
 * @param {Object} props - Component props
 */
const MyComponent = ({ prop1, prop2 }) => {
  // State declarations
  const [state, setState] = useState(null);
  
  // Effects
  useEffect(() => {
    // Effect logic
  }, []);
  
  // Event handlers
  const handleClick = () => {
    // Handler logic
  };
  
  // Render
  return (
    <div className="container">
      {/* JSX */}
    </div>
  );
};

export default MyComponent;
```

### CSS/Tailwind

- Use Tailwind utility classes
- Keep custom CSS minimal
- Use semantic class names
- Ensure responsive design

```jsx
// Good
<div className="flex items-center justify-between p-4 bg-white rounded-lg shadow-md">

// Avoid
<div style={{ display: 'flex', padding: '16px' }}>
```

### File Naming

- Components: `PascalCase.jsx` (e.g., `ReportCard.jsx`)
- Utilities: `camelCase.js` (e.g., `apiHelper.js`)
- Styles: `kebab-case.css` (e.g., `custom-styles.css`)

---

## 📋 Commit Guidelines

### Commit Message Format

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

| Type | Description |
|------|-------------|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation changes |
| `style` | Code style changes (formatting, etc.) |
| `refactor` | Code refactoring |
| `perf` | Performance improvements |
| `test` | Adding or updating tests |
| `chore` | Maintenance tasks |

### Examples

```bash
# Feature
git commit -m "feat(report): add PDF export functionality"

# Bug fix
git commit -m "fix(api): handle empty CSV records correctly"

# Documentation
git commit -m "docs(readme): update deployment instructions"

# Style
git commit -m "style(components): format code with prettier"

# Refactor
git commit -m "refactor(api): simplify database loading logic"
```

---

## 🔄 Pull Request Process

### Before Submitting

- [ ] Code follows project style guidelines
- [ ] All tests pass locally
- [ ] Documentation is updated
- [ ] Commit messages follow guidelines
- [ ] Branch is up to date with main

### PR Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
How to test these changes

## Screenshots (if applicable)
Add screenshots for UI changes

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Documentation updated
- [ ] No new warnings
```

### Review Process

1. **Automated Checks** - CI/CD runs automatically
2. **Code Review** - Maintainers review your code
3. **Feedback** - Address any requested changes
4. **Approval** - Once approved, PR will be merged
5. **Deployment** - Changes deployed to production

### After Merge

```bash
# Update your local main branch
git checkout main
git pull upstream main

# Delete your feature branch
git branch -d feature/your-feature-name
```

---

## 🐛 Reporting Bugs

### Before Reporting

- Check existing issues
- Verify it's reproducible
- Test on latest version

### Bug Report Template

```markdown
**Describe the bug**
Clear description of the bug

**To Reproduce**
Steps to reproduce:
1. Go to '...'
2. Click on '...'
3. See error

**Expected behavior**
What should happen

**Screenshots**
If applicable

**Environment:**
- OS: [e.g., Windows 10]
- Browser: [e.g., Chrome 120]
- Version: [e.g., 1.0.0]

**Additional context**
Any other relevant information
```

---

## ✨ Suggesting Features

### Feature Request Template

```markdown
**Is your feature request related to a problem?**
Clear description of the problem

**Describe the solution you'd like**
What you want to happen

**Describe alternatives you've considered**
Other solutions you've thought about

**Additional context**
Mockups, examples, etc.
```

---

## 🎯 Areas for Contribution

### High Priority

- 🐛 Bug fixes
- 📝 Documentation improvements
- ♿ Accessibility enhancements
- 🌍 Internationalization (i18n)
- 🧪 Test coverage

### Feature Ideas

- 🔍 Advanced search filters
- 📊 Analytics dashboard
- 🗺️ Location-based recommendations
- 📱 Mobile app (React Native)
- 🔔 Email notifications
- 🎨 Theme customization
- 📈 Historical data tracking

### Documentation Needs

- Video tutorials
- API documentation
- Architecture diagrams
- Deployment guides for other platforms
- Troubleshooting guides

---

## 🏆 Recognition

Contributors will be:
- Listed in CONTRIBUTORS.md
- Mentioned in release notes
- Credited in documentation

---

## 📞 Getting Help

- **Questions:** Open a [Discussion](https://github.com/yourusername/road-safety-expert-system/discussions)
- **Issues:** Create an [Issue](https://github.com/yourusername/road-safety-expert-system/issues)
- **Chat:** Join our community (if applicable)

---

## 📚 Resources

### Learning Resources

- [React Documentation](https://reactjs.org/docs)
- [Vite Guide](https://vitejs.dev/guide/)
- [TailwindCSS Docs](https://tailwindcss.com/docs)
- [Vercel Documentation](https://vercel.com/docs)

### Project Resources

- [Architecture Overview](docs/ARCHITECTURE.md)
- [API Documentation](docs/API.md)
- [Deployment Guide](frontend/DEPLOYMENT.md)

---

<div align="center">

### 🙏 Thank You!

Your contributions make this project better for everyone.

**Happy Coding! 🚀**

</div>

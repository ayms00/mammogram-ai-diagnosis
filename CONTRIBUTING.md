# Contributing to MammoAI

Thank you for considering contributing! Here's how to get started.

## Reporting Bugs

- Use the **Issues** tab on GitHub
- Include your browser name + version
- Describe what you expected vs. what happened
- Include a screenshot if relevant

## Suggesting Features

Open an issue with the tag `enhancement` and describe:
- What problem the feature solves
- How you'd expect it to work

## Pull Requests

1. **Fork** the repository
2. **Create a branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. **Make your changes** — keep commits focused and well-described
4. **Test** by opening `index.html` in multiple browsers (Chrome, Firefox, Safari)
5. **Push** your branch and **open a Pull Request**

## 📐 Code Style

- Use 2-space indentation in HTML/CSS/JS
- Keep CSS variables in `:root` for easy theming
- Add comments for non-obvious logic
- Prefer vanilla JS — no framework dependencies

## Commit Message Format

```
type: short description

Examples:
feat: add DICOM file parsing
fix: heatmap overlay alignment on mobile
docs: update README with deployment steps
style: improve dark mode contrast ratios
```

## Medical Content

Any medical content changes (accuracy claims, dataset stats, clinical language) must:
- Cite a credible source in the PR description
- Include the academic/educational disclaimer where appropriate

---

We appreciate every contribution, big or small! 🙏

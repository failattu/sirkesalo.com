# Agent Guidelines for sirkesalo.com

This document provides guidelines for AI coding agents working on this repository.

## Project Overview

- **Type**: Static HTML personal website
- **Hosting**: GitHub Pages with custom domain (sirkesalo.com)
- **Tech Stack**: Pure HTML5 with embedded CSS, no JavaScript
- **Philosophy**: Zero-dependency, ultra-minimal, maintenance-free

## Build, Test, and Deployment

### No Build Required
This is a static HTML site with no build process. Changes to `index.html` are deployed directly.

### Deployment
- Hosted on GitHub Pages
- Push to main branch to deploy automatically
- Custom domain configured via CNAME file

### Testing
No automated testing framework is configured. For changes:
1. Open `index.html` in a browser to visually verify
2. Test responsiveness using browser DevTools (especially mobile viewport at 768px breakpoint)
3. Validate HTML: Use online validators or browser DevTools
4. Check all navigation links work correctly
5. Verify external links (LinkedIn, YouTube, Eficode profile)

### Running Single Tests
Not applicable - no test framework is configured.

## Code Style Guidelines

### HTML Structure
- **DOCTYPE**: Always use `<!DOCTYPE html>`
- **Semantic HTML**: Use semantic tags (`<header>`, `<nav>`, `<section>`, `<article>`, `<footer>`)
- **Accessibility**: Include `alt` attributes for images, `lang` attribute on `<html>`, proper heading hierarchy
- **Meta tags**: Maintain viewport meta tag for mobile responsiveness

### CSS Style
- **Embedded CSS**: All styles must remain in `<style>` tag within `<head>` - do NOT create external CSS files
- **CSS Variables**: Use existing CSS custom properties (e.g., `--sea-deep`, `--wood-varnish`) for consistency
- **Mobile-first**: Existing mobile breakpoint at `@media (max-width: 768px)` - maintain this approach

### Design System
The site uses a **sailing-themed color palette**:
- `--sea-deep: #0A3D61` - Primary brand color (deep ocean blue)
- `--sea-lighter: #2E6F94` - Secondary blue
- `--wood-varnish: #C07D48` - Accent color (warm teak wood)
- `--wood-dark: #8B572A` - Darker accent
- `--bg-warm: #F8F5F0` - Warm cream background (sailcloth)
- `--bg-white: #ffffff` - Pure white for contrast

**Typography**:
- Headings: `Merriweather` serif (via Google Fonts)
- Body: `Lato` sans-serif (via Google Fonts)

### Formatting Conventions
- **Indentation**: 4 spaces (maintain consistency with existing code)
- **Line length**: Aim for ~100-120 characters max for readability
- **Comments**: Add CSS comments for major sections (e.g., `/* Navigation */`)
- **Whitespace**: One blank line between major CSS rule blocks

### Naming Conventions
- **CSS Classes**: Use kebab-case (e.g., `.nav-container`, `.hero-content`, `.card-link`)
- **IDs**: Use kebab-case for section anchors (e.g., `#about`, `#speaking`, `#contact`)
- **CSS Variables**: Use kebab-case with semantic names (e.g., `--sea-deep`, `--font-body`)

### Content Guidelines
- **Tone**: Professional but approachable, nautical/sailing metaphors fit the theme
- **Sections**: Maintain existing structure (About, Speaking, Writing, YouTube, Contact)
- **External links**: Always include `target="_blank"` for external URLs
- **Images**: Keep images in root directory, optimize for web (current: `kalle.jpg`)

### Error Handling
Not applicable - no JavaScript or server-side code.

## Common Tasks

### Adding a New Speaking Engagement
1. Locate the `#speaking` section
2. Add a new `<article class="card">` within `.grid-cards`
3. Follow existing structure: `<span class="card-meta">`, `<h3>`, `<p>`, `<a class="card-link">`
4. Ensure link has `target="_blank"`

### Adding a New Blog Post
1. Locate the `#writing` section
2. Add a new `<article class="card">` within `.grid-cards`
3. Use consistent structure with other cards
4. Keep descriptions concise (2-3 sentences max)

### Modifying Colors
1. Update CSS variables in `:root` section
2. Do NOT hardcode colors - always use variables
3. Maintain sailing theme coherence

### Updating Profile Information
1. Modify content in `#about` section
2. Keep bio conversational and professional
3. Maintain the sailing metaphor if appropriate

### Mobile Responsiveness
- Test changes at 768px breakpoint
- Grid layouts should stack appropriately
- Navigation should remain functional
- Images should scale properly

## Git Workflow

### Commit Messages
Based on existing history:
- Use lowercase imperative mood (e.g., "add new speaking engagement")
- Keep messages concise and descriptive
- Examples from history: "added starter version of index.html", "added a new picture"

### Branch Strategy
- Work directly on `main` branch (simple project)
- Changes deploy automatically via GitHub Pages

## File Structure

```
sirkesalo.com/
├── CNAME              # GitHub Pages custom domain config
├── index.html         # Main and only HTML file
├── kalle.jpg          # Profile image
└── AGENTS.md          # This file
```

## Important Constraints

### DO NOT:
- ❌ Create external CSS files (styles must stay embedded)
- ❌ Add JavaScript unless explicitly requested
- ❌ Add build tools, package managers, or dependencies
- ❌ Create additional HTML files (single-page design)
- ❌ Modify CNAME file without explicit instruction
- ❌ Break mobile responsiveness
- ❌ Remove or modify CSS custom properties without good reason

### DO:
- ✅ Maintain zero-dependency philosophy
- ✅ Use semantic HTML5 elements
- ✅ Keep all styles in embedded `<style>` tag
- ✅ Test responsiveness at mobile breakpoint
- ✅ Preserve sailing theme and color palette
- ✅ Keep code simple and maintainable
- ✅ Validate HTML structure
- ✅ Use CSS variables for all colors

## Questions or Clarifications

When uncertain about design decisions:
1. Maintain consistency with existing patterns
2. Prioritize simplicity over complexity
3. Keep the sailing theme cohesive
4. Preserve mobile-first responsive design
5. Ask the user if major structural changes are needed

---

**Last Updated**: Generated for coding agents on 2026-03-23

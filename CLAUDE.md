# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

GONEINSEC.COM is a static website focused on cybersecurity research and security content. The site uses a dark, terminal-style design aesthetic with blue color accents, monospace fonts, and a technical security theme.

## Architecture

This is a pure static HTML/CSS site designed for deployment on Azure Static Web Apps:

- **index.html** - Main landing page with ASCII banner, blog list, and navigation
- **css/style.css** - Dark theme stylesheet with terminal aesthetic
- **blog/** - Directory containing individual blog post HTML files
- **js/** - Directory for future JavaScript (currently unused)

### Design Philosophy

- Dark, high-contrast color scheme (black backgrounds, blue/cyan accents)
- Monospace fonts throughout for technical aesthetic
- ASCII art banner for branding
- Code-focused styling with syntax highlighting support
- Responsive and accessible design
- Blue color scheme (#4a9eff, #00d4ff, #7eb8ff)

## Adding New Blog Posts

To add a new blog post:

1. Create a new HTML file in the `blog/` directory (e.g., `blog/my-new-post.html`)
2. Copy the structure from `blog/example-post.html` as a template
3. Update the content, title, metadata, and date
4. Add an entry to the blog list in `index.html`:

```html
<li>
    <a href="blog/my-new-post.html">Your Post Title</a>
    <div class="blog-date">YYYY-MM-DD</div>
    <div class="blog-excerpt">Brief description of the post</div>
</li>
```

5. Commit and push to GitHub - Azure Static Web Apps will automatically deploy

## Deployment

The site is configured for Azure Static Web Apps deployment. When files are pushed to GitHub, Azure automatically builds and deploys the updated site.

To set up Azure Static Web Apps:
1. Create a Static Web App resource in Azure Portal
2. Connect it to this GitHub repository
3. Azure will auto-generate a workflow file in `.github/workflows/`
4. The workflow triggers on push to main branch

## Content Guidelines

- Content covers cybersecurity research including both offensive and defensive security topics
- Focus areas: security testing, vulnerability research, security tools, threat analysis, practical solutions
- Include appropriate legal disclaimers and ethical warnings
- Use the technical terminal aesthetic consistently
- Structure posts with clear sections using `<h2>` for major sections
- Include code examples in `<pre><code>` blocks
- Use checkmarks (✓) and warning symbols ([!]) for emphasis
- Balance between offensive security techniques and general security content

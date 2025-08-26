# simplefolio

A dead-simple, highly accessible portfolio template. No build tools, no dependencies, just a single HTML file that works everywhere.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Size](https://img.shields.io/badge/size-~20KB-purple.svg)
![Accessibility](https://img.shields.io/badge/WCAG-AAA-darkgreen.svg)

## Features

- **Automatic dark/light mode**: respects system preferences with manual override
- **Fully accessible**: WCAG AAA compliant, keyboard navigable, screen reader friendly
- **Responsive**: Looks great on all devices
- **Semantic HTML**: properly structured for SEO and accessibility
- **Lightning fast**: single file, no dependencies, under 10KB
- **Easy to customize**: well-commented code, CSS variables for theming
- **Clean typography**: optimal readability with proper link indicators
- **Smart year display**: shows "this year", "last year", etc. (uses JS)

## Quick Start

1. Download `index.html`
2. Edit the content:
   - Add your name
   - Update the bio text
   - Add your contact links
   - Add your projects
3. Deploy anywhere (GitHub Pages, Netlify, Vercel, or any static host)

That's it! No build process, no npm install, just edit and go.

## Adding Content

### Adding a new project

Projects are organized by year, with the most recent years at the top. Each project includes a title, description, and optional metadata tags.

```html
<article class="project">
    <div class="project-title-wrapper">
        <a href="YOUR_PROJECT_URL" class="project-title">Project Name</a>
        <span class="external-icon" aria-hidden="true">↗</span>
    </div>
    <p class="project-description">Brief description of your project.</p>
    <div class="project-meta">
        <span>active</span>
        <span>open source</span>
    </div>
</article>
```

### Adding a new year section

Years are displayed with smart relative time (e.g., "this year", "last year", "2 years ago") when JavaScript is enabled, falling back to just the year number without JS.

```html
<section class="year-section" aria-labelledby="year-2026">
    <h2 id="year-2026" data-year="2026">
        <span class="year-default">2026</span>
        <span class="year-relative"></span>
        <span class="year-absolute"></span>
    </h2>
    <!-- Add projects here -->
</section>
```

## Customization

### Colors

Edit the CSS variables in the `:root` selector:

```css
:root {
    --bg: #ffffff;
    --text: #1a1a1a;
    --text-muted: #666666;
    --link: #0066cc;
    --link-hover: #0052a3;
    --border: #e0e0e0;
}
```

### Dark theme colors

```css
[data-theme="dark"] {
    --bg: #1a1a1a;
    --text: #e0e0e0;
    --text-muted: #999999;
    --link: #66b3ff;
    --link-hover: #99ccff;
    --border: #333333;
}
```

### Typography

The template uses system fonts for optimal performance. To change fonts, update the `font-family` in the body selector.

## Accessibility Features

- **Skip to main content** link for keyboard users
- **Proper heading hierarchy** (h1 → h2 → h3)
- **ARIA labels** on all interactive elements
- **Screen reader announcements** for theme changes
- **Focus indicators** meeting WCAG AAA standards
- **Semantic HTML** structure
- **Respects prefers-reduced-motion**
- **Minimum 44x44px touch targets**
- **Proper link underlines** for color-blind users

## Support The Project

You can support simplefolio by contributing through these links:

[![Buy Me A Coffee](https://cdn.cottle.cloud/tabcloser/buttons/button-bmac.svg)](https://buymeacoffee.com/seth)

[![PayPal](https://cdn.cottle.cloud/tabcloser/buttons/button-paypal.svg)](https://www.paypal.com/paypalme/sethcottle)

[![GitHub Sponsors](https://cdn.cottle.cloud/tabcloser/buttons/button-ghs.svg)](https://github.com/sponsors/sethcottle)

Signing up through these services through these affiliate links is also a good way to support simplefolio.

[![Try DigitalOcean](https://cdn.cottle.cloud/tabcloser/buttons/button-do.svg)](https://m.do.co/c/632b45e20266)

[![Try Fathom Analytics](https://cdn.cottle.cloud/tabcloser/buttons/button-fa.svg)](https://usefathom.com/ref/EQVZMV)


## Stay Connected

Join the [Seth's Nook Discord](https://discord.gg/PrAEQFF2fK) server to get updates on simplefolio and more. Use the invite code `PrAEQFF2fK` or click the button below.

[![Discord](https://cdn.cottle.cloud/tabcloser/buttons/button-discord.svg)](https://discord.gg/PrAEQFF2fK)


## License

MIT License - feel free to use this for any purpose.

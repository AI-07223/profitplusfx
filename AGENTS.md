# Profit Plus FX - AI Coding Agent Guide

## Project Overview

**Profit Plus FX** is a premium Forex and Cryptocurrency education and investment platform website. It's a static, single-page application (SPA) landing page designed to attract users interested in:

- Forex & Crypto trading education
- Investment plans with structured returns
- Dashboard-based portfolio tracking
- Referral and rewards programs

The website features a luxury dark theme with gold accents, inspired by high-end trading platforms like GTCFX and BitCapitalX.

## Technology Stack

| Category | Technology |
|----------|------------|
| **Frontend** | HTML5 (Single File) |
| **Styling** | Tailwind CSS (CDN) + Custom CSS |
| **Fonts** | Google Fonts (Inter) |
| **Icons** | Inline SVG |
| **Animations** | CSS Keyframes + Intersection Observer API |
| **Charts** | HTML5 Canvas API (JavaScript) |
| **Build Tool** | None (Static Website) |

### External Dependencies
- `https://cdn.tailwindcss.com` - Tailwind CSS framework
- `https://fonts.googleapis.com` - Google Fonts (Inter font family)

## Project Structure

```
fxkimi/
├── index.html          # Main and only HTML file (~3360 lines)
├── logo.png            # Brand logo (~102 KB)
└── rewards/            # Reward images directory
    ├── bike-reward.png
    ├── car-reward.png
    ├── dubai-trip.png
    ├── iphone-reward.png
    ├── maldives-trip.png
    ├── quarterly-events.png
    ├── singapore-trip.png
    └── thailand-trip.png
```

## Architecture

### Single-File Architecture
The entire website is contained in a single `index.html` file with:
1. **Head Section**: Meta tags, Tailwind config, Google Fonts, and extensive custom CSS
2. **Body Section**: Semantic HTML structure with 10 main sections
3. **Script Section**: Vanilla JavaScript for interactivity at the bottom

### Page Sections

| Section ID | Purpose | Features |
|------------|---------|----------|
| `#home` | Hero Section | Login/Signup forms, dashboard preview, market snapshot |
| `#about` | About | Company overview, transparency features |
| `#services` | Services | 6 service cards (Portfolio, Fund Mgmt, Education, etc.) |
| `#plans` | Investment Plans | 3-tier pricing (Starter/Growth/Elite) |
| `#courses` | Training Programs | Course table, enrollment form |
| `#referral` | MLM Structure | SVG bridge diagram, rank achievements |
| `#rewards` | Incentives | 8 reward cards with images (trips, gadgets, vehicles) |
| `#faq` | FAQ | Common questions accordion-style |
| `#contact` | Contact | Contact info, inquiry form |

### Design System

#### Color Palette
- **Primary Gold**: `#d4af37` (main brand color)
- **Primary Light**: `#f4d03f` (highlights)
- **Background Dark**: `#000000` to `#0f172a` (slate-950)
- **Card Background**: `rgba(20, 20, 20, 0.9)` with glassmorphism
- **Accent Colors**: Green (`#10b981`), Blue (`#3b82f6`), Purple (`#8b5cf6`)

#### CSS Custom Properties
Defined in `:root` for consistent theming:
- `--primary`, `--primary-light`, `--primary-glow`
- `--gold-gradient`, `--gold-text`
- `--bg-dark`, `--bg-card`
- Section-specific watermark backgrounds (`--wm-about`, `--wm-services`, etc.)

#### Animation Classes
- `.fadeup` - Fade up entrance animation
- `.reveal` - Scroll-triggered reveal
- `.card-hover` - Hover lift effect
- `.gold-shimmer` - Shimmering gold effect
- `.pulse` - Pulsing indicator

## Development Conventions

### CSS Guidelines
1. **Tailwind First**: Use Tailwind utility classes for layout and spacing
2. **Custom CSS for**: 
   - Complex animations (keyframes)
   - Gold gradient effects
   - Section-specific backgrounds
   - Glassmorphism effects (`backdrop-filter`)
   - Responsive breakpoints beyond Tailwind

3. **Naming Convention**:
   - Component classes: `.luxury-card`, `.glass`, `.gold-border`
   - Animation classes: `.fadeup`, `.reveal`, `.card-hover`
   - Section backgrounds: `.bg-about`, `.bg-services`, etc.

### Responsive Breakpoints
- **Mobile**: ≤768px (reduced animations, single column)
- **Extra Small**: ≤375px (further typography reduction)
- **Tablet**: 769px - 1024px (2-column grids)
- **Desktop**: ≥1025px (full layout)
- **Large Desktop**: ≥1440px (wider containers)
- **Ultra Wide**: ≥1920px (maximum width)

### Image Handling
- All reward images are in `rewards/` folder
- Logo is at root level as `logo.png`
- Images use `object-cover` for consistent sizing
- Hover effects include `scale-110` transform

## Build and Run

### No Build Required
This is a static website with no build process. Simply:

```bash
# Option 1: Open directly in browser
open index.html

# Option 2: Use a local server (recommended for proper asset loading)
python -m http.server 8000
# or
npx serve .
# or
php -S localhost:8000
```

### Deployment
Deploy the entire folder to any static hosting:
- GitHub Pages
- Netlify
- Vercel
- Traditional web hosting (Apache/Nginx)
- AWS S3 + CloudFront

## Key JavaScript Features

### Market Ticker (`moveRandom()`)
- Simulates live market data updates every 2.5 seconds
- Updates prices with small random variations
- Updates both ticker row and market table

### Canvas Chart (`drawChart()`)
- Real-time line chart using HTML5 Canvas
- Auto-resizes with window
- Animated data points

### Mobile Navigation
- Hamburger menu toggle
- Full-screen overlay navigation
- Body scroll lock when open
- Close button and link click handling

### Scroll Animations
- Intersection Observer API for `.reveal` elements
- Triggers at 10% visibility threshold
- Applies `visible` class for CSS transitions

## Testing

### Manual Testing Checklist
- [ ] Navigation links scroll to correct sections
- [ ] Mobile menu opens/closes properly
- [ ] Market ticker updates automatically
- [ ] Canvas chart renders and animates
- [ ] All images load correctly
- [ ] Forms (Login, Signup, Enrollment, Contact) are interactive
- [ ] Responsive layout at all breakpoints
- [ ] Scroll reveal animations trigger correctly

### Browser Compatibility
Target browsers (based on CSS features used):
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile Safari (iOS 14+)
- Chrome Android

## Security Considerations

### Current State
- **No backend**: All forms are client-side only (no actual submission)
- **Demo data**: Market data is simulated, not real
- **No authentication**: Login/signup are UI mockups

### Before Production
If adding backend functionality:
1. Implement proper form validation and CSRF protection
2. Use HTTPS for all external resources
3. Sanitize user inputs
4. Implement rate limiting on API endpoints
5. Add Content Security Policy (CSP) headers

## Code Organization Tips

### When Editing
1. **CSS**: Custom styles are in the `<style>` block (lines 30-2199)
   - Component styles: Lines 30-120
   - Animations: Lines 120-170
   - Section backgrounds: Lines 797-902
   - Responsive styles: Lines 1257-2198

2. **HTML**: Sections are clearly commented (e.g., `<!-- ABOUT -->`)

3. **JavaScript**: Located at the bottom (lines 3209-3357)
   - Market data simulation
   - Canvas chart rendering
   - Event listeners

## Notes for AI Agents

1. **Language**: All content is in English, but pricing is in USD (plans) and INR (courses)
2. **Location Context**: The project appears to target Indian market (WhatsApp/phone format hints)
3. **Brand Identity**: Gold/yellow is the primary brand color representing premium/luxury
4. **No Framework**: This is vanilla HTML/CSS/JS - no React, Vue, or Angular
5. **CDN Dependencies**: Requires internet connection for Tailwind and Google Fonts
6. **Image Assets**: Don't modify files in `rewards/` folder without preserving filenames

# Profit Plus FX Landing Page

A premium, single-file landing page for a Forex & Crypto education and investment platform.

![Profit Plus FX](logo.png)

## Features

- **Responsive Design** - Works on mobile, tablet, and desktop
- **Live Market Ticker** - Animated market data display
- **Interactive Chart** - Canvas-based trend visualization
- **Modern UI/UX** - Glass morphism, gold accents, smooth animations
- **Single File** - Everything in one HTML file (CSS + JS included)

## Sections

- Hero with dashboard preview
- About
- Services
- Investment Plans (Starter, Growth, Elite)
- Courses & Training
- Referral Bridge & Rank System
- Rewards & Experiences
- FAQ
- Contact Form

## Quick Start

Simply open `index.html` in a browser:

```bash
# Clone the repository
git clone <repository-url>

# Open the file
open index.html
```

Or serve with a local server:

```bash
# Python 3
python -m http.server 8000

# Node.js
npx serve .

# PHP
php -S localhost:8000
```

## File Structure

```
.
├── index.html          # Main landing page (HTML + CSS + JS)
├── logo.png            # Company logo
├── INTEGRATION_GUIDE.txt  # CRM integration documentation
├── README.md           # This file
└── rewards/            # Reward images
    ├── thailand-trip.png
    ├── dubai-trip.png
    ├── singapore-trip.png
    ├── maldives-trip.png
    ├── iphone-reward.png
    ├── bike-reward.png
    ├── car-reward.png
    └── quarterly-events.png
```

## Technologies Used

- HTML5
- Tailwind CSS (CDN)
- Vanilla JavaScript
- Canvas API
- Intersection Observer API

## Customization

### Change Colors

Edit CSS variables in `index.html`:

```css
:root {
  --primary: #d4af37;        /* Gold */
  --primary-light: #f4d03f;  /* Light gold */
  --accent: #c5a028;
  --bg-dark: #000000;
}
```

### Update Content

Simply edit the HTML sections to change text content.

### Replace Images

Swap out images in the `rewards/` folder and update the paths in HTML.

## CRM Integration

See [INTEGRATION_GUIDE.txt](INTEGRATION_GUIDE.txt) for detailed instructions on connecting this landing page to a backend CRM system.

Key integration points:
- User authentication (login/signup)
- Live market data API
- Investment plan subscriptions
- Course enrollment forms
- Contact form submissions

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Performance

- Single file architecture for fast loading
- Optimized images
- Minimal external dependencies
- Hardware-accelerated animations

## License

Copyright © 2025 Profit Plus FX. All rights reserved.

## Contact

- Email: support@profitplusfx.com
- WhatsApp: +14453149552
- Telegram: [@profitplus_fx](https://t.me/profitplus_fx)

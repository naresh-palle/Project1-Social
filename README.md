# PALRAM AI — Website

Marketing site for PALRAM AI (palramai.in) — AI agents, automation, and custom software development.

Static, multi-page site. No build step or framework dependency — open any `.html` file directly, or serve the folder with any static host.

## Structure

```
palram-ai-website/
├── index.html            # Home — short overview + links out to every section
├── services.html         # All 6 service categories + DevOps/cloud
├── ai-solutions.html     # AI development, AI agents, model/tech stack
├── portfolio.html        # Case studies + tech stack
├── industries.html       # Industries served + testimonials
├── about.html            # Why choose us + process
├── pricing.html          # Cost calculator + pricing tiers + FAQ
├── contact.html          # Contact form
├── assets/
│   ├── css/style.css     # All styles (shared across pages)
│   ├── js/script.js      # Theme toggle, nav, reveals, calculator, FAQ, chat mock
│   └── img/               # Logo (dark/light/symbol variants) + favicons
└── README.md
```

Clicking the logo on any page returns to `index.html`. The current page is highlighted in the nav.

## Run locally

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Deploy

Static site — deploy directly to GitHub Pages, Vercel, Netlify, or any static host. No build command needed.

## Known gaps (static front end — needs backend work to go fully live)

- **Contact form** (`contact.html`) shows a confirmation alert on submit only. Wire it to Formspree, a serverless function, or your CRM's API to actually receive submissions.
- **Chatbot widget** replies with canned, keyword-matched responses. Swap `sendChat()` in `assets/js/script.js` for a real API call when ready.
- **Booking calendar, client dashboard, and blog CMS** from the original brief aren't included — each needs real infrastructure beyond static pages.

## Customization

Brand colors, fonts, and spacing are CSS variables at the top of `assets/css/style.css` (`:root` and `[data-theme="light"]`). Each page's content is plain HTML in its own file — no templating engine, just edit directly.

# tejas-kumar.com

Personal portfolio — live at **[tejas-kumar.com](https://tejas-kumar.com)**

Single-file site for my work as an Agentic AI / ML Engineer: production AI systems
for regulated industries — banking, healthcare, finance, utilities. All projects are
described at the pattern level; nothing here includes employer code, data, or
confidential information.

## Stack

- One `index.html` — vanilla HTML, CSS and JavaScript. No frameworks, no build step.
- `api/chat.js` — a Vercel serverless function powering **Lumen**, the site's AI assistant
  (OpenAI API, key held in a Vercel environment variable, never in client code)
- Fonts: Space Grotesk, Inter, IBM Plex Mono (Google Fonts)
- Contact form: Formspree
- Hosting: Vercel, auto-deployed from `main`
- Domain and DNS: Cloudflare

## Lumen — portfolio assistant

Lumen answers questions about my experience, grounded strictly in my resume via its
system prompt. Guardrails: answers only from the profile, refuses to invent, declines
prompt-injection attempts, keeps all work at the pattern level, and routes anything
personal to the contact form. Capped history, capped tokens, honeypot-free and
rate-sane by design.

## Features

- Animated preloader, scroll reveals, typewriter role titles
- Interactive pipeline diagram of a governed agentic workflow (fig.01)
- Tech-stack marquee, per-project expandable logs, suggestion chips in chat
- Contact form with inline status and a honeypot spam trap
- Respects `prefers-reduced-motion` throughout

## Run locally

Clone the repo and open `index.html` in a browser. The site works fully;
Lumen needs the deployed serverless function, so chat replies only on the live site.

## Deploy

Merge to `main` — Vercel builds and deploys automatically.

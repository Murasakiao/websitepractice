# 🗂️ Portfolio Website — Project Specification
**Owner:** Julius Darang  
**Role:** Renewable Energy & Power Systems Modelling Engineer  
**Last Updated:** 2026-03-23  
**Status:** Planning Phase

---

## 1. Project Overview

A personal portfolio website for Julius Darang, an Electrical Engineer specializing in Renewable Energy and Power Systems Modelling. The site should serve as a professional online presence — showcasing projects, skills, experience, and a blog — while being visually distinctive with a **clean, minimal, professional aesthetic** inspired by Bryl Lim's site (bryllim.com): white backgrounds, tight typography, monospace accents, and restrained use of color.

The target audience is:
- Potential employers & recruiters
- Fellow engineers and collaborators
- Clients looking for freelance/consulting work

---

## 2. Tech Stack

### Frontend
| Tool | Purpose |
|------|---------|
| **HTML5 + Tailwind CSS** | Markup & utility-first styling |
| **Vanilla JavaScript** | Interactivity, animations, scroll effects |
| **Google Fonts** | Typography (see Section 6 for choices) |

> ✅ Why not Next.js? Julius has experience with Flask + Tailwind CSS. This stack is more approachable and still produces a fast, professional result. Next.js can be a future upgrade.

### Backend (Contact Form only)
| Tool | Purpose |
|------|---------|
| **Flask (Python)** | Handles contact form POST requests & email sending |
| **Flask-Mail or smtplib** | Sends email via Gmail SMTP |
| **python-dotenv** | Manages secrets (email credentials) safely |

### Hosting & Deployment
| Service | Purpose |
|---------|---------|
| **Vercel** | Hosts the static frontend (HTML/CSS/JS) for free |
| **Render.com** | Hosts the Flask backend (free tier) for the contact form API |
| **GitHub** | Version control & source of truth for both repos |

> 💡 Why split? Vercel doesn't run Python natively. The frontend calls the Flask API (on Render) via `fetch()` when the contact form is submitted. This is a common, clean pattern.

### Domain
- Not purchased yet. Recommended registrars: **Namecheap** or **Cloudflare Registrar**
- Suggested domain: `juliusdarang.com` or `juliusdarang.dev`
- Connect custom domain to Vercel for free after purchase

---

## 3. Site Sections & Content Plan

### 3.1 — Hero (Landing)
- Full name: **Julius Darang**
- Title: **Renewable Energy & Power Systems Modelling Engineer**
- Location: *(add your city/country)*
- Tagline: *(1 punchy line — e.g. "Designing the grid of tomorrow.")*
- Status badge: small pill label (e.g. "Open to opportunities") — green dot + text
- CTA Buttons:
  - `View My Work` → scrolls to Projects
  - `Download CV` → downloads PDF resume
  - `Send Email` → scrolls to Contact
- Avatar: Profile photo in a rounded square (88×88px), with a fallback icon
- Background: Clean white — no patterns, no effects

### 3.2 — About
- Short bio paragraph (3–5 sentences): who you are, what you do, what drives you
- *(Julius to write this — keep it human and personal)*
- Stats cards (3 cards stacked on the right side):
  - `2+` Years of Experience
  - `X` Projects Completed *(fill in)*
  - `X` Certifications *(fill in)*
- Stats use monospace font for the number, muted label below

### 3.3 — Experience (Timeline)
Display as a vertical timeline with a left border line and dot markers.

| Year | Role | Company | Description |
|------|------|---------|-------------|
| *(fill)* | *(your latest role)* | *(company name)* | *(1-line description)* |
| *(fill)* | *(previous role)* | *(company name)* | *(1-line description)* |
| *(fill)* | BS Electrical Engineering | *(university name)* | *(1-line description)* |

- Current/most recent role dot is filled blue (accent color) with a soft glow ring
- Older roles use an empty circle dot
- Year shown in monospace, muted color above the role title

### 3.4 — Skills & Tools
Grouped by category. Each category has a muted bold label and a row of tag badges below.

**Categories:**
- **Power Systems & Simulation:** MATLAB, Simulink, DIgSILENT PowerFactory, ETAP, PSCAD, PSS/E
- **Renewable Energy Tools:** Homer Pro, PVsyst, RETScreen, SAM (NREL)
- **Design & Drafting:** AutoCAD, AutoCAD Electrical, Revit MEP
- **Programming & Data:** Python, Pandas, NumPy, Flask, Excel VBA, Git
- **Standards & Frameworks:** IEC 60364, IEEE Standards, NEC/PEC, Grid Codes

Tag style: small pill with light gray background, monospace font, subtle border on hover.

### 3.5 — Projects
Card grid (2 columns). Each card has: title, arrow icon (top right), description, and tag chips.

**Template per project (add as many as needed):**
```
Title: [Project Name]
Description: [2-3 sentences on what it is, what you did, what the outcome was]
Tags: [tools/technologies used] — shown as blue-tinted chip badges
Link: [GitHub / report / live demo — card is clickable if link exists]
```

Tag style on project cards: blue text on light blue background (`#eff4ff` bg, `#2563eb` text).

**Starter projects to fill in:**
- [ ] Thesis / Capstone project
- [ ] Any power systems modelling study
- [ ] Renewable energy feasibility study
- [ ] Any Python/simulation script you built
- [ ] Any work project you can describe (without confidential info)

### 3.6 — Certifications
List of certification rows. Each row: cert name + issuer on the left, year on the right (monospace). Subtle hover border effect.

| Certification | Issuer | Year |
|--------------|--------|------|
| Registered Electrical Engineer (REE) | PRC | *(year)* |
| *(add others)* | | |

### 3.7 — Blog
- Simple blog index page: list of posts with title, date, short excerpt
- Each post is a separate HTML page
- Topics Julius could write about:
  - Power systems concepts explained simply
  - Renewable energy trends in the Philippines / Southeast Asia
  - Python for electrical engineers
  - Career advice for EE graduates
- *(Start with 1–2 posts)*

### 3.8 — Hobbies / Personal
- A short, informal section humanizing the portfolio
- *(Julius to fill in his actual hobbies)*
- Optional: small photo gallery (3–6 images)

### 3.9 — Contact
- Two-column layout: left side has heading + description + contact links; right side has the form
- Form fields: Name, Email (side by side), Subject, Message
- Contact link items: each has a small square icon tile + label text
- On submit: POST to Flask backend → success/error shown inline (no page reload)
- Links to show: Email, LinkedIn, GitHub, Schedule a Call

### 3.10 — Footer
- Copyright: `© 2026 Julius Darang. All rights reserved.`
- Quick nav links on the right: LinkedIn, GitHub, Blog

---

## 4. Visual Design Direction

### Theme
**Clean Minimalist — Professional**

- Think: lots of white space, crisp borders, restrained color use, monospace details
- Inspired by: Bryl Lim's bryllim.com — clean layout, readable typography, card-based sections
- NOT: dark themes, neon effects, cyberpunk aesthetics, heavy animations

### Color Palette
```
Background:      #ffffff  (pure white)
Surface/Cards:   #fafaf8  (barely-off-white card backgrounds)
Soft Background: #f7f7f5  (section backgrounds, input fields)
Border:          #e8e8e4  (default borders)
Border Strong:   #d0d0c8  (hover borders)
Primary Accent:  #2563eb  (blue — used for links, active dots, project tags)
Accent Soft:     #eff4ff  (light blue backgrounds for project tag chips)
Text Primary:    #1a1a18  (near-black body text)
Text Muted:      #6b6b66  (secondary text, descriptions)
Text Light:      #9a9a94  (timestamps, labels, placeholders)
Tag Background:  #f0f0ec  (skill tag background)
Tag Text:        #4a4a44  (skill tag text)
Status Green:    #16a34a  (open-to-work badge)
Status Green Bg: #f0fdf4  (open-to-work badge background)
```

### Typography
```
Display / Body:    "DM Sans" — clean, geometric, readable at all sizes
Monospace accents: "DM Mono" — used for: nav logo, section title labels,
                              stat numbers, timeline years, cert years,
                              project tag chips, skill tags
```

Both fonts are free on Google Fonts. Import both weights:
- DM Sans: 300, 400, 500, 600, italic 400
- DM Mono: 400, 500

### Visual Effects (CSS Only — Minimal)
- **Scroll fade-in:** Intersection Observer API — elements fade up into view on scroll (`opacity: 0` → `1`, `translateY(16px)` → `0`)
- **Hover borders:** Cards and list items get a stronger border on hover (`border-color` transition)
- **Hover card shadow:** Project cards get a subtle `box-shadow` on hover
- **Button opacity:** Primary buttons reduce opacity on hover (clean, no color shift)
- **Form input focus:** Border turns accent blue on focus
- **Animated counters:** JS counter animation when stats scroll into view *(optional)*
- **No:** glitch effects, scan lines, grid overlays, neon glows, custom cursors, parallax

### Spacing & Layout
- Max content width: `900px`, centered, with `32px` horizontal padding
- Section padding: `72px` top and bottom
- Section dividers: `1px solid var(--border)` between sections
- Nav height: `56px`, sticky, with `backdrop-filter: blur(12px)` and white background at 92% opacity

---

## 5. File & Folder Structure

```
julius-portfolio/
│
├── index.html              ← Main single-page site
├── blog/
│   ├── index.html          ← Blog listing page
│   └── post-1.html         ← Individual blog post
│
├── assets/
│   ├── css/
│   │   └── style.css       ← Custom CSS (supplements Tailwind)
│   ├── js/
│   │   └── main.js         ← Scroll animations, counter, mobile menu
│   ├── images/
│   │   ├── profile.jpg     ← Your professional photo (used in hero avatar)
│   │   ├── projects/       ← Project screenshots (optional)
│   │   └── hobbies/        ← Hobby/gallery photos
│   └── cv/
│       └── julius-darang-cv.pdf  ← Downloadable CV
│
├── tailwind.config.js      ← Tailwind config (custom colors/fonts)
├── package.json            ← Node config (for Tailwind CLI)
└── README.md               ← Setup instructions

── flask-backend/           ← Separate repo or subfolder
   ├── app.py               ← Flask app with /send-email route
   ├── requirements.txt     ← Flask, Flask-Mail, python-dotenv
   ├── .env                 ← Email credentials (NEVER commit this)
   └── .gitignore           ← Must include .env
```

---

## 6. Pages & Routes

| Page | File | Description |
|------|------|-------------|
| Home (all sections) | `index.html` | Single-page portfolio |
| Blog Index | `blog/index.html` | List of all blog posts |
| Blog Post | `blog/post-[slug].html` | Individual post page |

---

## 7. Contact Form — Backend Plan

**Flask route:** `POST /send-email`

**Request body (JSON):**
```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "subject": "Project Inquiry",
  "message": "Hello Julius..."
}
```

**Steps:**
1. Frontend `fetch()` sends form data to Flask API URL
2. Flask validates fields (not empty, valid email format)
3. Flask uses Gmail SMTP to send email to Julius's inbox
4. Returns JSON `{ "success": true }` or `{ "error": "..." }`
5. Frontend shows success/error message without page reload

**Environment variables needed (in `.env`):**
```
MAIL_USERNAME=yourgmail@gmail.com
MAIL_PASSWORD=your-gmail-app-password   ← NOT your real password, use Gmail App Password
RECIPIENT_EMAIL=yourgmail@gmail.com
```

> ⚠️ You need to enable **2FA on Gmail** and generate an **App Password**. Julius to do this before deploying the backend.

---

## 8. Deployment Plan

### Step 1 — Frontend (Vercel)
1. Push `julius-portfolio/` to a GitHub repo
2. Go to vercel.com → Import repo → Deploy
3. Vercel auto-detects static HTML — no config needed
4. (Later) Connect custom domain in Vercel dashboard

### Step 2 — Backend (Render.com)
1. Push `flask-backend/` to a separate GitHub repo (or subfolder)
2. Go to render.com → New Web Service → Connect repo
3. Set environment variables (MAIL_USERNAME, MAIL_PASSWORD, etc.) in Render dashboard
4. Set start command: `gunicorn app:app`
5. Copy the Render public URL → paste into frontend `fetch()` call

### Step 3 — Domain (Optional, later)
1. Buy domain at Namecheap or Cloudflare (~$10–15/year)
2. Point DNS to Vercel (they give you instructions)
3. Add domain in Vercel dashboard → auto SSL certificate

---

## 9. Content Checklist (Julius to fill in)

Before handing to coding agent, complete this:

- [ ] Write your bio (3–5 sentences for About section)
- [ ] Write your tagline (1 punchy line for Hero)
- [ ] Decide status badge text (e.g. "Open to opportunities" or "Available for freelance")
- [ ] List all work experience (role, company, year range, 1-line description)
- [ ] List all projects (title, description, tags, links)
- [ ] List all certifications (name, issuer, year)
- [ ] List your hobbies (and optionally upload 3–6 hobby photos)
- [ ] Prepare your CV as a PDF → save as `julius-darang-cv.pdf`
- [ ] Prepare a professional profile photo → save as `profile.jpg` (square crop recommended)
- [ ] Set up Gmail App Password for contact form
- [ ] Write 1–2 blog post drafts (optional but recommended)
- [ ] Decide on final domain name
- [ ] Fill in stats: number of projects completed, number of certifications

---

## 10. Build Order (Recommended Sequence)

Build in this order to avoid redoing work:

```
Phase 1 — Setup
  → Install Tailwind CSS via CLI
  → Set up folder structure
  → Configure tailwind.config.js with custom colors & fonts
  → Add Google Fonts import (DM Sans + DM Mono)
  → Set up CSS variables for the color palette

Phase 2 — Frontend Sections (in order)
  → Nav (sticky, with logo + links + CTA button)
  → Hero (avatar, badge, name, title, location, tagline, 3 buttons)
  → About (bio paragraph + 3 stat cards)
  → Experience timeline
  → Skills tag groups
  → Projects card grid
  → Certifications list
  → Hobbies / Gallery
  → Contact (two-column: info + form)
  → Footer

Phase 3 — JS Interactions
  → Scroll fade-in (Intersection Observer)
  → Animated stat counters
  → Mobile nav menu toggle
  → Contact form fetch() call

Phase 4 — Flask Backend
  → Set up Flask app
  → Build /send-email route
  → Test locally
  → Deploy to Render

Phase 5 — Deploy & Polish
  → Deploy frontend to Vercel
  → Connect Flask URL to frontend
  → Test contact form end-to-end
  → Performance check (image compression, etc.)
  → (Optional) Buy & connect domain
```

---

## 11. Estimated Effort

| Phase | Estimated Time (with Claude's help) |
|-------|--------------------------------------|
| Setup | 30 min |
| Frontend (all sections) | 3–5 hours |
| JS interactions | 1–2 hours |
| Flask backend | 1–2 hours |
| Deployment | 1 hour |
| Content writing (bio, projects, etc.) | 2–4 hours |
| **Total** | **~9–14 hours** (spread over multiple sessions) |

> 💡 With Claude generating code section by section, each frontend phase can be done in one focused session. You provide your content, Claude writes the code.

---

## 12. How to Work With Claude on This

When you're ready to build, start a new chat and say:

> *"I'm building my portfolio based on project.md. Let's start with [Phase X — Section Y]. Here's my content: [paste your info]"*

Claude will generate the exact code for that section. You paste it into VS Code, open it in your browser, and review. Iterate section by section.

**Useful prompts to use:**
- `"Generate the Hero section HTML using Tailwind CSS with the color palette from my project.md"`
- `"Write the Flask /send-email route based on my project.md backend plan"`
- `"Help me deploy my Flask backend to Render step by step"`
- `"Review my index.html and suggest improvements for mobile responsiveness"`

---

*This file is a living document. Update it as the project evolves.*

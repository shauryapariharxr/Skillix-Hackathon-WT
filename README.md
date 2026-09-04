# Skillix

**Learn Skills. Build Your Future.**

Skillix is a static, front-end-only online learning / course platform website built with **HTML5 and CSS3 only** (no JavaScript, frameworks, or backend), for the Advanced Web Technologies (CSE0309) Mini Hackathon.

> **Note on folder structure:** the original hackathon brief specifies exactly three shared CSS files (`style.css`, `responsive.css`, `components.css`). This build instead ships **one shared stylesheet, `css/index.css`**, linked by every page. This is a deliberate deviation from the "mandatory folder structure" in the brief — confirm with your instructor before submitting if strict adherence to the original structure is required for grading.

## Project Structure

```
Skillix/
│
├── index.html
├── about.html
├── services.html
├── login.html
├── register.html
├── payment.html
├── legal.html
├── test.html          (scratch/dev file — not part of the site, see Notes)
│
├── css/
│   └── index.css      (single shared stylesheet used by every page)
│
├── images/
│   ├── logo.svg
│   ├── hero-art.svg
│   ├── course-*.svg   (6 course icons)
│   └── team-*.svg      (3 team avatars)
│
└── README.md
```

Every page links the same stylesheet: `<link rel="stylesheet" href="css/index.css">`.

## Pages

| Page | File | Contents |
|---|---|---|
| Home | `index.html` | Hero with CTA, feature/course preview cards, short About section |
| About Us | `about.html` | Company story, Mission, Vision, Team cards |
| Services / Courses | `services.html` | 6 course cards (image, title, description, price, Enroll button) |
| Login | `login.html` | Email, Password, Remember Me, Forgot Password, link to Register |
| Register | `register.html` | Full Name, Email, Password, Confirm Password, Phone, Gender, Course dropdown, Terms checkbox |
| Payment / Checkout | `payment.html` | Order summary table, card payment fields, static "Pay Now" demo |
| Legal / Privacy | `legal.html` | Privacy Policy, Terms & Conditions, Refund Policy |

Every page shares the same Navbar and Footer for a consistent layout, and uses semantic HTML5 (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).

## AI Prompts Used

The following prompts were used with AI assistance during development of this project:

1. Create only this component: Skillix Navbar (semantic header/nav, brand + links to Home, About, Courses, Login, Register).
2. Create only this component: Skillix Footer (brand blurb, page links, copyright, semantic footer).
3. Create only this page: index.html (Home) — hero section ("Learn. Practice. Succeed." / "Build industry-ready skills with practical courses." / "Explore Courses" CTA linking to services.html), 4 feature/course preview cards, short About section.
4. Create only this page: about.html (About Us) — company introduction, Mission section, Vision section, 3 team member cards with image, name and role.
5. Create only this page: services.html (Courses/Services) — 6 course cards (Java Programming, Web Development, Python Programming, Data Structures & Algorithms, Database Management, AI & Machine Learning) each with image, title, description, price and Enroll Now button.
6. Create only this page: login.html — Email field, Password field, Remember Me checkbox, Forgot Password link, link to Register page, centered layout.
7. Create only this page: register.html — Full Name, Email, Password, Confirm Password, Phone, Gender radio buttons, Course/Interest dropdown, Terms & Conditions checkbox, Submit button.
8. Create only this page: payment.html — Order Summary table (Product, Quantity, Price, Total) with a sample Skillix course order, payment fields (Card Number, Expiry Date, CVV, Name on Card), Pay Now button, clearly marked as a static demo with no real payment processing.
9. Create only this page: legal.html — Privacy Policy, Terms & Conditions and Refund Policy sections with proper headings and paragraphs.
10. Create only this CSS task: responsive styling (mobile, tablet, desktop breakpoints) for the Navbar, Footer and all seven pages.
11. Create only this CSS task: hover effects for buttons, cards and navigation links across the site.
12. Create only this task: review all pages for semantic HTML, image alt text, working navigation links and responsiveness; produce the Skillix README.md with the AI prompt list.
13. Create only this CSS task: split the shared stylesheets into one individual, self-contained CSS file per page (index.css, about.css, services.css, login.css, register.css, payment.css, legal.css), and update each page's `<link>` tag accordingly.
14. Create only this design refresh: taking visual/interaction cues from a reference SaaS landing page (dark hero, prominent search bar with trending tags, staggered entrance animations) and a peer project's README (pure-CSS `fadeInUp` keyframes, glassmorphic sticky navbar, button hover = lift + `scale(1.04)`) — add a hero search bar with trending course chips to `index.html`, staggered `fadeInUp` entrance animation on the hero content, a permanent elevation shadow on the sticky navbar, and a scale-up hover state on all buttons, keeping Skillix's existing navy/violet color system. Also flatten the zip/output folder structure so `index.html` sits at the project root instead of inside a nested folder.
15. Create only this rebrand + navbar redesign: rename the project from the previous name to **Skillix**, design a new logo mark (`images/logo.svg` — gradient rounded-square badge with a connected-dots motif), swap the old letter-badge logo for it across every page, and rebuild the navbar as a floating glassmorphic pill (inset from the viewport edges, rounded corners, dark translucent blur background, permanent elevation shadow) instead of a full-width bar — including a matching floating glass card for the mobile dropdown menu. Also restyle the home page hero heading into a two-line treatment with an italic gradient accent line ("Learn skills. / *Build your future.*"), inspired by a reference landing page's hero typography.

> **Note:** step 13 above split styles into one file per page; the codebase has since been consolidated back to a single shared `css/index.css` (see Project Structure). Update this log with the actual prompt if you re-run that consolidation intentionally — it isn't currently recorded as its own step.

## Design System

- **Theme:** dark navy/violet, glassmorphic surfaces
- **Background:** near-black navy (`#05070d` / `#090c17`)
- **Surfaces:** translucent glass panels (`rgba(255,255,255,0.045–0.09)`) over navy (`#0e1327` / `#121834`)
- **Accent gradient:** blue → violet (`#4d7bff` → `#7c6cf6`, with `#a99bff` as a lighter violet accent)
- **Secondary accent:** mint (`#34e5a8`)
- **Text:** off-white (`#f3f4fb`) with muted gray-blue for secondary text (`#aab0c9`, `#7c82a0`)
- **Typography:** Sora (headings/display) + Inter (body), loaded from Google Fonts
- **Layout:** CSS Flexbox and CSS Grid
- **Navbar:** floating glassmorphic pill, inset from the viewport edges with a permanent elevation shadow
- **Buttons:** pill-shaped, scale-up + lift hover state

## Notes

- No JavaScript, frameworks, libraries, or backend code is used, per the hackathon rules.
- The mobile navigation menu toggle is implemented with a CSS-only checkbox technique (no JS).
- `payment.html` is a static demo — no real payment is processed.
- `test.html` is a leftover scratch file from development (a bare "hello" page with no styling or links). It isn't linked from anywhere in the site and can be safely deleted before submission.
- All images are custom-made SVG illustrations/placeholders stored in `images/`, each with descriptive `alt` text.
- All seven site pages (`index`, `about`, `services`, `login`, `register`, `payment`, `legal`) share the single `css/index.css` stylesheet — shared rules like the navbar, footer and buttons are defined once rather than duplicated per page.
- Logo mark (`images/logo.svg`) is an original SVG design, not a third-party asset.

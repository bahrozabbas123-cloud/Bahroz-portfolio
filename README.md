# Bahroz Abbas — Portfolio

A scroll-driven personal portfolio for **Bahroz Abbas**, a frontend-focused web developer and BS Computer Science student at Quaid-i-Azam University, Islamabad (expected 2028).

The concept: **a portfolio that assembles itself as you scroll.** Sections build piece by piece, like the inside of a mechanical watch being revealed, and settle into a clean, readable final state.

<!-- Add a preview image or GIF here, e.g. ![Preview](./preview.png) -->
DEPLOYED PROJECT
https://bahrozportfolio.vercel.app/

## Features

- **Hero:** stacked, oversized name. It loads clean, then splits, scales and separates as you scroll, while technical tags and lines drift outward.
- **Animated aura background:** four large blurred colour layers on a `#faf8f2` base, using `mix-blend-mode: multiply`. They drift slowly, and their colours shift section by section as you scroll.
- **Depth layers:** aura, subtle grain, technical grid, a few light particles, content, and a soft cursor light (desktop only).
- **Smooth scrolling:** Lenis, synced with GSAP ScrollTrigger.
- **Sections:** About, Skills, Selected Work, Experience, Education, GitHub activity, Contact.
- **Project showcases:** real screenshots of NexaUI and EduCore LMS, revealed with a mask, with layered parallax and 3D tilt on hover. A set of small UI pieces travels from the NexaUI frame to the EduCore frame between the two.
- **Micro-interactions:** magnetic buttons, letter parallax in the name, underline reveals, section labels and a thin scroll progress line.
- **Responsive:** lighter blur, fewer particles, no cursor effects and shorter pinned scroll on mobile.
- **Accessible:** semantic HTML, visible focus states, a skip link, and full support for `prefers-reduced-motion` (content stays fully visible with motion removed).

## Projects shown

| Project | Description | Links |
| --- | --- | --- |
| **NexaUI** | Modern SaaS dashboard built with Next.js and TypeScript | [GitHub](https://github.com/bahrozabbas123-cloud/nexa-ui) · [Live](https://nexa-ui-nine.vercel.app) |
| **EduCore LMS** | Learning platform frontend (roles, dashboards, assignments, certificates) | [GitHub](https://github.com/bahrozabbas123-cloud/educore-lms-frontend) · [Live](https://educore-lms-frontend1.vercel.app) |
| **PrivacySearch** | Privacy-focused search engine project based on a Whoogle-based architecture | [GitHub](https://github.com/bahrozabbas123-cloud/privacy-search-engine) |
| **Flycon AI internship** | VisionGuard AI, SafeRide, EduCore LMS, SmartPOS AI | — |

## Tech

- HTML, CSS and vanilla JavaScript in a single `index.html`
- [GSAP](https://gsap.com) 3.12.5 and ScrollTrigger (cdnjs)
- [Lenis](https://lenis.darkroom.engineering) 1.1.13 for smooth scrolling (jsDelivr)
- Google Fonts: Bricolage Grotesque
- Project screenshots are embedded in the page as WebP data URIs, so the site is self-contained

## Run locally

No build step is needed.

```bash
git clone <your-repo-url>
cd <your-repo-folder>

# Option 1: open index.html in your browser
# Option 2: serve it locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

An internet connection is needed for the GSAP, Lenis and font CDNs.

## Deploy

It's a static site, so it works on any static host:

- **GitHub Pages:** Settings → Pages → deploy from the main branch, root folder.
- **Vercel or Netlify:** import the repo with no build command; the output is the repo root.

## Customise

- **Text and links:** edit the HTML in `index.html` (search for the section `id`s: `home`, `about`, `skills`, `projects`, `experience`, `education`, `activity`, `contact`).
- **Colours:** change the CSS variables in `:root` (`--bg`, `--fg`, `--acc`) and the aura palette array (`pal`) in the script.
- **Project screenshots:** replace the `src` of the `<img>` inside each `.frame.shot`, either with a file path (for example `projects/nexa-ui.png`) or a new data URI.
- **Email:** the contact section currently links to LinkedIn and GitHub. Add an `mailto:` button when you want one.

## Performance notes

- Animations use `transform` and `opacity`, with `will-change` only on the moving layers.
- The particle canvas pauses when the tab is hidden, and uses fewer particles on mobile.
- Scroll effects share ScrollTrigger and one Lenis loop rather than separate scroll handlers.

## Contact

- GitHub: [bahrozabbas123-cloud](https://github.com/bahrozabbas123-cloud)
- LinkedIn: [bahroz-khan-42459a336](https://linkedin.com/in/bahroz-khan-42459a336)

© 2026 Bahroz Abbas

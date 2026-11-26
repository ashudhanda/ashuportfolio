# 🎬 Ashu's Portfolio

My personal portfolio — an immersive, scroll-driven website with 3D motion, glassmorphism UI and custom animations.

## ✨ Features

- Scroll-driven storytelling with smooth animations
- 3D motion effects and depth
- Glassmorphism UI design
- Custom interactions and transitions
- Sound toggle — mute the WebAudio click pop (bottom left)
- Reduced motion — CSS animation and smooth scrolling switch off under `prefers-reduced-motion`
- Skip link — the first Tab stop jumps straight to the main content and moves keyboard focus there
- Mobile menu — below 820px the nav collapses to a toggle button (Escape closes it); body scroll locks while it is open, and it closes on resize past 820px
- In-page anchors — nav and hero links scroll smoothly through Lenis (native smooth scroll when Lenis is off) and land below the fixed nav; Back to the plain URL scrolls back to the top
- Back to top — scrolls through Lenis when it is running, so it never fights the smooth-scroll loop (native smooth scroll otherwise)
- Favicon + `og:url` — inline SVG favicon and the canonical URL of the live GitHub Pages site
- JSON-LD — `Person` structured data (name, role, Chitkara affiliation, LinkedIn/Instagram/GitHub profiles)
- Nav scroll-spy — the link to the section in view carries `aria-current`, including the Let's talk link to the contact section
- Anchor hash sync — clicking a nav/hero link updates the URL hash, so sections are deep-linkable and Back works
- Scroll indicator — starts clear of the fixed sound button and its "Sound" label (`left: max(5vw, 150px)`); hidden below 820px, where it printed over the button
- Project tilt — the mock window inside each project card tilts with the mouse; the card itself keeps its scroll parallax

## 🛠 Tech Stack

- **HTML5** — structure
- **CSS3** — glassmorphism styling and layout
- **JavaScript** — interactivity
- **GSAP** — scroll-based and timeline animations

## 📄 What's on the page

- **Hero** — full-screen intro over `assets/welcome.mp4`, with a fallback panel if the video can't play
- **Name reveal** — large animated name section
- **About** — short bio, plus Frontend / Web Animation / UI-UX / AI Tools tags
- **Skills** — horizontal-scrolling track of five cards (Frontend, Programming, Design, AI & Prompting, Tools)
- **Projects** — three mock-window showcases: Animated Portfolio, Automation Toolkit (Python), Console Utilities (C). The Animated Portfolio card links to this repo; the other two have no live link yet, so their buttons read Coming soon
- **Journey** — education timeline, ending in the current B.E. CSE run at Chitkara University
- **Contact** — email, LinkedIn, and Instagram links

## 🎬 Animation

No build step — everything runs from the single `index.html`:

- **GSAP + ScrollTrigger** — scroll reveals, the skills-track pin, the timeline fill, and the snake path that draws down the page as you scroll
- **Lenis** — smooth scrolling, wired into ScrollTrigger
- **Custom cursor** — a blend-difference ring + dot that follows the mouse
- **Click sound** — a short WebAudio pop on click, no audio files needed; mute it with the sound toggle (bottom left)

## ♿ Accessibility

- **No-JS fallback** — the loader overlay is removed when JavaScript is off, so the page stays readable
- **Reduced motion** — CSS animation and smooth scrolling switch off under `prefers-reduced-motion`, and the timed GSAP intro/enter animations, the orb parallax and the scroll-velocity skew are skipped too (scroll-linked motion follows the scroll position); back-to-top also scrolls instantly instead of smoothly
- **Focus** — keyboard users get a visible accent outline (`:focus-visible`) instead of the browser default
- **Touch devices** — the custom cursor ring/dot are hidden and the native pointer returns (they used to sit frozen mid-screen, since they only move on mousemove); the cursor animation loop does not even start on coarse pointers
- **Unmute button** — exposes its state as an accessible label (Unmute video / Mute video) instead of emoji alone
- **Landmarks** — page sections sit inside a `<main>` landmark; the nav is labelled
- **Keyboard** — back-to-top is a real button, so Enter/Space work without extra handlers; pressing Tab never unmutes the hero video (keyboard users unmute with the Unmute button)
- **Mobile menu** — the toggle button reports `aria-expanded`, closes when a link is tapped or Escape is pressed, and returns focus to the toggle; body scroll locks while it is open, and it closes on resize past 820px
- **Decorative numbers** — the large background numerals on the skill cards are hidden from assistive tech (the visible `01`–`05` labels already carry the number)

## 🚀 Run locally

GSAP + Lenis load from CDNs, so an internet connection is needed for the animations.

```bash
git clone https://github.com/ashudhanda/ashuportfolio.git
cd ashuportfolio
# open index.html in your browser
```

---

Built with ❤️ by [Ashu Dhanda](https://github.com/ashudhanda)

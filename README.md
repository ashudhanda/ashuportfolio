# 🎬 Ashu's Portfolio

My personal portfolio — an immersive, scroll-driven website with 3D motion, glassmorphism UI and custom animations.

## ✨ Features

- Scroll-driven storytelling with smooth animations
- 3D motion effects and depth
- Glassmorphism UI design
- Custom interactions and transitions
- Sound toggle — mute the WebAudio click pop (bottom left)
- Reduced motion — CSS animation and smooth scrolling switch off under `prefers-reduced-motion`

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
- **Projects** — three mock-window showcases: Animated Portfolio, Automation Toolkit (Python), Console Utilities (C)
- **Journey** — education timeline, ending in the current B.E. CSE run at Chitkara University
- **Contact** — email, LinkedIn, and Instagram links

## 🎬 Animation

No build step — everything runs from the single `index.html`:

- **GSAP + ScrollTrigger** — scroll reveals, the skills-track pin, the timeline fill, and the snake path that draws down the page as you scroll
- **Lenis** — smooth scrolling, wired into ScrollTrigger
- **Custom cursor** — a blend-difference ring + dot that follows the mouse
- **Click sound** — a short WebAudio pop on click, no audio files needed; mute it with the sound toggle (bottom left)

## 🚀 Run locally

```bash
git clone https://github.com/ashudhanda/ashuportfolio.git
cd ashuportfolio
# open index.html in your browser
```

---

Built with ❤️ by [Ashu Dhanda](https://github.com/ashudhanda)

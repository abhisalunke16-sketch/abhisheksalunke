# abhisheksalunke.github.io

Personal portfolio website built as a single HTML file. No frameworks, no build step, no dependencies — just HTML, CSS, and vanilla JavaScript.

---

## What's on the page

- **Bio** — short introduction and what I do outside work
- **NASA Astronomy Picture of the Day** — live feed, updates automatically every day via the NASA APOD API
- **Where I work** — current and past roles
- **Find me** — links to LinkedIn, GitHub, Medium, and Instagram
- **Want to play?** — two interactive games (Sorting Race and Gravity Simulator) launched via an in-page overlay

---

## File structure

```
index.html    — the entire site, one file
README.md     — this file
```

---

## How to deploy on GitHub Pages

1. Create a new repository named `yourusername.github.io`
2. Upload `index.html` to the root of the repo
3. Go to **Settings → Pages**
4. Set source to the `main` branch, root folder
5. Save — your site will be live at `https://yourusername.github.io` within a minute

---

## NASA APOD API key

The site uses the NASA APOD API to load today's astronomy image. A free API key is required for production use.

**To get a key:**

1. Go to [api.nasa.gov](https://api.nasa.gov)
2. Fill in your name and email
3. A key will be emailed to you instantly

**To update the key:**

Open `index.html` and find this line:

```js
const API_KEY = 'your_key_here';
```

Replace the value inside the quotes with your new key.

The `DEMO_KEY` placeholder works for testing but has strict rate limits (30 requests per hour). Use your own key in production.

---

## Games

Two games are available via the "Want to play?" button. Both run entirely in the browser with no external dependencies.

**Sorting race** — bubble sort, merge sort, and quicksort race to sort the same shuffled array of 20 numbers. A podium appears when the race finishes.

**Gravity simulator** — click to spawn particles that attract each other via inverse-square gravity. Particles leave trails and bounce off walls. Hit Burst to spawn a ring of 12 particles at once.

---

## Customisation

All content is in plain HTML — no templating, no CMS. To update anything:

- **Bio text** — find the `.bio` paragraph near the top of `<body>`
- **Job history** — find the `<!-- WHERE I WORK -->` comment
- **Social links** — find the `<!-- SOCIALS -->` comment, update the `href` values
- **NASA key** — find `const API_KEY` in the `<script>` block
- **Footer text** — find `<!-- FOOTER -->` near the bottom of `<body>`

---

## Built with

- HTML5 Canvas (games and APOD image rendering)
- NASA APOD API (`api.nasa.gov`)
- ipwho.is (visitor location, no key required)
- Google Fonts — JetBrains Mono
- No libraries, no frameworks, no build tools

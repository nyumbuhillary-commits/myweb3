# Hillary N. Nyumbu — ICT251 Interactive Personal Website

Live site: https://YOUR-RENDER-URL.onrender.com (update after deployment)
Repository: https://github.com/YOUR-USERNAME/myweb (update with your repo link)

## About this project

Personal student portfolio for ICT251 Web Technologies at Mulungushi University.
Builds on my Activity 2 site by adding a Skills/Projects section and four
JavaScript features, then deploying the static site to Render.

## Project structure

```
myweb/
├── index.html
├── css/
│   └── styles.css
├── js/
│   └── script.js
├── images/
│   ├── image-1.jpg
│   ├── image-2.jpg
│   └── image-3.jpg
├── videos/
│   ├── video.mp4
│   └── voice.mp3
└── README.md
```

## The four JavaScript features (in js/script.js)

1. **Contact form validation and preview (compulsory).** On submit, the script
   rejects a blank or whitespace-only name/message and a badly formatted email,
   showing an error message next to each field. When everything is valid it
   builds a summary on the page with `textContent` (never `innerHTML` for user
   text) that clearly states the data was *validated, not sent*.
   `event.preventDefault()` keeps the submission local.
2. **Expandable project/skill cards.** Each card in "My Skills & Projects" has
   a "Show details / Hide details" button that toggles its details and updates
   `aria-expanded`.
3. **Photo gallery viewer.** Previous/Next buttons move through an array of my
   three photos, updating the image, caption and a "Photo X of 3" counter, and
   wrapping around correctly at the first and last photo.
4. **Light/Dark theme switch.** A header button toggles a `dark-theme` class on
   `<body>`, swapping CSS custom properties for background, text and border
   colours. The chosen theme is remembered with `localStorage`.

A bonus mobile navigation toggle shows/hides the nav links on narrow screens.

## How to test each feature

- **Form:** submit empty, then a name of only spaces, then an email like `abc`,
  then valid details — a local preview should appear.
- **Skills cards:** click "Show details" on each card.
- **Gallery:** click Next past photo 3 (loops to photo 1) and Previous past
  photo 1 (loops to photo 3).
- **Theme switch:** click the theme button; reload — the last theme persists.
- **Mobile nav:** resize below ~600px and use the "☰ Menu" button.

## Deployment (GitHub → Render)

1. Pushed this folder to GitHub with `index.html` at the repo root.
2. Render → New → Static Site → connected the repository.
   - Build Command: `echo "No build required"`
   - Publish Directory: `.`
   - Auto-Deploy: enabled on `main`
3. Verified the live `onrender.com` link, then made one small follow-up commit
   to confirm auto-deploy works.

## Sources used

- MDN Web Docs (https://developer.mozilla.org/en-US/docs/Learn_web_development)
  for HTML, CSS and JavaScript reference.

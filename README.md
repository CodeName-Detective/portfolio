# Shri Harsha Adapala — portfolio

Built on the fimbo "Tatum" template (template 1). Three static files, no build step.

Live reference for the original design: https://imfunniee.github.io/template/1/

## Sections

`about` (your LinkedIn summary line) → `experience` (all 8 roles, bullets verbatim
from your profile) → `education` (all 3 degrees) → `contact`.

To add a role, copy a whole `<div class="project">` block in `index.html`.
To add a degree, copy a `<div class="item">` block inside `#education`.

## Worth checking

- **Email** — currently `shriadapala@outlook.com`. Swap for your Buffalo address if you prefer.
- **GitHub link** — points at `github.com/codename-detective`, inferred from your
  portfolio URL rather than read anywhere. Verify it.
- **Hero tagline** — "teaching cars to see." Change it in `index.html` if it's not you.
- **Not included** — your certifications and Top Skills from LinkedIn. Say the word
  and they can go in as a fourth section.

## Swapping the hero image

The hero lives in the `#middle` rule near the top of `index.css` (look for the
`HERO IMAGE` comment). It's currently a Waymo at dawn in fog, from Unsplash,
with a dark blue-black overlay on top so the white tagline stays readable.

To use your own picture, drop the file next to these files and change the
`url(...)` to `url("hero.jpg")`. To make the image darker or lighter, adjust the
two `rgba(2,6,20,...)` alpha values in the same line — higher is darker.

Photo credit: David Yao (@davidsusu_) on Unsplash.

The coral gradient used on your name, the section headings and the footer link is
`linear-gradient(to left, #FF416C 0%, #FF4B2B 100%)` — it appears in three
places in `index.css` if you want to reshade it.

## Making the contact form actually send

The form is inert until you point it at a service. Easiest is
[Formspree](https://formspree.io): sign up, create a form, then set

```html
<form action="https://formspree.io/f/YOUR_ID" method="POST">
```

## Previewing locally

```bash
cd path/to/this/folder
python3 -m http.server 8000
# then open http://localhost:8000
```

## Publishing

Three static files — GitHub Pages (push to a repo, Settings → Pages), Netlify,
or Vercel all work with no build step.

Original template: [fimbo](https://github.com/imfunniee/fimbo) by imfunniee (MIT).

# Md Mehtabul Islam — Portfolio

A one-page, responsive portfolio built with plain HTML, CSS and JavaScript (no frameworks, no build step).

```
mehtab-portfolio/
├── index.html                 ← all the text content lives here
├── css/style.css              ← colours, fonts, layout
├── js/main.js                 ← menu, scroll spy, animations, gallery, contact form
└── assets/
    ├── Md_Mehtabul_Islam_Resume.pdf   ← the "Download CV" button
    └── images/
        ├── profile.jpg, about.jpg, og-image.jpg, favicon.svg
        ├── logos/      bracu.png, auc.png, auhs.png
        ├── projects/   mushroom-classification.jpg, gray-code-converter.jpg
        ├── leadership/ bizbee.jpg, kushiara-house.jpg, debate-club.jpg, science-club.jpg
        ├── sports/     football.jpg, badminton.jpg, marathon.jpg
        └── gallery/    gallery-01.jpg … gallery-08.jpg
```

## 1. Add your own photos (easiest way)

Every picture on the site is a green placeholder that shows its **own file name**.
To swap one, save your photo with **exactly the same name** into the same folder
(overwrite the placeholder). Nothing in the code needs to change.

| File | Where it shows | Best shape |
|---|---|---|
| `profile.jpg` | Hero portrait | Portrait, 800 × 1000 |
| `about.jpg` | About section | Portrait, 900 × 1100 |
| `logos/*.png` | Education timeline | Square, 200 × 200 |
| `projects/*.jpg` | Project cards | Landscape, 1200 × 750 |
| `leadership/*.jpg` | Club cards | Landscape, 900 × 600 |
| `sports/*.jpg` | Sports cards | Landscape, 900 × 650 |
| `gallery/gallery-01…08.jpg` | Gallery grid | Any (cropped automatically) |
| `og-image.jpg` | Preview when the link is shared | 1200 × 630 |

Tips
- Keep each photo under ~300 KB so the site stays fast (use squoosh.app or tinypng.com to compress).
- If your photo is a `.png` or `.jpeg`, either rename it to `.jpg` after converting, or change the file name in `index.html`.
- File names on GitHub Pages are **case-sensitive**: `Profile.JPG` is not the same as `profile.jpg`.

## 2. Edit text

Open `index.html` in VS Code and search for `EDIT:` comments. They mark the places you will most likely change:
- LinkedIn link (`your-linkedin-id`) — or delete those lines
- Project links (Code / Notebook / Demo video)
- Gallery captions (`data-caption="..."`) and alt text
- To add a project, copy one `<article class="project-card">…</article>` block

The rotating hero phrases are in `js/main.js` (search `roles`).
Colours are at the top of `css/style.css` (`:root { ... }`).

## 3. Preview locally

Just double-click `index.html`, or in VS Code use the **Live Server** extension.

## 4. Publish on GitHub Pages

1. Create a new repository on GitHub. For the address `https://mehtabul-islam.github.io/`
   name it exactly **`Mehtabul-Islam.github.io`**. (Any other name gives `https://mehtabul-islam.github.io/<repo-name>/`.)
2. Upload everything **inside** the `mehtab-portfolio` folder (so `index.html` sits at the top level of the repo).
   - Web: *Add file → Upload files*, drag the files and folders in, *Commit changes*.
   - Or with Git:
     ```bash
     cd mehtab-portfolio
     git init
     git add .
     git commit -m "First version of portfolio"
     git branch -M main
     git remote add origin https://github.com/Mehtabul-Islam/Mehtabul-Islam.github.io.git
     git push -u origin main
     ```
3. In the repo go to **Settings → Pages**, set *Source* to **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
4. Wait a minute or two and open the URL GitHub shows you.

To update the site later, replace files and commit again; Pages republishes automatically.

## Features
- Sticky navbar with smooth scrolling and the current section highlighted
- Hamburger menu on tablets and phones
- Light / dark theme toggle (remembered per visitor)
- Scroll-in animations, counting stats, animated language and running bars (all switched off for visitors who prefer reduced motion)
- Gallery lightbox with keyboard arrows and swipe
- Contact form that opens the visitor's email app (no server needed)
- Download CV button

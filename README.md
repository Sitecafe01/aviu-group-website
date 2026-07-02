# Aviu Group Website — File Guide

Design aur content bilkul same hai jaisa pehle tha — bas file 3 hisso me baant di hai taaki edit karna aasan ho.

## Files
- **index.html** — sirf page ka content/structure (text, sections, form). Isi file me text change karoge.
- **styles.css** — poora design (colors, fonts, spacing, layout). Isi file me look-and-feel change karoge.
- **script.js** — scroll-in animation ka JS.
- **images/** — apni images yahan daalo.

Teeno files same folder me honi chahiye — `index.html` andar hi `styles.css` aur `script.js` ko link kiya gaya hai (`<link rel="stylesheet" href="styles.css">` aur `<script src="script.js">`), isliye folder structure mat badalna.

## Hero image already wired
`styles.css` me `.site-plan` class ko already is tarah set kar diya hai:
```css
.site-plan{
  background: url('images/hero-site.jpg') center/cover no-repeat;
  background-color:var(--ink);
  ...
}
```
Matlab bas apni image ka naam **hero-site.jpg** rakh ke `images` folder me daal do — turant black box ki jagah image dikhne lagegi. Agar image file na mile, to purana dark background hi dikhega (design nahi tootega).

Agar image ka naam kuch aur rakhna hai, to `styles.css` me `url('images/hero-site.jpg')` wali line me sirf naam change kar dena.

## Content kaise change karein
- Text/headings: `index.html` me directly edit karo.
- Colors/fonts/spacing: `styles.css` ke top pe `:root{ }` wale variables (`--ink`, `--brass`, etc.) change karo — poori site me automatically apply ho jayega.
- Project cards, contact details, form fields: `index.html` me respective `<section>` dhundo (`id="projects"`, `id="contact"` etc.) aur edit karo.

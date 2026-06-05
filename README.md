# Kishor weds Ruthika — 24 June 2026

Luxury cream-and-gold temple wedding invitation. Cinematic temple-door loader, hand-illustrated section backgrounds, live countdown, WhatsApp RSVP, and Devanagari sacred typography.

---

## 📂 Folder structure

Your repo should look like this:

```
your-wedding-repo/
├── index.html
├── README.md
└── images/
    ├── door.png             ← the loader temple doors
    ├── bg-hero.png          ← hero background (lamps + tilak)
    ├── bg-invocation.png    ← Ganesha section background
    ├── bg-invitation.png    ← invitation card background
    ├── bg-muhurtham.png     ← muhurtham section background
    └── bg-couple.png        ← bride & groom section background
```

**Keep the images folder exactly as named** — the HTML references these specific filenames.

---

## 🚀 Deploy on GitHub Pages (step by step)

1. Sign in to [github.com](https://github.com), click **+** → **New repository**.
2. Name it `wedding-invite` (or anything lowercase, no spaces). Make it **Public**. Check **"Add a README file"**. Click **Create repository**.
3. Click **Add file → Upload files**. Drag in `index.html`.
4. Click **Add file → Create new file**. In the filename, type `images/.gitkeep` (this creates the folder). Commit.
5. Click into the `images` folder. Click **Add file → Upload files**. Drag in all 6 images. Commit.
6. Go to **Settings → Pages**. Source: **Deploy from a branch**, Branch: **main**, Folder: **/ (root)**. Save.
7. Wait ~1 minute, refresh — your live URL appears at the top: `https://<your-username>.github.io/wedding-invite/`

Paste that URL into WhatsApp — the preview card uses the hero image automatically.

---

## ✏️ Customizing details

Open `index.html` in any editor (VS Code, Notepad, even GitHub's web editor).

### Couple photos
Find the "Meet the Bride & Groom" section, look for `<!-- Replace with -->` comments. Upload `kishor.jpg` and `ruthika.jpg` into your `images` folder, then change:
```html
<div class="portrait-inner">K</div>
```
to:
```html
<div class="portrait-inner"><img src="images/kishor.jpg" alt="Kishor"></div>
```
(Same for Ruthika, with `images/ruthika.jpg`.)

### Wedding date for the live countdown
Near the bottom of the file in `<script>`, find:
```js
const WEDDING_DATE = new Date('2026-06-24T12:29:00+05:30').getTime();
```
This is already set to **24 June 2026, 12:29 PM IST**. Change if needed.

### WhatsApp RSVP number
Search for `917249776066` (your number with country code 91). Already set correctly. If you want a different number, update both that link and the `tel:+917249776066` link.

### Background music
The audio toggle (top-right) plays a sample track. To use your own:
1. Upload `music.mp3` to the repo root.
2. Find `<source src="https://...` and change to `<source src="music.mp3" type="audio/mpeg">`.

### Colors
Top of the `<style>` block, the `:root` section has all colors as CSS variables. Tweak `--gold-rich`, `--maroon`, `--kumkum` to taste.

---

## 🎨 What's included

- **Temple-door loader** — your actual door image splits and slides open on load
- **Cream & gold aesthetic** — matching the hand-illustrated backgrounds you provided
- **Devanagari sacred text** — "ॐ श्री गणेशाय नमः" rendered in proper Sanskrit font
- **Five image-backed sections** — hero, invocation, invitation, muhurtham, couple
- **Live countdown** — auto-updates to 24 June 2026, 12:29 PM IST
- **WhatsApp + Call RSVP** — both routed to +91 72497 76066
- **Floating petals** — pink lotus, marigold, and jasmine mix on cream
- **Fully responsive** — looks great in WhatsApp browser, mobile, desktop
- **Open Graph preview** — clean WhatsApp share card

---

## 💡 Tips

- The image backgrounds are designed for portrait mobile screens. On desktop, they're centered with cream filling the sides — keeps the artwork from stretching.
- If you want to swap any image, replace the file in `/images/` with one of the same name. Keep aspect ratios portrait (around 3:4 or 9:16) for best results.
- After any edit, just commit/save in GitHub — the live site refreshes in 30-60 seconds.

✦ With love · 24 June 2026 · #KISHORWEDSRUTHIKA ✦

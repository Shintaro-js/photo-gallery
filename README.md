# Photography Portfolio

A minimal, elegant photo gallery website.

## Setup

### 1. Add your photos
Copy your image files into the `photos/` folder.
Supported formats: JPG, PNG, WEBP

### 2. Register your photos
Open `gallery.js` and add each photo to the `photos` array:

```js
const photos = [
  { file: "sunset.jpg",    title: "Golden hour",   location: "Sydney, AU" },
  { file: "portrait.jpg",  title: "Morning light"                         },
  { file: "landscape.jpg"                                                  },
];
```

- `file` — the filename (required)
- `title` — caption shown on hover and in the lightbox (optional)
- `location` — shown below the title on hover (optional)

### 3. Customise the site
Open `index.html` and update:
- **Line 103** — your name in the header (`Your Name Photography`)
- **Line 116** — hero subtitle text
- **Line 136** — About section quote and bio
- **Line 137** — your city and email address
- **Line 142** — footer name and year

### 4. Deploy (free on Netlify)
1. Go to [netlify.com](https://netlify.com) and sign up (free)
2. Click **"Add new site" → "Deploy manually"**
3. Drag your entire `photo-gallery` folder onto the page
4. Done — your site is live!

## Adding new photos

1. Drop new photos into the `photos/` folder
2. Resize them for web (keeps files small, loads fast):
   ```
   sips --resampleWidth 2000 photos/YOURPHOTO.jpg
   ```
   Or to resize all photos at once:
   ```
   sips --resampleWidth 2000 photos/*.jpg
   ```
3. Add each photo to `gallery.js`
4. Commit and push — Netlify will auto-deploy:
   ```
   git add .
   git commit -m "add new photos"
   git push
   ```

## Keyboard shortcuts
- `←` / `→` — navigate photos in lightbox
- `Esc` — close lightbox

## File structure
```
photo-gallery/
├── index.html      ← main site
├── gallery.js      ← your photo list (edit this)
├── README.md       ← this file
└── photos/
    ├── photo1.jpg
    ├── photo2.jpg
    └── ...
```

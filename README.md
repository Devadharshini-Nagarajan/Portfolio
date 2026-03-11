# 🌿 Your Portfolio — Astro

A warm, personal developer portfolio built with [Astro](https://astro.build).

## 🎨 Design

- **Palette:** Cream · Terracotta · Deep Charcoal
- **Fonts:** Playfair Display (headings) · DM Sans (body) · JetBrains Mono (code/labels)
- **Vibe:** Warm, personal, crafted — not corporate

## 🚀 Getting Started

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build

# Preview production build
npm run preview
```

## 📁 Structure

```
src/
├── components/
│   ├── Nav.astro         # Fixed navigation
│   ├── Hero.astro        # Hero + status card
│   ├── About.astro       # Summary / about me
│   ├── Skills.astro      # Skills grid
│   ├── Experience.astro  # Timeline
│   ├── Projects.astro    # Projects (image/video/links)
│   └── Contact.astro     # Contact form + footer
├── layouts/
│   └── Layout.astro      # Base HTML, fonts, CSS vars
└── pages/
    └── index.astro       # Assembles all sections
```

## ✏️ Customization

### Personal Info
- Edit `src/components/Hero.astro` — name, tagline, meta
- Edit `src/components/About.astro` — your summary & quote
- Edit `src/components/Nav.astro` — logo initials

### Skills
Edit the `skillGroups` array in `src/components/Skills.astro`

### Experience
Edit the `experiences` array in `src/components/Experience.astro`

### Projects
Edit the `projects` array in `src/components/Projects.astro`

Each project supports:
- `image` — path to image in `/public` folder
- `video` — path to `.mp4` file OR a YouTube URL
- `liveUrl` — live site link
- `githubUrl` — GitHub repo link

### Avatar / Photo
In `Hero.astro`, replace the `.avatar-placeholder` div with:
```html
<img src="/your-photo.jpg" alt="Your Name" class="avatar-img" style="width:100%;height:100%;border-radius:50%;object-fit:cover;" />
```
Place your photo in the `/public` folder.

### Contact Form
The form is ready to wire up. In `Contact.astro`, replace the simulated submit with your preferred service:

**Formspree** (easiest):
```html
<form action="https://formspree.io/f/YOUR_KEY" method="POST">
```

**Netlify Forms**: Add `data-netlify="true"` to the `<form>` tag.

## 🌐 Deployment

**Vercel (recommended):**
```bash
npx vercel
```

**Netlify:**
```bash
npx netlify deploy --prod --dir=dist
```

**GitHub Pages:** See [Astro docs](https://docs.astro.build/en/guides/deploy/github/)

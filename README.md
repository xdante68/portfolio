# CS Student Portfolio 🚀

A modern, dark-themed portfolio website built with **Next.js 14**, **Tailwind CSS**, **Framer Motion**, and **TypeScript**. Glassmorphism UI, smooth animations, and a fully data-driven architecture.

## ✨ Features

- **Dark Mode Default** with glassmorphism cards & gradient accents
- **Animated Hero** with typing effect & floating particles
- **8 Sections**: Hero, About, Education, Organization, Skills, Projects, Certificates, Gallery
- **Project Detail Pages** with `/projects/[slug]` routing
- **Category Filtering** on Skills, Projects, Certificates, Gallery
- **Command Palette** (⌘K / Ctrl+K) for quick navigation
- **Lightbox** for Gallery & Project screenshots
- **Certificate Modal** with verify & download actions
- **Animated Counters, Progress Bars, Scroll Indicators**
- **Responsive** — mobile, tablet, desktop
- **Reading Progress Bar** at the top
- **Back to Top** button
- **Creative 404 Page** with terminal theme
- **SEO Optimized** with full metadata

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| Next.js 14 (App Router) | Framework |
| TypeScript | Type safety |
| Tailwind CSS v4 | Styling |
| Framer Motion | Animations |
| Lucide React | Icons |

## 📁 Project Structure

```
├── app/
│   ├── layout.tsx          # Root layout
│   ├── page.tsx            # Home (all sections)
│   ├── not-found.tsx       # 404 page
│   └── projects/[slug]/    # Project detail pages
├── components/
│   ├── layout/             # Navbar, Footer
│   ├── sections/           # Hero, About, Education, etc.
│   └── ui/                 # Reusable UI components
├── data/                   # All content data files
└── types/                  # TypeScript types
```

## 🚀 Quick Start

```bash
# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build
```

## ✏️ Customizing Your Data

All content is in the `/data/` directory. **You never need to touch any component files** to update your content.

### Profile (`data/profile.ts`)
Update your name, title, bio, social links, etc.

### Education (`data/education.ts`)
Add/edit your educational history. Each entry has institution, degree, GPA, highlights.

### Organizations (`data/organizations.ts`)
Add your organizational experiences. Types: `himpunan`, `ukm`, `komunitas`, `external`.

### Skills (`data/skills.ts`)
Add skills with icons from [devicons CDN](https://devicon.dev/). Categories: `language`, `framework`, `database`, `tools`. Set `currentlyLearning: true` for skills you're learning.

### Projects (`data/projects.ts`)
Add projects with:
- `slug` — used for the URL `/projects/[slug]`
- `featured: true` — marks as featured
- `category` — `web`, `mobile`, `ml`, `iot`, `other`
- `status` — `completed`, `ongoing`, `archived`

### Certificates (`data/certificates.ts`)
Add certificates with issuer info, credential URLs, and optional PDF files.

### Gallery (`data/gallery.ts`)
Add photos with captions, dates, locations, and categories.

## 🖼️ Adding Images

Place images in the `/public/images/` directory:

```
public/
├── images/
│   ├── profile/photo.jpg        # Your profile photo
│   ├── projects/*.jpg           # Project thumbnails
│   ├── certificates/*.jpg       # Certificate images
│   ├── education/*.png          # Institution logos
│   ├── organizations/*.png      # Org logos
│   └── gallery/*.jpg            # Gallery photos
└── cv/cv.pdf                    # Your CV/resume
```

## 🎨 Customizing Theme

Edit CSS variables in `app/globals.css`:

```css
:root {
  --accent-cyan: #00f0ff;     /* Primary accent */
  --accent-purple: #7c3aed;   /* Secondary accent */
  --accent-blue: #06b6d4;     /* Tertiary accent */
  --bg-dark: #0a0a0f;         /* Background */
}
```

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| ⌘K / Ctrl+K | Open command palette |
| ↑ ↓ | Navigate command palette |
| Enter | Select item |
| Esc | Close modal / palette |
| ← → | Navigate lightbox images |

## 📦 Deploy

Deploy to Vercel:

```bash
npm run build
npx vercel
```

Or push to GitHub and connect to [Vercel](https://vercel.com) for auto-deploys.

## 📝 License

MIT — feel free to use this for your own portfolio!

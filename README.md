# Kanav Singhal — Personal Portfolio

A Marvel-inspired personal portfolio site built with [Astro](https://astro.build), designed to grow from a student portfolio into a full professional presence.

## ✨ Features

- Marvel-inspired design (crimson, gold, near-black) with arc reactor animation
- Fully static — zero JS bundle shipped to the user by default
- 100% responsive (mobile-first)
- Sections: Hero · About · Achievements · Interests · Journal · Contact
- Ready for Cloudflare Pages free hosting
- GitHub Actions auto-deploy on every push

---

## 🚀 Getting Started (Local Dev)

**Prerequisites:** Node.js 18+

```bash
# 1. Install dependencies
npm install

# 2. Start the dev server
npm run dev
# → Open http://localhost:4321

# 3. Build for production
npm run build

# 4. Preview the production build
npm run preview
```

---

## 📦 Deploy to GitHub + Cloudflare Pages

### Step 1 — Push to GitHub

```bash
git init
git add .
git commit -m "Initial commit — Kanav's portfolio"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/kanav-singhal.git
git push -u origin main
```

### Step 2 — Connect to Cloudflare Pages (Free)

1. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages** → **Create**
2. Connect your GitHub account and select the `kanav-singhal` repo
3. Set these build settings:
   - **Framework preset:** Astro
   - **Build command:** `npm run build`
   - **Build output directory:** `dist`
4. Click **Save and Deploy** — that's it! 🎉

### Step 3 — Add your custom domain (e.g. kanavsinghal.com)

In Cloudflare Pages → your project → **Custom domains** → Add domain.
If the domain is registered through Cloudflare, it'll configure DNS automatically.

---

## 🔧 Auto-Deploy via GitHub Actions

For the GitHub Actions workflow (`.github/workflows/deploy.yml`) to work, add these secrets to your GitHub repo under **Settings → Secrets → Actions**:

| Secret name               | Where to find it                                |
|---------------------------|-------------------------------------------------|
| `CLOUDFLARE_API_TOKEN`    | Cloudflare dashboard → My Profile → API Tokens  |
| `CLOUDFLARE_ACCOUNT_ID`   | Cloudflare dashboard → right sidebar            |

> **Alternatively**, skip GitHub Actions entirely. Cloudflare Pages has a built-in Git integration that auto-deploys on every push — no secrets needed. The Actions workflow is optional.

---

## ✏️ Updating Content

All content lives in the component files under `src/components/`:

| File                  | What to edit                            |
|-----------------------|-----------------------------------------|
| `Hero.astro`          | Name, tagline, bio, stats               |
| `About.astro`         | Bio paragraphs, skill levels, details   |
| `Achievements.astro`  | Add/edit achievement cards              |
| `Interests.astro`     | Interests, tags, descriptions           |
| `Journal.astro`       | Blog post previews                      |
| `Contact.astro`       | Email, social links                     |
| `src/styles/global.css` | Colors, fonts, spacing tokens         |

---

## 🎨 Design Tokens (global.css)

| Token           | Value      | Usage               |
|-----------------|------------|---------------------|
| `--crimson`     | `#C0122C`  | Primary accent      |
| `--gold`        | `#E8B84B`  | Secondary accent    |
| `--void`        | `#0A0A0F`  | Page background     |
| `--panel`       | `#111118`  | Cards, nav          |
| `--font-display`| Bebas Neue | Headlines           |
| `--font-body`   | Inter      | Body text           |
| `--font-mono`   | JetBrains Mono | Labels, tags   |

---

Built with 💛 as a birthday gift. Here's to many more chapters, Kanav.

# Camp Digital Site

A modern, responsive website for **camp.digital** — "The social team for brands".

This repository includes two complete, distinct design directions:
1. **Version 1: Spartan Minimalist** (`index.html`) — Sparse, distraction-free aesthetic matching the ethos of `allenmask.com` and `newberncollection.com`, featuring a 2-page smooth slider (Home & Offerings), official Camp Digital CD pennant flag mark, standalone mail icon to `hello@camp.digital`, and Instagram portfolio arrow.
2. **Version 2: Studio Editorial** (`studio.html`) — Rich, comprehensive boutique creative agency experience informed by the `@camp_digital` pitch deck, Canva brand kit, and Instagram feed. Features the 3 core pillars in depth, client roster (Nike, Spotify, Lime, Apple & Airbnb alumni), credo, and visual campaign showcases.

---

## Brand Identity & Core Assets

- **Domain**: [camp.digital](https://camp.digital)
- **Tagline**: *"The social team for brands"*
- **Contact Email**: `hello@camp.digital`
- **Instagram**: [@camp_digital](https://www.instagram.com/camp_digital/)
- **Brand Emblem**: Pennant Flag Mark with CD Cutout (`assets/flag.svg`)
- **Favicon**: `assets/favicon.svg`

### Core Offerings / Service Architecture
1. **Social Media Management** — Full-service orchestration, publishing cadences, community architecture, compounding audience growth.
2. **Creative Development and Production** — Thumb-stopping short-form video/reels, editorial photography, surreal social cinema, multi-channel art direction.
3. **Influencer Campaigns** — Creator scouting, high-affinity talent casting, authentic product seeding, performance activations.
4. **Go-to-Market Strategy** — Launch playbooks, brand re-positioning, paid amplification advisory.

---

## Deployment & Hosting Workflow (GitHub Pages + Squarespace)

### 1. Push to GitHub
Repository: `https://github.com/allenmask/camp.digital.git`

```bash
cd /Users/allenmask/campdigital-site
git remote set-url origin https://github.com/allenmask/camp.digital.git
git push -u origin main
```

### 2. Enable GitHub Pages
1. Go to your repository settings: `https://github.com/allenmask/camp.digital/settings/pages`
2. Under **Build and deployment**:
   - Source: **Deploy from a branch**
   - Branch: `main` / `/ (root)`
   - Click **Save**
3. Under **Custom domain**:
   - Enter: `camp.digital`
   - Click **Save** (verifies the `CNAME` file in this repo)
   - Check **Enforce HTTPS** (once DNS propagates)

---

## Squarespace DNS Configuration for camp.digital

In your Squarespace account:
1. Navigate to **Domains** &rarr; select **camp.digital** &rarr; **DNS Settings**.
2. Add the **4 GitHub Pages Apex A Records**:
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.108.153`
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.109.153`
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.110.153`
   - **Type**: `A` | **Host**: `@` | **Data**: `185.199.111.153`
3. Add the **CNAME Record**:
   - **Type**: `CNAME` | **Host**: `www` | **Data**: `allenmask.github.io.`

---

## Email Forwarding Setup (`hello@camp.digital` -> Gmail)

Squarespace Domains includes free email forwarding:
1. In Squarespace, go to **Domains** &rarr; select **camp.digital**.
2. Click **Email** (or **Email Forwarding** in the sidebar).
3. Click **Add Rule** (or **Add Forward**):
   - **Alias / Forward from**: `hello` (making it `hello@camp.digital`)
   - **Forward to**: your personal Gmail address.
4. Squarespace sends a verification email. Click **Verify** to activate forwarding immediately.

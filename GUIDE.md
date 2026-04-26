# How to Create an Awesome GitHub Profile Like This

> A complete guide to making your GitHub profile stand out with animated headers, GIFs, auto-updating stats, and more.

---

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Create Profile Repository](#1-create-profile-repository)
3. [Animated Header Banner](#2-animated-header-banner)
4. [Typing Animation](#3-typing-animation)
5. [Social Badges](#4-social-badges)
6. [About Me Section with GIF](#5-about-me-section-with-gif)
7. [Tech Stack with Animated Icons](#6-tech-stack-with-animated-icons)
8. [GitHub Stats Cards](#7-github-stats-cards)
9. [Streak Stats](#8-streak-stats)
10. [GitHub Trophies](#9-github-trophies)
11. [Contribution Snake Animation](#10-contribution-snake-animation)
12. [Activity Graph](#11-activity-graph)
13. [Random Dev Quote](#12-random-dev-quote)
14. [Profile Views Counter](#13-profile-views-counter)
15. [Auto-Update Workflow](#14-auto-update-workflow-keep-repo-on-top)
16. [Color Scheme Reference](#color-scheme-reference)
17. [Full File Structure](#full-file-structure)

---

## Prerequisites

- A GitHub account
- Basic knowledge of Markdown and HTML
- That's it! No coding required for most features

---

## 1. Create Profile Repository

GitHub has a **secret feature**: if you create a repository with the **same name as your username**, the `README.md` of that repo will appear on your profile page.

**Steps:**
1. Go to [github.com/new](https://github.com/new)
2. Set Repository name = **your username** (e.g., `xinnxz`)
3. Make it **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

> **Important:** The repo name MUST exactly match your GitHub username.

---

## 2. Animated Header Banner

Uses **[capsule-render](https://github.com/kyechan99/capsule-render)** to generate an animated gradient wave header.

```html
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:6C63FF,25:3F51B5,50:00BCD4,75:26C6DA,100:6C63FF&height=200&section=header&text=YOUR_NAME&fontSize=90&fontColor=ffffff&fontAlignY=30&desc=Your%20Tagline%20Here&descSize=20&descColor=d4e0ff&descAlignY=52&animation=twinkling" width="100%" />
</div>
```

**Parameters to customize:**
| Parameter | Description | Example |
|-----------|-------------|---------|
| `type` | Wave shape | `waving`, `egg`, `shark`, `slice` |
| `color` | Gradient colors (0-100%) | `0:6C63FF,50:00BCD4,100:6C63FF` |
| `height` | Banner height in px | `200` |
| `text` | Main title text | `0xKen` |
| `fontSize` | Title font size | `90` |
| `desc` | Subtitle text (URL encoded) | `Full%20Stack%20Developer` |
| `animation` | Animation type | `twinkling`, `fadeIn`, `scaleIn` |

> **Tip:** Use `%20` for spaces and `%E2%80%A2` for bullet dots (•) in the URL.

For the **footer**, use `section=footer`:
```html
<img src="https://capsule-render.vercel.app/api?type=waving&color=0:6C63FF,25:3F51B5,50:00BCD4,75:26C6DA,100:6C63FF&height=120&section=footer" width="100%" />
```

---

## 3. Typing Animation

Uses **[readme-typing-svg](https://github.com/DenverCoder1/readme-typing-svg)** for an animated typing effect.

```html
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=20&duration=3000&pause=1000&color=6C63FF&center=true&vCenter=true&multiline=true&repeat=true&width=800&height=130&lines=Line+1+text;Line+2+text;Line+3+text;Line+4+text" />
</a>
```

**Key parameters:**
| Parameter | Description |
|-----------|-------------|
| `font` | Font family (`JetBrains+Mono`, `Fira+Code`, etc.) |
| `size` | Font size |
| `color` | Text color (hex without #) |
| `width` / `height` | SVG container dimensions |
| `multiline` | `true` = show all lines stacked, `false` = cycle one at a time |
| `lines` | Lines separated by `;` (use `+` for spaces) |
| `duration` | Typing speed in ms |
| `pause` | Pause between lines in ms |

> **Common issue:** If text gets cut off, increase `width` and `height`.

---

## 4. Social Badges

Uses **[shields.io](https://shields.io/)** to create styled badge links.

```markdown
[![YouTube](https://img.shields.io/badge/YouTube-FF0000?style=for-the-badge&logo=youtube&logoColor=white)](https://youtube.com/YOUR_CHANNEL)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_PROFILE)
[![Instagram](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://instagram.com/YOUR_HANDLE)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge&logo=x&logoColor=white)](https://x.com/YOUR_HANDLE)
[![Portfolio](https://img.shields.io/badge/Portfolio-6C63FF?style=for-the-badge&logo=googlechrome&logoColor=white)](https://YOUR_WEBSITE)
```

**Badge format:**
```
https://img.shields.io/badge/LABEL-COLOR?style=STYLE&logo=LOGO&logoColor=white
```

Find logo names at [simpleicons.org](https://simpleicons.org/).

---

## 5. About Me Section with GIF

A side-by-side layout using HTML `<table>` — code block on the left, GIF on the right.

```html
<table>
  <tr>
    <td width="55%">

<!-- Code block inside table -->
```typescript
const dev: Developer = {
    name: "Your Name",
    roles: ["Full Stack Developer"],
    languages: ["JavaScript", "TypeScript", "Python"],
    motto: "Code it. Ship it. Iterate."
};
```

    </td>
    <td width="45%" align="center">
      <img src="https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif" width="100%" />
    </td>
  </tr>
</table>
```

**Popular coding GIFs from Giphy:**
| GIF | URL |
|-----|-----|
| Man coding | `https://media.giphy.com/media/qgQUggAC3Pfv687qPC/giphy.gif` |
| Laptop code | `https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif` |
| Cat typing | `https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif` |

For bullet point icons, use shields.io colored badges:
```html
<img src="https://img.shields.io/badge/-✦-6C63FF?style=flat-square" height="18"/>
```

---

## 6. Tech Stack with Animated Icons

### Animated Tech GIFs

These are popular animated tech logo GIFs hosted on GitHub:

```html
<img src="https://user-images.githubusercontent.com/74038190/212257454-16e3712e-945a-4ca2-b238-408ad0bf87e6.gif" width="80">
<img src="https://user-images.githubusercontent.com/74038190/212257472-08e52665-c503-4bd9-aa20-f5a4dae769b5.gif" width="80">
<img src="https://user-images.githubusercontent.com/74038190/212257468-1e9a91f1-b626-4baa-b15d-5c385dfa7ed2.gif" width="80">
<img src="https://user-images.githubusercontent.com/74038190/212257465-7ce8d493-cac5-494e-982a-5a9deb852c4b.gif" width="80">
<img src="https://user-images.githubusercontent.com/74038190/212257467-871d32b7-e401-42e8-a166-fcfd7baa4c6b.gif" width="80">
<img src="https://user-images.githubusercontent.com/74038190/212281775-b468df30-4edc-4bf8-a4ee-f52e1aaddc86.gif" width="80">
```

> **Source:** [Anmol-Baranwal/Cool-GIFs-For-GitHub](https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub)

### Skill Icons (Static)

Uses **[skillicons.dev](https://skillicons.dev/)** for beautiful tech stack icons:

```html
<img src="https://skillicons.dev/icons?i=js,ts,react,nodejs,python,php&theme=dark" />
```

Browse all icons at [skillicons.dev](https://skillicons.dev/).

### Category Badges

Use shields.io as section labels:
```html
<img src="https://img.shields.io/badge/-Languages-6C63FF?style=for-the-badge&logoColor=white" />
<img src="https://img.shields.io/badge/-Frameworks-3F51B5?style=for-the-badge&logoColor=white" />
<img src="https://img.shields.io/badge/-Databases-00BCD4?style=for-the-badge&logoColor=white" />
<img src="https://img.shields.io/badge/-Tools-26C6DA?style=for-the-badge&logoColor=white" />
```

---

## 7. GitHub Stats Cards

Uses **[github-readme-stats](https://github.com/anuraghazra/github-readme-stats)**.

```html
<!-- Stats + Top Languages side by side -->
<img src="https://github-readme-stats-eight-theta.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&bg_color=0d1117&title_color=6C63FF&icon_color=6C63FF&text_color=c9d1d9" width="49%" />

<img src="https://github-readme-stats-eight-theta.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=6C63FF&text_color=c9d1d9&langs_count=8" width="49%" />
```

> **Tip:** Using `width="49%"` on both cards makes them sit side-by-side.

---

## 8. Streak Stats

Uses **[github-readme-streak-stats](https://github.com/DenverCoder1/github-readme-streak-stats)**.

```html
<img src="https://github-readme-streak-stats.herokuapp.com/?user=YOUR_USERNAME&theme=tokyonight&hide_border=true&background=0d1117&stroke=6C63FF&ring=6C63FF&fire=FF6B6B&currStreakLabel=6C63FF&sideLabels=c9d1d9&currStreakNum=c9d1d9&dates=8b949e" width="70%" />
```

---

## 9. GitHub Trophies

Uses **[github-profile-trophy](https://github.com/ryo-ma/github-profile-trophy)**.

```html
<img src="https://github-trophies.vercel.app/?username=YOUR_USERNAME&theme=discord&no-frame=true&no-bg=true&column=7&margin-w=10" width="100%" />
```

---

## 10. Contribution Snake Animation

This is the coolest feature — an animated snake that "eats" your contribution graph!

### Step 1: Create `.github/workflows/snake.yml`

```yaml
name: Generate Snake Animation

on:
  schedule:
    - cron: '0 1 * * *'     # Daily at 08:00 WIB
  workflow_dispatch:          # Manual trigger
  push:
    branches: [main]

permissions:
  contents: write

jobs:
  generate-snake:
    runs-on: ubuntu-latest
    steps:
      - name: Generate snake SVG
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: YOUR_USERNAME
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

### Step 2: Display in README

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-snake.svg" />
  <img src="https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_USERNAME/output/github-snake-dark.svg" width="100%" />
</picture>
```

> The `<picture>` tag automatically shows the dark/light version based on the visitor's theme.

---

## 11. Activity Graph

Uses **[github-readme-activity-graph](https://github.com/Ashutosh00710/github-readme-activity-graph)**.

```html
<img src="https://github-readme-activity-graph.vercel.app/graph?username=YOUR_USERNAME&bg_color=0d1117&color=6C63FF&line=6C63FF&point=ffffff&area_color=6C63FF&area=true&hide_border=true&custom_title=Contribution%20Activity" width="100%" />
```

---

## 12. Random Dev Quote

Uses **[github-readme-quotes](https://github.com/PiyushSuthar/github-readme-quotes)**.

```html
<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=tokyonight&border=true" width="70%" />
```

This shows a different programming quote every time the page loads!

---

## 13. Profile Views Counter

Uses **[komarev/github-profile-views-counter](https://github.com/antonkomarev/github-profile-views-counter)**.

```html
<img src="https://komarev.com/ghpvc/?username=YOUR_USERNAME&style=for-the-badge&color=6C63FF&label=PROFILE+VIEWS" />
```

Followers badge:
```html
<img src="https://img.shields.io/github/followers/YOUR_USERNAME?style=for-the-badge&color=6C63FF&labelColor=0d1117" />
```

---

## 14. Auto-Update Workflow (Keep Repo on Top)

This workflow makes a daily commit so your profile repo always appears as "recently updated" at the top of your repositories list.

### Create `.github/workflows/auto-update.yml`

```yaml
name: Auto Update Profile

on:
  schedule:
    - cron: '0 0 * * *'    # Daily at 07:00 WIB
  workflow_dispatch:         # Manual trigger

permissions:
  contents: write

jobs:
  auto-update:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
        with:
          fetch-depth: 0

      - name: Update and commit
        run: |
          node -e "
          const fs = require('fs');
          let data = { totalUpdates: 0, history: [] };
          try { data = JSON.parse(fs.readFileSync('lastUpdated.json', 'utf8')); } catch(e) {}

          const quotes = [
            'Keep pushing forward',
            'Code. Learn. Repeat.',
            'Another day, another commit',
            'Consistency is key',
            'Building something great',
            'Growing every day',
            'Refining the craft',
            'Always learning',
            'Making progress'
          ];

          const quote = quotes[Math.floor(Math.random() * quotes.length)];
          const now = new Date();
          data.lastUpdated = now.toISOString();
          data.totalUpdates = (data.totalUpdates || 0) + 1;
          data.lastQuote = quote;
          data.history = (data.history || []);
          data.history.unshift({ date: now.toISOString().split('T')[0], quote });
          data.history = data.history.slice(0, 30);

          fs.writeFileSync('lastUpdated.json', JSON.stringify(data, null, 2));
          fs.writeFileSync('/tmp/msg.txt', quote);
          "

          # IMPORTANT: Use YOUR email so commits count in YOUR contribution graph!
          git config --local user.email "YOUR_ID+YOUR_USERNAME@users.noreply.github.com"
          git config --local user.name "YOUR_USERNAME"
          git add lastUpdated.json
          COMMIT_MSG=$(cat /tmp/msg.txt)
          if ! git diff --cached --quiet; then
            git commit -m "$COMMIT_MSG"
            git push
          fi
```

> **Critical:** Replace `user.email` with YOUR GitHub noreply email (find it at GitHub → Settings → Emails). If you use `github-actions[bot]`, commits will NOT appear in your contribution graph!

### Create `lastUpdated.json`

```json
{
  "lastUpdated": "",
  "totalUpdates": 0,
  "history": []
}
```

---

## Color Scheme Reference

This profile uses a cohesive **indigo-cyan** color palette:

| Color | Hex | Used For |
|-------|-----|----------|
| Primary Indigo | `#6C63FF` | Main accent, badges, titles |
| Deep Indigo | `#3F51B5` | Secondary badges |
| Cyan | `#00BCD4` | Tertiary badges |
| Light Cyan | `#26C6DA` | Accent details |
| GitHub Dark BG | `#0d1117` | Stats card backgrounds |
| Text Primary | `#c9d1d9` | Main text color |
| Text Secondary | `#8b949e` | Date/subtitle text |
| Fire Red | `#FF6B6B` | Streak fire icon |

---

## Full File Structure

```
your-username/
├── .github/
│   └── workflows/
│       ├── snake.yml          # Snake animation (daily)
│       └── auto-update.yml    # Auto-commit (daily)
├── README.md                  # Your profile README
└── lastUpdated.json           # Auto-updated by workflow
```

---

## Useful Resources

| Resource | URL |
|----------|-----|
| Capsule Render | https://github.com/kyechan99/capsule-render |
| Typing SVG | https://github.com/DenverCoder1/readme-typing-svg |
| Shields.io | https://shields.io |
| Skill Icons | https://skillicons.dev |
| GitHub Stats | https://github.com/anuraghazra/github-readme-stats |
| Streak Stats | https://github.com/DenverCoder1/github-readme-streak-stats |
| Trophies | https://github.com/ryo-ma/github-profile-trophy |
| Snake Animation | https://github.com/Platane/snk |
| Activity Graph | https://github.com/Ashutosh00710/github-readme-activity-graph |
| Dev Quotes | https://github.com/PiyushSuthar/github-readme-quotes |
| Profile Views | https://github.com/antonkomarev/github-profile-views-counter |
| Cool GIFs | https://github.com/Anmol-Baranwal/Cool-GIFs-For-GitHub |
| Simple Icons | https://simpleicons.org |
| Awesome READMEs | https://github.com/abhisheknaiidu/awesome-github-profile-readme |

---

> **Made with passion by [0xKen](https://github.com/xinnxz)**

# ⚡ Raghu Vardhan Venuvanka — Portfolio

> **World-class developer portfolio** for an AI Engineer & Data Scientist.  
> Built with advanced frontend techniques: custom cursor, cinematic loading screen, parallax, scroll-reveal, animated skill bars, a ticker marquee, project filtering, and a full dark-luxury design system.

---

## 🔗 Live Demo

👉 **[venuvankaraghuvardhan-arch.github.io/portfolio](https://venuvankaraghuvardhan-arch.github.io/portfolio/)**

---

## 📸 Preview

| Section | Description |
|---|---|
| **Hero** | Cinematic full-height with parallax name, animated stats, status badge |
| **Ticker** | Infinite marquee of tech stack across violet band |
| **About** | Split layout: rich bio + info cards |
| **Projects** | 10 real GitHub repos, filterable by category, featured card layout |
| **Skills** | Animated skill bars across 3 columns + 4 certification cards |
| **Contact** | Split layout: contact links + live contact form |

---

## 🗂️ Projects Included (All 10 Real GitHub Repos)

| # | Project | Category | Link |
|---|---|---|---|
| 01 | Production RAG with Guardrails | AI / Full-Stack | [GitHub](https://github.com/venuvankaraghuvardhan-arch/Production-RAG-with-Guardrails) |
| 02 | LLM Eval Dashboard | AI / LLM | [GitHub](https://github.com/venuvankaraghuvardhan-arch/LLM-eval-dashboard) |
| 03 | Domain Fine-Tune API | AI / LLM | [GitHub](https://github.com/venuvankaraghuvardhan-arch/Domain-Fine-Tune-API) |
| 04 | Synthetic Data Factory | AI / ML | [GitHub](https://github.com/venuvankaraghuvardhan-arch/Synthetic-Data-Factory) |
| 05 | LLM Router Prompt Gateway | AI / LLM | [GitHub](https://github.com/venuvankaraghuvardhan-arch/-LLM-Router-System-1-vs-System-2-Prompt-Gateway) |
| 06 | WikiMind Knowledge Base | AI / Full-Stack | [GitHub](https://github.com/venuvankaraghuvardhan-arch/WikiMind-AI-Powered-Knowledge-Base) |
| 07 | SmartCart Intelligence | ML / Full-Stack | [GitHub](https://github.com/venuvankaraghuvardhan-arch/SmartCart-Intelligence) |
| 08 | Customer Churn Prediction | Machine Learning | [GitHub](https://github.com/venuvankaraghuvardhan-arch/customer-churn-prediction) |
| 09 | HR Employee SQL Analysis | Data Engineering | [GitHub](https://github.com/venuvankaraghuvardhan-arch/hr-sql-analysis) |
| 10 | Global COVID-19 EDA | Data Analytics | [GitHub](https://github.com/venuvankaraghuvardhan-arch/Global-COVID-19-Data) |

---

## 🎨 Design System

### Color Palette
```css
--void:          #050508   /* Primary background */
--abyss:         #0c0c12   /* Section alternation */
--surface:       #13131c   /* Card surfaces */
--lift:          #1c1c28   /* Subtle lift */
--violet:        #6366f1   /* Brand accent */
--violet-bright: #818cf8   /* Lighter violet */
--cyan:          #22d3ee   /* Data accent */
--green:         #4ade80   /* Status / success */
--amber:         #fbbf24   /* QA accent */
--white:         #f0eee8   /* Warm white text */
```

### Typography
- **Display / Headings**: `Bebas Neue` — bold, impactful, all-caps system
- **Body / Quotes**: `Fraunces` — elegant, italic-capable optical serif
- **Mono / Labels / Code**: `DM Mono` — refined monospace for technical details

### Animations
| Effect | Implementation |
|---|---|
| Loading screen | CSS keyframe + JS timeout |
| Custom cursor | RAF loop with lag interpolation |
| Scroll reveal | `IntersectionObserver` + CSS transform |
| Skill bars | `IntersectionObserver` + `scaleX()` transition |
| Hero parallax | `scroll` event + `translateY` |
| Counter count-up | JS `setInterval` |
| Ticker marquee | CSS `@keyframes translateX` |
| Ambient orbs | CSS `@keyframes` with `filter: blur()` |
| Noise texture | Inline SVG `feTurbulence` overlay |

---

## 🏗️ Architecture

```
portfolio/
├── index.html          # Single-file portfolio (HTML + CSS + JS)
└── README.md           # This file
```

Everything lives in one **self-contained `index.html`** — no build step required.  
Zero dependencies. No npm. No webpack. Pure HTML/CSS/JS that loads instantly.

---

## 🚀 How to Deploy on GitHub Pages

### Step 1 — Replace Your Portfolio File

```bash
# Clone your portfolio repo
git clone https://github.com/venuvankaraghuvardhan-arch/venuvankaraghuvardhan-arch.github.io
# or if it's in a subfolder:
git clone https://github.com/venuvankaraghuvardhan-arch/portfolio
```

### Step 2 — Replace index.html

```bash
# Copy the new index.html into your repo root
cp /path/to/new/index.html ./index.html
```

### Step 3 — Commit and Push

```bash
git add index.html README.md
git commit -m "feat: complete portfolio redesign with 10 live projects"
git push origin main
```

### Step 4 — Verify on GitHub Pages

Go to `Settings → Pages` in your repo and confirm the source is set to `main` branch, root folder. Your portfolio will be live at:

```
https://venuvankaraghuvardhan-arch.github.io/portfolio/
```

---

## 📧 Enable Contact Form (Optional)

The contact form is wired up and ready. To make it actually send emails, sign up for **[EmailJS](https://emailjs.com)** (free tier — 200 emails/month):

1. Create a free account at emailjs.com
2. Connect your Gmail
3. Create an email template
4. Add this before `</body>`:

```html
<script src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
<script>
  emailjs.init("YOUR_PUBLIC_KEY");
</script>
```

5. In the form's submit handler, replace the comment:

```javascript
emailjs.sendForm('YOUR_SERVICE_ID', 'YOUR_TEMPLATE_ID', this)
  .then(() => { /* success */ })
  .catch(console.error);
```

---

## 🧠 Project Filter Tags

Each project card is tagged with `data-category` for the live filter system:

```
all    → Shows all 10 projects
ai     → AI / LLM projects (RAG, Router, Fine-Tuning, Eval)
ml     → Machine Learning (Churn, SmartCart, Synthetic Data)
data   → Data Engineering (HR SQL, COVID EDA)
full   → Full-Stack (Production RAG, WikiMind, SmartCart)
qa     → QA Automation (none currently — ready to add)
```

---

## ✏️ How to Update Projects

Each project card follows this pattern inside `<!-- PROJECTS -->`:

```html
<div class="project-card reveal" data-category="ai ml">
  <div class="project-index">XX</div>
  <div class="project-category cat-ai">AI / LLM</div>
  <h3 class="project-name">PROJECT NAME</h3>
  <p class="project-tagline">SUBTITLE / METRIC</p>
  <p class="project-desc">Description here.</p>
  <div class="project-metrics">
    <div class="metric">
      <div class="metric-val">97%</div>
      <div class="metric-label">Key Metric</div>
    </div>
  </div>
  <div class="project-stack">
    <span class="stack-tag">Python</span>
  </div>
  <a href="GITHUB_LINK" target="_blank" class="project-link">
    View on GitHub
    <svg viewBox="0 0 16 16" fill="none" stroke="currentColor" stroke-width="1.5">
      <path d="M3 8h10M8 3l5 5-5 5"/>
    </svg>
  </a>
</div>
```

**Category classes:** `cat-ai` · `cat-ml` · `cat-data` · `cat-qa` · `cat-full`

---

## 📱 Responsive Breakpoints

| Breakpoint | Behaviour |
|---|---|
| `> 1024px` | Full desktop layout, 2-col projects, 3-col skills |
| `≤ 1024px` | Single column everything, custom cursor disabled |
| `≤ 640px` | Mobile nav hidden, hero stack simplified |

---

## 👤 Author

**Raghu Vardhan Venuvanka**  
B.Tech Computer Science & Data Science — VJIT Hyderabad (GPA 8.1) — Class of 2026

| Channel | Link |
|---|---|
| 📧 Email | [venuvankaraghuvardhan@gmail.com](mailto:venuvankaraghuvardhan@gmail.com) |
| 💻 GitHub | [github.com/venuvankaraghuvardhan-arch](https://github.com/venuvankaraghuvardhan-arch) |
| 💼 LinkedIn | [linkedin.com/in/raghuvardhan-venuvanka](https://www.linkedin.com/in/raghuvardhan-venuvanka) |
| 📸 Instagram | [@_raghuvardhan](https://www.instagram.com/_raghuvardhan/) |

---

## 📜 License

MIT — Feel free to fork and customise. If you use this as inspiration, a GitHub star ⭐ is appreciated.

---

*"No student in the world should have a portfolio like mine."* — Raghu Vardhan

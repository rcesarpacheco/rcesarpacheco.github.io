# rodrigopacheco.com

Personal academic website — Hugo + GitHub Pages.

## Quick start

### 1. Install Hugo

```bash
# macOS
brew install hugo

# or download from https://gohugo.io/installation/
```

### 2. Run locally

```bash
hugo server -D
# Open http://localhost:1313
```

### 3. Add your files

Place these in the `static/` directory:

```
static/
├── img/
│   └── headshot.jpg            ← your photo (square, ~400x400px)
├── files/
│   ├── Pacheco_CV.pdf
│   ├── Pacheco_JMP.pdf
│   ├── Pacheco_JMP_slides.pdf
│   ├── Pacheco_JMP_appendix.pdf
│   ├── Pacheco_BankCompetition.pdf
│   ├── Pacheco_BankCompetition_slides.pdf
│   ├── Pacheco_Hanson_JobLadder.pdf
│   └── teaching/
│       ├── IntMacro_Syllabus_2024.pdf
│       ├── IntMacro_Syllabus_2025.pdf
│       ├── IntMacro_Slides_2024.zip
│       ├── IntMacro_Slides_2025.zip
│       └── IntMacro_ProblemSets_2025.zip
```

### 4. Edit content

All pages are in `content/`:

| File              | Page     |
|-------------------|----------|
| `_index.md`       | Home     |
| `research.md`     | Research |
| `cv.md`           | CV       |
| `teaching.md`     | Teaching |

Fill in the `[bracketed placeholders]` with your actual content (abstracts, coauthor names, etc.).

### 5. Update config

Edit `config.toml` to set your real email, links, etc.

## Deploy to GitHub Pages

1. Create a GitHub repo (e.g., `rodrigopacheco.github.io` or any name)
2. Push this project to the repo
3. Go to **Settings → Pages → Source** → select **GitHub Actions**
4. The included `.github/workflows/hugo.yml` will auto-deploy on every push

## Custom domain

1. Buy a domain (e.g., Namecheap, Google Domains, Cloudflare)
2. In your domain's DNS settings, add:
   - A record: `185.199.108.153`
   - A record: `185.199.109.153`
   - A record: `185.199.110.153`
   - A record: `185.199.111.153`
   - CNAME for `www`: `rodrigopacheco.github.io`
3. In GitHub repo → **Settings → Pages → Custom domain**: enter `rodrigopacheco.com`
4. Check "Enforce HTTPS"
5. Update `baseURL` in `config.toml`

## Structure

```
├── config.toml          ← site settings, nav menu
├── content/             ← page content (Markdown)
├── layouts/             ← HTML templates
│   ├── _default/
│   │   ├── baseof.html  ← base wrapper
│   │   └── single.html  ← inner pages
│   ├── index.html       ← home page
│   └── partials/
│       └── sidebar.html ← sidebar component
├── static/
│   ├── css/style.css    ← all styles
│   ├── files/           ← PDFs, slides, etc.
│   └── img/             ← headshot
└── .github/workflows/   ← auto-deploy config
```

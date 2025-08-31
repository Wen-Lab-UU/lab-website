
# Hugo Lab Website Starter (PaperMod)

This is a **ready-to-go Hugo lab skeleton** with sections for **People, Publications, Projects, News, Openings, Contact** using the **PaperMod** theme.

## Quick Start

### Option A: Local preview
1. Install **Hugo (extended)**: https://gohugo.io/installation/
2. Install **Git**: https://git-scm.com/
3. In a terminal:
   ```bash
   git init
   git submodule add https://github.com/adityatelange/hugo-PaperMod themes/PaperMod
   hugo server
   ```
4. Open http://localhost:1313

### Option B: Deploy with Netlify (no local install needed)
1. Push this folder to a **GitHub** repository.
2. In **Netlify**, click **"Add new site → Import an existing project"** and select your repo.
3. Build command: `hugo --gc --minify`
4. Publish directory: `public`
5. Netlify will give you `https://SITENAME.netlify.app`. You can add a **custom domain** and HTTPS for free.

## Editing Content
- **People:** `content/people/` (one Markdown file per person). Add photos under `static/img/people/`.
- **Publications:** `content/publications/` (one Markdown file per paper). Put PDFs under `static/pdfs/`.
- **Projects:** `content/projects/`
- **News:** `content/news/` (use `YYYY-MM-DD-title.md`).
- **Openings:** `content/openings/_index.md`
- **Contact:** `content/contact/_index.md`

## Customize
- Site title, tagline, menu: `config.toml`
- Logos/Favicon: replace files in `static/img/`

## Optional: Switch to Wowchemy (Academic) for advanced publications
If you want BibTeX import, filters, and academic layouts:

1. Remove PaperMod submodule (if added):
   ```bash
   git rm themes/PaperMod
   rm -rf themes/PaperMod
   ```
2. Use Hugo Modules to pull Wowchemy:
   ```bash
   hugo mod init github.com/yourname/lab-website
   # Add this to config.toml:
   #   theme = ""
   #   [module]
   #     [[module.imports]]
   #       path = "github.com/wowchemy/starter-hugo-research-group"
   # Then run:
   hugo mod get -u
   ```
3. Copy/adapt your content into the Wowchemy content structure (authors, publication, project, post).
4. Deploy to Netlify; Netlify will fetch modules during build.

## Custom Domain
- In Netlify: **Domain management → Add custom domain** (e.g., `yourlab.org`).
- Point your domain's DNS **CNAME** to your Netlify subdomain.
- Netlify will issue **free HTTPS** automatically.

## Tips
- Keep images small (webp/jpg) for speed.
- Use `weight:` in front matter to order people.
- Add DOIs/links in publications and upload PDFs you have permission to share.

---

Happy publishing!

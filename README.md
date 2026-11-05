# Felix Mosner – academic website

A simple, free, bilingual (EN/DE) website hosted on **GitHub Pages**. No software to install, no costs, no ads — everything is done in the browser.

Pages: Home · Publications · Blog · Teaching · CV (each in English and German).

---

## 1. Put it online (one-time, ~15 minutes)

1. **Create a free GitHub account** at <https://github.com/signup>. Pick your user name carefully — it becomes your web address, e.g. `felixmosner` → `https://felixmosner.github.io`.
2. **Create a repository:** click **+** (top right) → **New repository**.
   - Repository name: exactly `USERNAME.github.io` (your user name, e.g. `felixmosner.github.io`)
   - Visibility: **Public** → **Create repository**.
3. **Upload the files:** on the new empty repository page, click **"uploading an existing file"**. Unzip the website folder on your computer, open it, select **everything inside it** (including the folders `_data`, `_layouts`, … — *not* the outer folder itself) and drag it into the browser window. Click **Commit changes**.
   - Tip: on a Mac, folders starting with `_` are visible; on Windows too. If you don't see them, they're still selected when you press Ctrl/Cmd + A.
4. **Turn on Pages:** repository → **Settings** → **Pages** → under *Build and deployment* choose **Source: Deploy from a branch**, **Branch: main / (root)** → **Save**.
5. Wait 1–2 minutes, then open `https://USERNAME.github.io`. Done.
6. In `_config.yml`, replace `USERNAME` in the `url:` line with your user name (see "How to edit" below).

## 2. How to edit anything

Open the file on github.com → click the **pencil icon** (Edit) → change the text → **Commit changes**. The site updates automatically within ~1 minute.

| What you want to change | File |
|---|---|
| Name, e-mail, ORCID / Scholar / LinkedIn links, photo on/off | `_config.yml` |
| Home page: headline, intro, selected work, research topics, contact text (EN / DE) | `index.md` / `de/index.md` (all texts are at the top of the file) |
| Impressum (legal notice) — **fill in your address before going live** | `impressum.md` |
| Publications | `_data/publications.yml` (one list for both languages) |
| Courses & teaching materials | `_data/teaching.yml` |
| CV | `cv/index.md` / `de/cv/index.md` |
| Colours, fonts | `assets/style.css` (top of the file) |

**Careful with `.yml` files:** indentation (spaces) matters. Copy an existing entry and change its values — that's the safest way.

## 3. Add a blog post

1. Go to the `_posts` folder (English) or `de/_posts` (German) → **Add file → Create new file**.
2. Name it `YYYY-MM-DD-short-title.md`, e.g. `2026-12-01-new-paper.md`.
3. Paste this and write below it:

```
---
title: "My post title"
summary: "One sentence shown in the post list."
---
Your text here. **Bold**, *italic*, [a link](https://example.org).

## A sub-heading

- a list item
```

4. **Commit changes.** If you also write a translation, add `alt: /de/blog/2026/kurzer-titel/` to the English post (and the reverse in the German one) so the language button jumps between the two.

## 4. Upload PDFs (papers, slides, handouts)

1. Go to `files/papers` or `files/teaching` → **Add file → Upload files** → drop the PDF → **Commit**.
2. Link it:
   - Paper: in `_data/publications.yml` set `pdf: /files/papers/your-file.pdf`
   - Course material: in `_data/teaching.yml`, under the course:
     ```
     materials:
       - { title: "Slides week 1", file: /files/teaching/week1.pdf }
     ```

Use simple file names (no spaces or umlauts): `mosner-2025-jom.pdf`.

⚠️ **Copyright:** for published articles, check the journal's self-archiving policy (usually the *accepted manuscript* is allowed, the publisher's final PDF often isn't). Wiley/JOM policies can be checked on <https://openpolicyfinder.jisc.ac.uk>.

## 5. Add your photo

Upload a square image named `profile.jpg` to `assets/img/`, then set `photo: true` in `_config.yml`.

## 6. Optional extras

- **Own domain** (e.g. `felixmosner.de`, ~€5–15/year — the only thing that costs money): Settings → Pages → Custom domain.
- **Prefer editing on your computer?** Install *GitHub Desktop* (free) and any text editor; changes sync with one click.
- **Uni Köln:** you can also link this site from your official university profile.

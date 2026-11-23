# Site Editing & Maintenance Guide

Quick reference for updating `yamaishou.github.io`.  
*(This file is excluded in `_config.yml`, so it will not appear on your live website.)*

---

## Where to Edit Content

| What you want to update | File to edit | Section / Field to look for |
| :--- | :--- | :--- |
| **Site title, tagline, or top nav bar** | `_config.yml` | `title:`, `description:`, and `header_pages:` |
| **Homepage bio & research interests** | `index.md` | Text under `### Research Interests` |
| **Selected papers on the homepage** | `index.md` | `<div class="pub-item">` blocks under `### Selected Publications & Preprints` |
| **Email, office, or profile links** | `index.md` | Bullet list under `### Contact & Links` (InspireHEP, Google Scholar, GitHub) |
| **Full publication list, abstracts & talks** | `publications.md` | `<div class="pub-item">` blocks and `### Notes & Talks` |
| **LaTeX macros or font/CSS styling** | `_includes/head-custom.html` | `MathJax = { ... }` config or `<style>` block |

---

## Copy-Paste Template for a New Paper

Open **`publications.md`** (and **`index.md`** if featuring on the homepage) and paste this block at the top of the list:

```html
<div class="pub-item">
  <div class="pub-title">Paper Title (supports inline LaTeX like $\text{dS}_4$)</div>
  <div><strong>S. Yamamoto</strong>, Co-author Name</div>
  <div><em>Journal Name / arXiv:26XX.XXXXX [hep-th]</em> (2026)</div>
  <div class="pub-links">
    <a href="[https://arxiv.org/abs/26XX.XXXXX](https://arxiv.org/abs/26XX.XXXXX)">[arXiv]</a>
    <a href="[https://doi.org/](https://doi.org/)...">[DOI]</a>
    <a href="/assets/paper.pdf">[PDF]</a>
  </div>
  <details>
    <summary>Abstract</summary>
    <p>Paste abstract here. Inline math ($...$) and display math ($$...$$) render automatically.</p>
  </details>
</div>

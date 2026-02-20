# danielkleviansky.com

Personal website built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme. Auto-deploys to GitHub Pages on push to `main`.

Live at **[danielkleviansky.com](https://danielkleviansky.com)**

---

## Local development

```bash
# Clone with theme submodule
git clone --recurse-submodules https://github.com/lqid/danielkleviansky.com.git
cd danielkleviansky.com

# Run dev server
hugo server -D
# → http://localhost:1313
```

If you cloned without `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

## Adding a post

```bash
hugo new posts/post-title.md
# Edit content/posts/post-title.md
# Set draft: false when ready
git add . && git commit -m "Add post: title" && git push
```

## Key files

| File | Purpose |
| ---- | ------- |
| `hugo.toml` | Site config, nav, social links |
| `content/resume.md` | Résumé content |
| `layouts/projects/single.html` | Projects page data |
| `layouts/music/single.html` | Music releases data |
| `assets/css/extended/` | Custom styles |

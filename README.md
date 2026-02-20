# danielkleviansky.com

Personal website built with [Hugo](https://gohugo.io/) and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) theme.  
Auto-deploys to GitHub Pages on every push to `main`.

---

## First-time setup

### 1. Install Hugo

```bash
# macOS
brew install hugo

# or grab a binary from https://github.com/gohugoio/hugo/releases
```

### 2. Clone this repo with the theme submodule

```bash
git clone --recurse-submodules https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd YOUR_REPO
```

If you already cloned without `--recurse-submodules`:

```bash
git submodule update --init --recursive
```

### 3. Add PaperMod as a submodule (first time only)

```bash
git submodule add --depth=1 https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

### 4. Run locally

```bash
hugo server -D
# Open http://localhost:1313
```

---

## Writing a new post

```bash
hugo new posts/my-post-title.md
# Edit content/posts/my-post-title.md
# Change draft: false when ready to publish
git add . && git commit -m "Add new post" && git push
```

That's it — GitHub Actions will build and deploy automatically.

---

## Updating your résumé

Edit `content/resume.md` directly, then commit and push.

---

## GitHub Pages setup (one-time)

1. Go to your repo → **Settings → Pages**
2. Set **Source** to `GitHub Actions`
3. Point your custom domain (`danielkleviansky.com`) to GitHub Pages by adding a `CNAME` file:

```bash
echo "danielkleviansky.com" > static/CNAME
git add . && git commit -m "Add CNAME" && git push
```

Then update your DNS to point to GitHub Pages (see [GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).

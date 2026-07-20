# AutoIndex — Project Page

A high-level, results-focused project page for **AutoIndex: Learning Representation
Programs for Retrieval**.

AutoIndex treats document representation as a code-optimization problem: given a corpus
and a fixed retriever (BM25), it searches over executable *representation programs* that
transform documents before indexing, keeping only changes that improve retrieval on a
validation set. On the CRUMB benchmark it improves Recall@100 on all 8 tasks
(+8.4% avg) with no retriever fine-tuning.

## Structure

```
index.html                 # the page (single file)
static/
  css/style.css            # theme-aware styles (light default, dark toggle)
  images/loop_diagram.png  # Figure 1 — the optimization loop
  AutoIndex.pdf            # the paper
```

The results bar chart is inline, hand-built SVG with hover tooltips (not a screenshot),
and the worked-example pipeline is a scroll-triggered, left-to-right animated flow — both
crisp and theme-aware in light and dark.

## Run locally

```bash
python3 -m http.server 8731
# open http://localhost:8731
```

It's fully static — deploy to GitHub Pages, Vercel, Netlify, or any static host by
serving the folder root.

## Deploying

- **GitHub Pages:** push to a repo, then enable Pages (Settings → Pages → deploy from
  branch, root).
- **Vercel:** `vercel` from this folder, or import the repo (framework preset: *Other*,
  output dir: root).

## Credits

Layout adapted from the [Academic Project Page Template](https://github.com/eliahuhorwitz/Academic-project-page-template)
(CC BY-SA 4.0).

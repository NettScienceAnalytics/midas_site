# MIDAS Blog — How to Publish (Weekly Cheat Sheet)

Your blog runs on **Jekyll**, which GitHub Pages builds automatically. You never
touch HTML to publish — you just add one Markdown file and push.

---

## To publish a new post (the whole weekly routine)

1. In the `midas_site` repo, go to the `_posts` folder.
2. Click **Add file → Create new file**.
3. Name it with this exact pattern (date first, then a short slug, `.md` ending):

   ```
   _posts/2026-06-17-your-post-slug.md
   ```

   The date in the filename is the publish date. The slug becomes the URL:
   `midas.nettscience.com/blog/your-post-slug/`

4. Paste this template at the top, then write your post below it in Markdown:

   ```markdown
   ---
   layout: post
   title: "Your Headline Here"
   subtitle: "One or two sentences that appear under the title and on the blog index card."
   date: 2026-06-17
   author: Raja Bhat
   description: "A 1-line SEO description for search engines."
   ---

   Your first paragraph here.

   ## A section heading

   More text. **Bold**, *italic*, and [links](https://example.com) all work.

   - bullet one
   - bullet two

   > A pull-quote, if you want one.
   ```

5. Click **Commit changes**.
6. Wait ~1 minute. The post is live at `midas.nettscience.com/blog/` and at its
   own URL. The blog index lists it automatically — you never edit the index.

That's it. One file a week.

---

## Markdown quick reference

| You want | You type |
|---|---|
| Heading | `## Heading` (use `##`, not `#` — `#` is reserved for the title) |
| Sub-heading | `### Sub-heading` |
| Bold | `**bold**` |
| Italic | `*italic*` |
| Link | `[text](https://url.com)` |
| Internal link to demo | `[Book a demo](/#contact)` |
| Bullet list | `- item` on each line |
| Numbered list | `1. item` on each line |
| Pull-quote | `> quoted text` |
| Image | `![alt text](/assets/img/photo.jpg)` |

For images: create an `assets/img/` folder in the repo, upload the image there,
then reference it as shown above.

---

## Front matter fields explained

- **layout** — always `post`. Don't change it.
- **title** — the headline. Keep the quotes.
- **subtitle** — optional. Shows under the title and as the card excerpt on the
  blog index. If omitted, the index auto-generates an excerpt from your first lines.
- **date** — `YYYY-MM-DD`. Should match the filename date.
- **author** — optional. Defaults to nothing if omitted.
- **description** — optional but recommended for SEO.

---

## What's in this folder (one-time setup — already done)

```
midas_site/
├── _config.yml          ← Jekyll settings (scoped so it ignores your SPA)
├── index.html           ← your existing site, untouched except a Blog nav link
├── assets/site.css      ← your full design + blog article styles
├── _layouts/
│   ├── default.html     ← header + footer shell (matches your site)
│   └── post.html        ← article page layout
├── _posts/
│   └── 2026-06-10-attribution-blind-spot.md   ← sample post (delete or keep)
└── blog/
    └── index.html       ← the /blog/ landing page (auto-lists posts)
```

You don't need to understand or edit any of these to publish. Only `_posts/`.

---

## One-time GitHub Pages check

After the first push, make sure GitHub Pages is building from the right branch:
**repo → Settings → Pages → Build and deployment → Source: "Deploy from a branch",
Branch: `main`, folder `/ (root)`.** That's the default, so it's likely already set.

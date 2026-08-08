# ericangella.com

Personal site and blog for Eric Angella. Built with [Astro](https://astro.build), deployed via Netlify.

## Stack

- **Astro** — static site generator, content collections for blog posts
- **Netlify** — hosting, auto-deploys on push to `main`
- **Markdown** — blog posts live as plain `.md` files, no CMS/admin panel

## Writing a new post

1. Create a new file in `src/content/blog/`, e.g. `my-new-post.md`
2. Add frontmatter:
   ```yaml
   ---
   title: "Post title"
   excerpt: "One-line description, shown in the post list."
   date: 2026-07-15
   ---
   ```
3. Write the post body in markdown below the frontmatter.
4. Commit and push — Netlify rebuilds and deploys automatically.

Add `draft: true` to the frontmatter to keep a post out of the build until it's ready.

## Local development

```bash
npm install
npm run dev       # local dev server
npm run build     # production build to dist/
npm run preview   # preview the production build locally
```

## Project structure

- `src/content/blog/` — blog posts (markdown)
- `src/components/Hero.astro` — homepage hero ("Mostly Human Stuff")
- `src/components/PostList.astro` — post list renderer
- `src/layouts/BaseLayout.astro` — shared page shell (nav, footer)
- `src/pages/index.astro` — homepage
- `src/pages/blog/[...id].astro` — individual post pages
- `src/pages/about.astro` — about page
- `src/styles/global.css` — design tokens (colors, fonts)
- `public/images/headshot.jpg` — homepage headshot (replace with final photo)

## Design system

- Background: warm dark charcoal (`#1B1918`)
- Headlines/post titles: Fraunces (serif, italic)
- Body text: Source Serif 4
- Metadata (dates, nav, labels): IBM Plex Mono
- Monochrome accent — no color yet, brightness/contrast only

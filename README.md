# Dialed In Trades — Site Source

Static Jekyll site, built to deploy on GitHub Pages.

## Local setup

1. Install Ruby and Bundler if not already installed.
2. From this directory, run:
   ```
   bundle install
   bundle exec jekyll serve
   ```
3. Visit `http://localhost:4000`.

## Before launch, replace these placeholders

- `_config.yml`
  - `booking_url`: your real Calendly (or similar) link
  - `url`: your GitHub Pages URL or custom domain
- `contact.md`
  - Calendly embed `src` URL
  - Formspree form `action` URL (sign up at formspree.io, create a form, use the ID it gives you)
- `assets/css/style.css`
  - Brand colors (terracotta/teal) and fonts (Fraunces/Manrope) are set, matching
    davidcmitchell.com's rebrand.
- `newsletter.md`
  - Create a dedicated form for Dialed In Trades in the Kit dashboard, then
    replace the placeholder embed comment with the real `<script>` embed.
- Add a real logo image if you don't want the text logo in the header.
- `_config.yml` → `analytics.plausible_domain`: set this to enable Plausible
  analytics (leave blank to keep analytics off). Swap the snippet in
  `_layouts/default.html` if Fathom or GA4 is preferred instead.
- Testimonials: placeholder comment blocks are left in `about.md` and
  `services.md` — uncomment and fill in once a client quote exists.

## Deploying to GitHub Pages

1. Push this content to the repo's default branch (or a `gh-pages` branch,
   depending on how the repo's Pages settings are configured).
2. In the repo's Settings > Pages, set the source to the branch you pushed to.
3. GitHub Pages will build automatically using its built-in Jekyll support
   since the Gemfile uses the `github-pages` gem.

## Adding blog posts

Add a new Markdown file to `_posts/` named `YYYY-MM-DD-title.md` with this
front matter:

```
---
title: "Post Title"
date: YYYY-MM-DD
excerpt: "One sentence summary for the blog index."
---
```

Write the post body in Markdown below the front matter. It will appear
automatically on the blog index page.

## Structure

```
_config.yml          site settings, booking/contact links
_layouts/default.html   header, nav, footer, wraps every page
_layouts/post.html      blog post template
_posts/               blog content, one file per post
_includes/             (empty, reserved for shared snippets)
index.html            home page
about.md               about page
services.md            services page
resources.md            tools & blog resources page
newsletter.md           email signup page
contact.md              contact page, form + booking embed
blog/index.html         blog listing page
assets/css/style.css     all site styling
```

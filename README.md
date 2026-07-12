# Idea Spinner

A single-file, no-build, works-offline participatory-budgeting idea tool.
Built and hosted by [Wildest Future](https://wildestfuture.com). The entire app
is `index.html` — HTML, CSS, and vanilla JS with no dependencies and no framework. Open it
in a browser and it runs; host it anywhere static.

Deployed to <https://spinner.wildestfuture.com> via GitHub Pages.

## Running it

Open `index.html` in any modern browser, or serve the folder statically. There is nothing
to build or install.

## How it works

Participants move through five screens: landing → names → spin (a name paired with an idea
prompt) → proposal → thank-you. A hidden settings panel (gear icon) lets a facilitator
customize the title, people prompts, idea prompts, and colors, and share a configuration
via a `?config=` URL. Saved proposals can be reviewed and exported (Copy, Email, CSV,
Decidim JSON).

## Analytics (pageviews only)

This site includes [Plausible](https://plausible.io) to count pageviews — that is all.
Plausible is cookieless, collects no personal data, and does **not** track in-session
actions (no export instrumentation, no event tracking). It answers only "is anyone using
this," and nothing more. Offline sessions are never reported, by design.

The script sits in the `<head>` of `index.html`:

```html
<!-- Privacy-friendly analytics by Plausible -->
<script async src="https://plausible.io/js/pa-aCemsgbdYbXG3kURHtSQQ.js"></script>
<script>
  window.plausible=window.plausible||function(){(plausible.q=plausible.q||[]).push(arguments)},plausible.init=plausible.init||function(i){plausible.o=i||{}};
  plausible.init()
</script>
```

**To strip it from a fork:** delete that whole block (both `<script>` tags). The app is
unaffected — it never depends on the script loading.

# Changelog

All notable changes to Idea Spinner. Versions follow [Semantic Versioning](https://semver.org).
Pre-1.0: still evolving quickly, so minor versions may include behavior/UI changes.

## [0.3.0] — 2026-07-12

### Added
- Proposals persist to `localStorage` (survive a refresh); facilitator "Clear all
  proposals" on the Review screen, guarded by a confirm that warns louder when
  nothing has been exported yet.
- Plausible pageview analytics (pageview-only, no events/session tracking).
- Email client picker on export — Mail app / Gmail / Outlook / Yahoo compose
  links instead of a raw `mailto:` (viewport-aware, flips up on mobile).
- "Tell us how it went" opt-in feedback button (prefills the proposal count only).
- Thematic prompt packs: pack chips in Settings append prompts (deduped), plus
  plain-text pack import/export (one prompt per line).
- Semantic versioning (this changelog + a version shown in Settings).

### Changed
- Merged the spin and proposal steps into one screen: typing an answer reveals
  the Title label + money/why fields + Save inline; the answer is the title;
  "Spin again" resets.
- Adopted the Wildest Future brand palette (Velvet Teal anchor + Marigold spark)
  with a full contrast pass; fixed the theme engine so muted and placeholder
  text stay readable instead of rendering dark-on-dark or gold-on-white.
- Easier Settings exit: sticky close button, Escape, and backdrop click.
- Renamed the product to "Idea Spinner"; repo renamed to `idea-spinner`.

## [0.2.0] — earlier

### Added
- Review screen with select + export (Copy, Email, CSV, Decidim JSON).
- Floating proposal counter/indicator.
- Facilitator customization via a hidden Settings menu: app title, people
  prompts, idea prompts, and color themes.
- Share/import settings via a `?config=` URL.

## [0.1.0] — initial

### Added
- The core spinner app: landing → names → spin → proposal → thank-you, pairing a
  person prompt with an idea prompt to draft participatory-budgeting proposals.

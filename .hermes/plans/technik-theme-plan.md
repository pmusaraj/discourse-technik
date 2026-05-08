# Technik Discourse theme plan

## Reference URL

- URL: https://zed.dev/pricing
- Page inspected: pricing landing page, hero/pricing/FAQ/footer areas.
- Notes: browser visual pass and computed-style sampling confirmed a pale technical drawing aesthetic: graph-paper fields, thin construction lines, dashed rails, small node/crosshair details, mono body/navigation, serif display headings, rectangular cards, and strong blue action states.

## Visual extraction

- Palette direction: light engineering-paper base with cool gray text, muted blue-gray grid lines, and a vivid but original indigo-blue accent. Do not copy Zed exact colors.
- Background/surface: warm off-white page, white-to-paper panels, subtle blue-tinted selected/hover states.
- Typography: system UI for readable Discourse body copy; serif display headings for category/topic section headings; mono labels for nav, metadata, counts, and table headings.
- Radius scale: mostly square/technical (`4px`-`8px`), no pill-heavy treatment except optional compact badges.
- Borders/shadows: hairline borders and linework instead of heavy shadows. Small low-opacity shadows only for menus/composer separation.
- Patterns: use Zed-like line styling — graph grid, dashed vertical guides, corner/crosshair nodes, and diagonal hatching — implemented as original CSS gradients.
- Spacing density: precise and moderately spacious, not oversized; keep Discourse tables readable.
- Buttons/inputs/cards: rectangular, thin-border controls; primary button gets solid blueprint-blue fill.

## Discourse mapping

- Color scheme: create/update `Technik` with near-black primary text, warm paper secondary, original indigo tertiary, cyan quaternary, pale technical highlight, normal semantic colors.
- CSS variables: map `--technik-*` tokens onto Discourse color variables and use them for backgrounds, borders, linework, surfaces, and focus states.
- Target selectors/components:
  - page/body background linework
  - header/sidebar surface
  - nav pills and buttons
  - topic/category/latest tables
  - category boxes
  - topic posts/composer
  - inputs/select-kit/menu panels
  - user/group card `.card-content` only
- Intentionally default: Discourse markup, app behavior, core navigation, plugin UI, icon set, and most layout sizing.

## Theme scaffold

- Repo/path: `/Users/pmusaraj/Projects/discourse-technik`
- Theme name: `Technik`
- Files:
  - `about.json`
  - `common/common.scss`
  - `README.md`
  - `.hermes/plans/technik-theme-plan.md`
- Optional files: no desktop/mobile split for first pass; no JS; no settings.
- Icon component: none needed.

## Testing plan

1. Initialize local repo and write scaffold.
2. Import/update local theme into `https://disco2021.musaraj.com` using the existing Docker Discourse instance.
3. Create/update `Technik` color scheme and set as theme color scheme/default theme.
4. Verify DB/theme state and compiled CSS URL.
5. Browser-check `/latest`, `/categories`, a topic page, and composer/new-topic.
6. Confirm rendered page loads `common_theme_<id>`, Technik tokens are applied, no theme error banner, and no relevant console errors.

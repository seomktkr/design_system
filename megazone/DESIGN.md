# Design System Inspiration of MegazoneCloud

## 1. Visual Theme & Atmosphere

MegazoneCloud's website is the visual declaration of a cloud-native company that has staked its identity on AI transformation. The design system lives in a precise tension: a rigidly professional white-and-gray enterprise foundation is punctuated by a five-color AI gradient — green (`#32ef7a`) through cyan (`#00d7f8`), electric blue (`#414aff`), violet (`#8920ff`), and pink (`#ff41c1`) — that functions as the brand's single most distinctive element. This gradient is not a decoration; it is the brand's thesis statement that AI technology spans the full spectrum of possibility.

The overall atmosphere is B2B-premium: clean white canvases (`#fff`), light gray alternating backgrounds (`#f7f7f7`, `#f0f0f0`), and near-black body text (`#191919`). The result reads as trustworthy and competent, the visual language of a company that handles enterprise infrastructure for 8,000+ clients. The design never shouts — it reassures.

Typography is anchored by **Pretendard**, a Korean-optimized variable font that covers weights 100–900, with fallback to Noto Sans JP and Noto Sans SC for multilingual support. At display sizes, text is set in semibold or bold (600–700) with moderate negative tracking for Korean-optimized density. The system uses Tailwind CSS v4 utility classes for spacing, but custom CSS tokens (`--color-*`, `--color-gradient-*`) carry the brand identity above the utility layer.

The gradient is deployed with surgical precision: as a text treatment for hero headlines, as a border accent on featured cards, and as a background band on section headers. Outside these signature moments, the palette returns to strict neutrals.

**Key Characteristics:**
- Pretendard (Korean-first) with full 9-weight range (100–900) via WOFF web fonts
- Five-color AI spectrum gradient as the primary brand signature element
- Strict neutral base: White `#fff` / Light Gray `#f7f7f7` / Medium Gray `#f0f0f0`
- Near-black text `#191919` — slightly softened from pure black for extended reading
- Conservative 8px (`0.5rem`) border-radius throughout — professional, never playful
- Card-based content architecture for services, products, industries, and case studies
- Tailwind CSS v4 utility system layered with custom brand tokens
- Multilingual-ready: Pretendard (KO) + Noto Sans JP (JA) + Noto Sans SC (ZH)

---

## 2. Color Palette & Roles

### Background
- **White** (`#ffffff` / `--color-bg-white`): Primary page background, card surfaces, modal overlays.
- **Light Gray** (`#f7f7f7` / `--color-bg-light-gray`): Alternate section background for visual rhythm without harsh color shifts.
- **Medium Gray** (`#f0f0f0` / `--color-bg-medium-gray`): Deeper section background, input fill, subdued containers.
- **Black** (`#000000` / `--color-bg-black`): Dark hero sections, immersive feature moments, footer background.

### Text
- **Dark Gray** (`#191919` / `--color-text-dark-gray`): Primary body text, headings on light backgrounds. Near-black with warmth.
- **Black** (`#000000` / `--color-text-black`): Maximum contrast text, hero headlines on white.
- **White** (`#ffffff` / `--color-text-white`): Text on dark and colored backgrounds.
- **Gray** (`#777777` / `--color-text-gray`): Secondary text, metadata, captions.
- **Medium Gray** (`#aaaaaa` / `--color-text-medium-gray`): Muted labels, placeholder text, disabled states.
- **Light Gray** (`silver` / `--color-text-light-gray`): Tertiary text, decorative labels on dark.

### AI Spectrum Accent (Point Colors)
- **Point Green** (`#32ef7a` / `--color-point-green`): Innovation, growth, AI output. Start of the brand gradient.
- **Point Light Blue** (`#00d7f8` / `--color-point-light-blue`): Cloud technology, data flow. Second gradient anchor.
- **Point Blue** (`#414aff` / `--color-point-blue`): Primary interactive accent, CTA elements, links. Core brand blue.
- **Point Purple** (`#8920ff` / `--color-point-purple`): AI intelligence, deep tech, enterprise premium.
- **Point Pink** (`#ff41c1` / `--color-point-pink`): Innovation edge, creativity. End of the brand gradient.

### Brand Gradients
- **Full Spectrum** (`--color-gradient`):
  `linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1)`
  The master brand gradient — used for hero text treatment, section accent bands.

- **Gradient 01-01** (`--color-gradient-01_01`): `linear-gradient(118deg, #32ef7a 20.19%, #00d7f8)`
- **Gradient 01-02** (`--color-gradient-01_02`): `linear-gradient(304deg, #414aff 45.28%, #00d7f8 105.07%)`
- **Gradient 01-03** (`--color-gradient-01_03`): `linear-gradient(314deg, #8920ff 22.12%, #414aff)`
- **Gradient 01-04** (`--color-gradient-01_04`): `linear-gradient(127deg, #ff41c1 -15.74%, #8920ff 59.05%)`
- **Gradient 02-01** (`--color-gradient-02_01`): `linear-gradient(116deg, #32ef7a 10.37%, #414aff 85.62%)`
- **Gradient 02-02** (`--color-gradient-02_02`): `linear-gradient(132deg, #00d7f8 -21.51%, #8920ff 66.38%)`
- **Gradient 02-03** (`--color-gradient-02_03`): `linear-gradient(125deg, #ff41c1 -10.23%, #414aff 88.92%)`

### Lines & Borders
- **Line Gray** (`#dddddd` / `--color-line-gray`): Dividers, card borders, input outlines.

### Semantic
- **Red** (`red` / `--color-text-red`): Error states, validation messages, alerts.

---

## 3. Typography Rules

### Font Family
- **Primary (Korean)**: `Pretendard`, with fallback: `'Noto Sans JP', 'Noto Sans SC', sans-serif`
- **Font loading**: WOFF via `@font-face`, `font-display: swap`
- **No monospace stack** in the primary UI — technical content uses default browser monospace

Full weight range available:
| Weight | Value |
|--------|-------|
| Thin | 100 |
| Extra Light | 200 |
| Light | 300 |
| Regular | 400 |
| Medium | 500 |
| Semi Bold | 600 |
| Bold | 700 |
| Extra Bold | 800 |
| Black | 900 |

### Hierarchy

| Role | Size (rem) | Size (px) | Weight | Line Height | Notes |
|------|-----------|-----------|--------|-------------|-------|
| Display Hero | 3.75rem | 60px | 700 | 1.15 | Hero headline — AI-Native tagline |
| Section Heading | 2.5rem | 40px | 700 | 1.25 | Major section titles |
| Sub-heading | 2.25rem | 36px | 600–700 | 1.25 | 4xl — Feature headings |
| Card Heading Large | 1.875rem | 30px | 600 | 1.35 | 3xl — Product/service card title |
| Card Heading | 1.5rem | 24px | 600 | 1.4 | 2xl — Standard card title |
| Body Large | 1.25rem | 20px | 400–500 | 1.6 | xl — Feature descriptions |
| Body | 1rem | 16px | 400 | 1.6 | base — Standard reading text |
| Body Small | 0.875rem | 14px | 400 | 1.5 | sm — Captions, metadata |
| Label / Button | 1rem | 16px | 500–600 | 1.0 | Navigation, CTA button text |
| Caption | 0.875rem | 14px | 400 | 1.43 | Timestamps, badges, fine print |

### Principles
- **Korean-first scaling**: Pretendard is optimized for Korean character density — line-height stays tighter (1.25–1.4) compared to Latin-only fonts that require looser rhythm.
- **Weight contrast over size contrast**: The type scale jumps between 400 (body) and 600–700 (headings) rather than relying primarily on size differences. This creates crisp hierarchy at all viewport sizes.
- **No decorative letter-spacing**: Unlike many Western brand systems, Pretendard-based Korean UI avoids positive letter-spacing on headings — the glyph shapes create sufficient rhythm naturally.
- **Consistent reading text**: All body content uses 16px / 400 weight / 1.6 line-height regardless of section background color.

---

## 4. Component Stylings

### Buttons

**Primary Blue (CTA)**
- Background: `#414aff` (Point Blue)
- Text: `#ffffff`
- Padding: 12px 24px
- Radius: 8px (`--radius-lg: 0.5rem`)
- Font: Pretendard 16px weight 600
- Hover: background darkens, slight scale or shadow lift
- Use: Primary CTA ("문의하기", "시작하기", "자세히 보기")

**Ghost / Outlined**
- Background: transparent
- Text: `#414aff`
- Border: `1px solid #414aff`
- Padding: 12px 24px
- Radius: 8px
- Hover: background fills with `rgba(65,74,255,0.06)`
- Use: Secondary actions alongside primary CTA

**Text Link (Learn More)**
- Background: transparent
- Text: `#414aff` or `#191919`
- No border
- Decoration: underline on hover or right-arrow icon appended
- Font: Pretendard 14px–16px weight 500
- Use: Card-level "Learn More" inline actions throughout all content sections

**Dark / Inverted**
- Background: `#ffffff`
- Text: `#191919` or `#414aff`
- Radius: 8px
- Use: CTAs placed on dark (`#000`) or gradient backgrounds

### Cards & Containers

**Standard Content Card**
- Background: `#ffffff`
- Border: `1px solid #dddddd`
- Radius: 8px
- Shadow: none or very subtle `rgba(0,0,0,0.06) 0px 4px 16px`
- Structure: Thumbnail image → Category label → Title → Description → Link
- Image: WebP format, top-rounded corners, 16:9 or square ratio

**Service Card**
- Background: `#f7f7f7` or `#ffffff`
- Radius: 8px
- Content: Icon/illustration + Service name (semibold 24px) + 1–2 sentence description + "Learn More" link
- No border — separation achieved by background color

**Product Card**
- Background: `#ffffff`
- Border: `1px solid #dddddd`
- Radius: 8px
- Hover: subtle border color shift or shadow lift
- Content: Product image + Product name + Brief tagline + CTA link

**Case Study Card**
- Background: `#ffffff`
- Radius: 8px
- Structure: Hero image (top, 16:9) + Company name + Outcome headline + Body text
- Key metric displayed prominently (e.g., "85% 비용 절감") in bold accent size

**Statistics / Metric Display**
- Large number: Pretendard 48px+ weight 700, color `#191919` or gradient text
- Suffix (++, %): same weight, slightly smaller
- Label below: 16px weight 400, color `#777`
- Example: `8000++ Clients`, `2700++ Employees`, `9 Global Offices`

### Navigation

**Global Header**
- Background: `#ffffff` (light mode) with option for transparent-over-hero
- Height: 64px–72px
- Logo: MegazoneCloud logotype, left-aligned
- Links: Pretendard 15px–16px weight 500, color `#191919`
- Hover: color shift to `#414aff`
- CTA: Blue button ("문의하기") right-aligned, 8px radius
- Mobile: hamburger collapse
- Variant `.header-color-white`: white logo and link text for use over dark sections

### Industry Icon Grid
- 9 icons in a 3×3 grid (desktop) → horizontal scroll (mobile)
- Each item: SVG icon (monochrome or brand-colored) + Label (14px weight 500)
- Industries: Manufacturing, Public, Software, Finance, Healthcare, Retail, Game, Telco/Media, Data & AI

### Badges / Tags
- Background: `rgba(65,74,255,0.08)` (tinted blue) or `#f0f0f0`
- Text: `#414aff` or `#191919`
- Padding: 4px 10px
- Radius: 4px or 9999px (pill)
- Font: 12px–14px weight 500
- Use: Certification labels, product category tags, "New" indicators

### Certification Strip (Footer area)
- Row of certification badges: ISMS-P, ISO 42001, ISO 27001, ISO 27018, ACT ACERTi
- Small logo + text label per badge
- Muted gray treatment — supportive, not decorative

---

## 5. Layout Principles

### Spacing System
- Base unit: `0.25rem` (4px) via Tailwind CSS `--spacing` token
- Common spacing values: 4px, 8px, 12px, 16px, 24px, 32px, 48px, 64px, 80px, 96px
- Section vertical padding: 80px–96px (desktop), 48px–64px (mobile)

### Grid & Container
- Max content width: approximately 1280px, centered with auto horizontal margins
- Section inner container: 1200px max-width
- Default grid columns:
  - Hero: single column, full-width
  - Services: 1 column (stacked vertical, with internal 2-col text+image split)
  - Industries: 3 columns (icon grid)
  - Products: 2–3 columns card grid
  - Case Studies: 2 columns
  - Resources/News: 4 columns (desktop), 2 columns (tablet), 1 column (mobile)

### Whitespace Philosophy
- **Professional breathing room**: 80px+ vertical rhythm between major sections — enterprise content requires space for cognitive processing, not visual density.
- **Alternating backgrounds**: White → Light Gray (`#f7f7f7`) → White → Medium Gray (`#f0f0f0`) cycles create visual rhythm without explicit section borders.
- **Card internal padding**: 24px–32px — generous enough to read as premium, not bloated.
- **Image-content balance**: Most feature sections use a 60:40 or 50:50 split — product image paired with explanatory text.

### Border Radius Scale
- Micro (4px): Small badges, tag pills, tooltips
- Standard (8px / `--radius-lg`): Buttons, cards, containers, inputs — the system default
- Large (12px–16px): Hero feature panels, modal dialogs, prominent callout blocks
- Full Pill (9999px): Selected badge variants, toggle switches

---

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat (Level 0) | No shadow, solid background | Section backgrounds, text blocks |
| Border (Level 1) | `1px solid #dddddd` | Standard cards, dividers, input outlines |
| Soft Lift (Level 2) | `rgba(0,0,0,0.06) 0px 4px 16px` | Hovered cards, dropdown menus |
| Modal (Level 3) | `rgba(0,0,0,0.12) 0px 8px 32px` | Modals, floating panels, sticky navigation |
| Focus (Accessibility) | `2px solid #414aff` outline | Keyboard focus on all interactive elements |

**Shadow Philosophy**: MegazoneCloud's shadow system is minimal by design. The enterprise B2B audience expects clarity and precision over visual drama. Shadows appear only on hover states and floating elements — never as a baseline card treatment. Depth is communicated primarily through background color changes (white → light gray alternation) rather than shadow elevation. This keeps the interface feeling clean and performant.

### Decorative Depth
- **Gradient text**: Hero headlines rendered with the full-spectrum gradient as `background-clip: text` — creates the appearance of the gradient living inside the letterforms.
- **Gradient bands**: Thin horizontal gradient stripes (`--color-gradient`) used as section accent lines or hero underline elements.
- **Dark section immersion**: When background shifts to `#000`, the AI spectrum gradient becomes the primary light source — gradient elements glow against pure black.

---

## 7. Do's and Don'ts

### Do
- Apply the full-spectrum gradient (`linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1)`) only to hero headlines and signature accent elements — not decoratively throughout
- Use `#414aff` (Point Blue) as the exclusive interactive color for links, CTAs, and focus rings
- Set all primary body text in Pretendard 400 / `#191919` on white or light gray backgrounds
- Alternate section backgrounds in the sequence: `#fff` → `#f7f7f7` → `#f0f0f0` → `#000` (for immersive moments)
- Keep border-radius at 8px for all interactive components — the system is conservative, not playful
- Display key metrics (client counts, savings percentages) in large, bold Pretendard with the gradient or `#191919` color
- Include the multilingual font stack: `Pretendard, 'Noto Sans JP', 'Noto Sans SC', sans-serif`
- Use the two-gradient-stop subsets (gradient-01_*, gradient-02_*) for individual cards or icons rather than the full five-color spectrum

### Don't
- Don't apply the full five-color gradient to buttons, form elements, or navigation — it is a headline treatment only
- Don't use Point Green (`#32ef7a`), Point Purple (`#8920ff`), or Point Pink (`#ff41c1`) as standalone interactive colors — they exist only within gradient contexts
- Don't use warm grays — MegazoneCloud's neutrals are cool/neutral toned (`#f7f7f7`, `#f0f0f0`), not warm beige
- Don't add heavy multi-layer shadows to cards — one subtle shadow on hover maximum
- Don't use border-radius above 16px on rectangular containers — pill shapes are reserved for small badge elements only
- Don't center-align body text in sections longer than 2 lines — left-align for reading comfort
- Don't use font-weight below 400 in body text — light (300) is reserved for large display-only contexts
- Don't mix gradient variants arbitrarily — each gradient-02_* variant has directional intent (green-to-blue, cyan-to-purple, pink-to-blue)

---

## 8. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | < 640px | Single column, stacked sections, reduced heading sizes |
| Small (sm) | ≥ 640px | 2-column grids begin, expanded card layouts |
| Large (lg) | ≥ 1024px | Full desktop layout, 3–4 column grids |
| XL | ≥ 1280px | Maximum content width, generous margins |

### Touch Targets
- Buttons: minimum 44px height via padding 12px–16px
- Navigation links: 48px+ touch-friendly areas
- Cards: entire card surface clickable (not just the "Learn More" link)
- Mobile hamburger: minimum 44×44px tap target

### Collapsing Strategy
- Hero headline: 60px → 40px → 28px (maintains weight 700, adjusts size)
- Section grids: 4-column → 2-column → 1-column stacked
- Navigation: full horizontal nav → hamburger menu with full-screen overlay
- Industry icons: 3-column fixed grid → horizontal scroll on mobile
- Case study cards: 2-column → 1-column stacked, images above text
- Footer: multi-column → stacked single column
- Section padding: 80px → 48px on mobile

### Image Behavior
- All images use WebP format for performance
- Product/case images maintain 16:9 aspect ratio at all breakpoints
- Logo grid in footer maintains horizontal scroll rather than wrapping on mobile
- Certification badges compress to smaller size on mobile

---

## 9. Agent Prompt Guide

### Quick Color Reference
- Primary CTA / Links: Point Blue (`#414aff`)
- Background (primary): White (`#ffffff`)
- Background (alt 1): Light Gray (`#f7f7f7`)
- Background (alt 2): Medium Gray (`#f0f0f0`)
- Background (dark): Black (`#000000`)
- Heading text: Dark Gray (`#191919`)
- Body text: Dark Gray (`#191919`)
- Secondary text: Gray (`#777777`)
- Muted text: Medium Gray (`#aaaaaa`)
- Border / Divider: Line Gray (`#dddddd`)
- Focus ring: Point Blue (`#414aff`)
- Brand gradient (full): `linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1)`

### Example Component Prompts

**Hero Section**
```
Create a hero section on white (#fff) background.
Headline: Pretendard 60px weight 700, line-height 1.15, color #191919.
Apply gradient text treatment to the keyword phrase:
  background: linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1);
  -webkit-background-clip: text; -webkit-text-fill-color: transparent;
Subtitle: 20px weight 400, line-height 1.6, color #777.
CTA button: #414aff background, white text, Pretendard 16px weight 600, 8px radius, 12px 24px padding.
Ghost button beside it: transparent bg, 1px solid #414aff border, #414aff text, same sizing.
```

**Standard Content Card**
```
Design a content card: white (#fff) background, 1px solid #ddd border, 8px border-radius.
Hover shadow: rgba(0,0,0,0.06) 0px 4px 16px, transition 150ms ease.
Top image: 16:9 ratio, WebP, 8px top radius (matching card radius).
Category tag: 12px Pretendard weight 500, #414aff color, rgba(65,74,255,0.08) background, 4px radius, 4px 10px padding.
Title: 24px Pretendard weight 600, #191919, line-height 1.4.
Body: 14px–16px Pretendard weight 400, #777, line-height 1.6.
Footer: "Learn More" link in #414aff, 14px weight 500, underline on hover.
Card padding: 24px.
```

**Metric / Statistics Display**
```
Create a statistics block: 3 metrics in a row.
Each metric: number at 48px Pretendard weight 700, color #191919 (or gradient-text treatment).
Suffix "++" at same weight, slightly smaller (36px).
Label below: 16px weight 400, #777, margin-top 8px.
Examples: "8000++ Clients", "2700++ Employees", "9 Global Offices".
No card border — white background, generous spacing 48px between items.
```

**Navigation**
```
Build a global header: white (#fff) background, height 64px, bottom border 1px solid #f0f0f0.
Logo: MegazoneCloud logotype, left-aligned.
Nav links: Pretendard 15px weight 500, color #191919. Hover: color #414aff, transition 150ms.
Right side: "문의하기" button — #414aff background, white text, Pretendard 15px weight 600, 8px radius, 10px 20px padding.
Mobile: hamburger button, min 44×44px tap target.
```

**Dark Immersive Section**
```
Create a dark feature section: #000 background.
Headline: Pretendard 40px weight 700, white (#fff) text.
Gradient accent line below headline: height 2px, full-spectrum gradient:
  linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1)
Body: 16px weight 400, color #aaa (medium gray for dark bg readability).
CTA button: white background, #191919 text, 8px radius, 12px 24px padding.
Section padding: 96px vertical.
```

**Industry Icon Grid**
```
Create a 3×3 icon grid (desktop), horizontal scroll (mobile).
Each cell: SVG icon (48×48px) centered + label below (14px Pretendard weight 500, #191919).
Cell background: transparent, hover: #f7f7f7 background, 8px radius, transition 150ms.
Grid gap: 24px.
9 industries: Manufacturing, Public, Software, Finance, Healthcare, Retail, Game, Telco/Media, Data & AI.
```

### Iteration Guide
1. The five-color AI gradient is MegazoneCloud's single most recognizable brand element — use it deliberately on 1–2 elements per view, not decoratively everywhere
2. Point Blue (`#414aff`) is the only standalone interactive color — all links, CTAs, focus rings use it
3. Neutral palette is strictly cool/gray — avoid warm beige, cream, or yellow-tinted backgrounds
4. Typography uses weight contrast over size contrast: jump directly from 400 (body) to 600–700 (headings)
5. Cards use a single subtle border (`1px solid #ddd`) at rest — shadow appears only on hover
6. Section backgrounds alternate White → Light Gray → Medium Gray → Black for cinematic pacing
7. All interactive elements receive `2px solid #414aff` focus ring for keyboard accessibility
8. Pretendard weight range 100–900 is available — use 700 for display, 600 for card titles, 500 for UI labels, 400 for body

---

## Appendix: CSS Token Reference

```css
/* Background */
--color-bg-white: #ffffff;
--color-bg-light-gray: #f7f7f7;
--color-bg-medium-gray: #f0f0f0;
--color-bg-dark-gray: #777777;
--color-bg-black: #000000;

/* Text */
--color-text-dark-gray: #191919;
--color-text-black: #000000;
--color-text-white: #ffffff;
--color-text-gray: #777777;
--color-text-medium-gray: #aaaaaa;
--color-text-light-gray: silver;
--color-text-red: red;

/* Point / Accent */
--color-point-green: #32ef7a;
--color-point-light-blue: #00d7f8;
--color-point-blue: #414aff;
--color-point-purple: #8920ff;
--color-point-pink: #ff41c1;

/* Line */
--color-line-gray: #dddddd;

/* Gradients */
--color-gradient: linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1);
--color-gradient-01_01: linear-gradient(118deg, #32ef7a 20.19%, #00d7f8);
--color-gradient-01_02: linear-gradient(304deg, #414aff 45.28%, #00d7f8 105.07%);
--color-gradient-01_03: linear-gradient(314deg, #8920ff 22.12%, #414aff);
--color-gradient-01_04: linear-gradient(127deg, #ff41c1 -15.74%, #8920ff 59.05%);
--color-gradient-02_01: linear-gradient(116deg, #32ef7a 10.37%, #414aff 85.62%);
--color-gradient-02_02: linear-gradient(132deg, #00d7f8 -21.51%, #8920ff 66.38%);
--color-gradient-02_03: linear-gradient(125deg, #ff41c1 -10.23%, #414aff 88.92%);

/* Spacing & Radius */
--spacing: 0.25rem;      /* 4px base unit */
--radius-lg: 0.5rem;     /* 8px — system default radius */

/* Typography scale */
--text-sm: 0.875rem;     /* 14px */
--text-base: 1rem;       /* 16px */
--text-lg: 1.125rem;     /* 18px */
--text-xl: 1.25rem;      /* 20px */
--text-2xl: 1.5rem;      /* 24px */
--text-3xl: 1.875rem;    /* 30px */
--text-4xl: 2.25rem;     /* 36px */

/* Font weights */
--font-weight-medium: 500;
--font-weight-semibold: 600;
--font-weight-bold: 700;

/* Line heights */
--leading-tight: 1.25;
--leading-relaxed: 1.625;

/* Transition */
transition: all 150ms cubic-bezier(0.4, 0, 0.2, 1);
```

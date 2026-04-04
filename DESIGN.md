# Design System: roserenuu

## 1. Visual Theme & Atmosphere

roserenuu is a personal UGC creator portfolio designed to attract brand deals. The design philosophy is **bold confidence meets editorial clarity** — a site that feels like a premium media kit, not a generic freelancer template. It balances the personality of a content creator with the trust signals brands need to commit to a partnership.

The palette is built on a near-white canvas (`#fafaf9`) that avoids the clinical coldness of pure white. The primary accent is an electric coral-orange (`#FF4D2D`) — energetic and memorable, cutting through the noise without feeling garish. Dark surfaces use a near-black with warm undertones (`#111110`) rather than pure black, keeping the contrast human rather than harsh.

Typography is anchored by **Inter**, a clean geometric sans-serif. Headlines use heavy weights (800) with tight negative letter-spacing, creating a commanding visual presence. Body text stays at a readable 400–500 weight with generous line-height. Numbers and metrics are displayed large and bold — brands care about reach and engagement, so those figures should own the screen.

The overall feel: a creator who takes their work seriously. No gradients, no clutter. Clean grids, deliberate whitespace, and one punchy accent color applied with restraint.

**Key Characteristics:**
- Inter with aggressive negative letter-spacing at display sizes (-2px at 56px+)
- Near-white canvas (`#fafaf9`) + near-black text (`#111110`) with warm undertones
- Electric coral-orange (`#FF4D2D`) as the singular accent — CTAs, highlights, active states
- Thin `1px solid rgba(0,0,0,0.08)` borders throughout — structural but never heavy
- Subtle multi-layer shadows for card depth — felt, not seen
- 8px base spacing unit with a clean 4x scale
- Portfolio-grid layouts and metric cards as primary storytelling tools

## 2. Color Palette & Roles

### Primary
- **Near-Black** (`#111110`): All headings, primary body text, navbar, footer text.
- **Near-White Canvas** (`#fafaf9`): Page background. Warm tint avoids sterile feel.
- **Electric Coral** (`#FF4D2D`): Primary CTA buttons, active links, highlights, hover accents. The sole saturated color in UI chrome — use sparingly and with purpose.

### Brand Secondary
- **Coral Dark** (`#D93A1E`): Button active/pressed state, stronger emphasis.
- **Coral Pale** (`#FFF1EE`): Badge backgrounds, tinted surfaces, highlights behind metrics.

### Neutral Scale
- **Surface** (`#f4f3f1`): Section alternation background, card fill, subtle dividers.
- **Border** (`rgba(0,0,0,0.08)`): Standard card and section borders — whisper-weight.
- **Mid Gray** (`#6b6b6b`): Body descriptions, secondary labels, sub-headings.
- **Muted Gray** (`#9b9b9b`): Captions, placeholder text, timestamps, metadata.
- **Light Rule** (`#e8e7e5`): Horizontal rules, dividers between sections.

### Interactive
- **Link Coral** (`#FF4D2D`): Inline links and icon links.
- **Focus Ring** (`#FF4D2D`): 2px focus outline for all keyboard-interactive elements.
- **Hover Surface** (`rgba(255,77,45,0.06)`): Subtle background wash on hoverable cards.

### Semantic
- **Success Green** (`#16a34a`): Partnership confirmed, available status.
- **Amber** (`#d97706`): In-progress, pending review.
- **Info Blue** (`#2563eb`): Informational callouts, external links.

### Shadows & Depth
- **Card Shadow** (`rgba(0,0,0,0.05) 0px 2px 12px, rgba(0,0,0,0.03) 0px 1px 4px`): Standard card elevation.
- **Hover Shadow** (`rgba(0,0,0,0.08) 0px 8px 24px, rgba(0,0,0,0.04) 0px 2px 8px`): Lifted state on hovered cards.
- **Modal Shadow** (`rgba(0,0,0,0.12) 0px 16px 48px, rgba(0,0,0,0.06) 0px 4px 16px`): Overlays, modals, dropdowns.

## 3. Typography Rules

### Font Family
- **Primary**: `Inter`, with fallbacks: `-apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, Arial, sans-serif`
- **Monospace** (metrics/numbers): `"JetBrains Mono", "Fira Code", monospace` — used for stat counters and metric displays.

### Hierarchy

| Role | Size | Weight | Line Height | Letter Spacing | Notes |
|------|------|--------|-------------|----------------|-------|
| Display Hero | 60px (3.75rem) | 800 | 1.0 | -2.0px | Name, main headline |
| Display Sub | 48px (3.00rem) | 800 | 1.05 | -1.5px | Section headings |
| Headline Large | 36px (2.25rem) | 700 | 1.1 | -1.0px | Feature titles, portfolio section titles |
| Headline | 26px (1.63rem) | 700 | 1.2 | -0.5px | Card titles, sub-section headers |
| Sub-heading | 20px (1.25rem) | 600 | 1.3 | -0.25px | Intro paragraphs, featured descriptions |
| Body | 16px (1.00rem) | 400 | 1.6 | normal | Standard reading text |
| Body Medium | 16px (1.00rem) | 500 | 1.6 | normal | Navigation, emphasized UI text |
| Label | 14px (0.88rem) | 600 | 1.4 | 0.05em | Badges, tags, category labels (UPPERCASE) |
| Caption | 14px (0.88rem) | 400 | 1.5 | normal | Metadata, dates, platform names |
| Micro | 12px (0.75rem) | 500 | 1.4 | 0.05em | Tiny labels, timestamps |
| Metric Number | 48px (3.00rem) | 800 | 1.0 | -1.5px | Follower counts, engagement rates — monospace |

### Principles
- **Weight as hierarchy**: 400 for reading, 500 for interaction, 600 for labels, 700 for headings, 800 for display. Never skip more than one step.
- **Tight at top**: Display text uses -2.0px letter-spacing. Relaxes to normal at body size. Headlines breathe; bodies read.
- **Uppercase labels**: 14px weight 600 with `letter-spacing: 0.05em` and `text-transform: uppercase` for category labels, platform badges, and section eyebrows. Creates editorial structure.
- **Metric display**: Use monospace for numbers in stats/metrics — it aligns digits and feels data-authoritative.

## 4. Component Stylings

### Buttons

**Primary Coral CTA**
- Background: `#FF4D2D`
- Text: `#ffffff`, 15px Inter weight 600
- Padding: 12px 24px
- Radius: 6px
- Border: none
- Hover: `#D93A1E` background, translateY(-1px), hover shadow
- Active: `#C03218`, scale(0.98)
- Focus: `2px solid #FF4D2D` outline, 2px offset
- Use: "Work With Me", "Download Media Kit", primary actions

**Secondary / Outline**
- Background: transparent
- Border: `1.5px solid #111110`
- Text: `#111110`, 15px weight 600
- Padding: 11px 24px
- Radius: 6px
- Hover: `#111110` bg, `#ffffff` text
- Use: "View Portfolio", "See More Work"

**Ghost / Text Link**
- Background: transparent
- Text: `#FF4D2D`, 15px weight 500
- Decoration: underline-offset 3px on hover
- Use: inline CTAs, "View all →"

**Tag / Badge Button**
- Background: `#FFF1EE`
- Text: `#FF4D2D`, 12px weight 600, uppercase, letter-spacing 0.05em
- Padding: 4px 10px
- Radius: 4px
- Use: content categories ("BEAUTY", "LIFESTYLE", "TECH")

### Cards & Containers

**Portfolio Card**
- Background: `#ffffff`
- Border: `1px solid rgba(0,0,0,0.08)`
- Radius: 12px
- Shadow: card shadow (2-layer, max 0.05 opacity)
- Hover: hover shadow + translateY(-2px)
- Aspect ratio: 9:16 (vertical video) or 1:1 (square content)
- Overlay on hover: semi-transparent dark overlay with play/view icon

**Metric / Stat Card**
- Background: `#fafaf9`
- Border: `1px solid rgba(0,0,0,0.08)`
- Radius: 10px
- Padding: 24px
- Number: 48px Inter weight 800, monospace, `#111110`
- Label: 13px weight 600, uppercase, `#9b9b9b`, letter-spacing 0.08em
- Use: follower count, avg engagement rate, brand collaborations count

**Brand Logo Card**
- Background: `#ffffff`
- Border: `1px solid rgba(0,0,0,0.08)`
- Radius: 8px
- Padding: 20px 28px
- Logo: grayscale by default, full color on hover
- Use: "Brands I've Worked With" section

**Testimonial Card**
- Background: `#f4f3f1`
- Radius: 12px
- Padding: 28px 32px
- Quote: 18px Inter weight 400, line-height 1.6, `#111110`
- Attribution: 14px weight 600, `#6b6b6b`
- Accent line: 3px coral left border

### Navigation
- Fixed top, white background with `border-bottom: 1px solid rgba(0,0,0,0.08)`
- Logo/Name: Inter 18px weight 800, `#111110`, letter-spacing -0.5px
- Links: Inter 15px weight 500, `#6b6b6b`, hover `#111110`
- Active link: `#FF4D2D`
- CTA button: Primary Coral CTA ("Work With Me"), right-aligned
- Mobile: hamburger collapse, full-screen nav overlay

### Forms / Contact
- Label: 14px weight 600, `#111110`
- Input: white background, `1px solid rgba(0,0,0,0.15)` border, 8px radius, 12px 16px padding
- Focus: `1px solid #FF4D2D`, coral glow (`box-shadow: 0 0 0 3px rgba(255,77,45,0.12)`)
- Placeholder: `#9b9b9b`
- Submit: Primary Coral CTA full-width

### Section Eyebrow Pattern
- Uppercase label in coral (`#FF4D2D`), 12px weight 600, letter-spacing 0.1em
- Followed by large heading at display/headline size
- Sub-description at 18px weight 400, `#6b6b6b`, max-width 560px

## 5. Layout Principles

### Spacing System
- Base unit: 8px
- Scale: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64, 80, 96, 128px
- Section vertical padding: 80–96px on desktop, 48–64px on mobile
- Card grid gaps: 20–24px

### Grid & Container
- Max content width: 1100px, centered
- Hero: full-width with centered content, generous top padding (120px desktop)
- Portfolio grid: 3-column on desktop, 2-column tablet, 1-column mobile (9:16 cards)
- Stats row: 4-column horizontal strip
- Brand logos: 5–6 column grid, responsive wrap
- Section alternation: white (`#ffffff`) and surface (`#f4f3f1`) backgrounds

### Whitespace Philosophy
- **Content leads**: Every section breathes with 80px+ vertical margins. No cramming.
- **Hero dominates**: The name/title hero gets maximum real estate — 100vh or close. First impression matters for brand deals.
- **Grid density in portfolios only**: The work grid can be tighter (20px gaps) — the richness comes from the content itself.
- **Metrics earn space**: Stat cards are large format. Numbers like "2.4M followers" should be unmissable.

### Border Radius Scale
- Sharp (4px): Tags, badges, small labels
- Subtle (6px): Buttons, inputs
- Standard (10–12px): Cards, containers
- Large (16px): Hero content blocks, featured sections
- Full (9999px): Availability status pill

## 6. Depth & Elevation

| Level | Treatment | Use |
|-------|-----------|-----|
| Flat | No shadow, thin border | Page background, text sections |
| Card | 2-layer shadow (max 0.05) + border | Portfolio cards, stat cards |
| Lifted | 2-layer shadow (max 0.08) + translateY(-2px) | Hovered cards |
| Overlay | 3-layer shadow (max 0.12) | Modals, image lightbox |
| Nav | `border-bottom: 1px solid rgba(0,0,0,0.08)` only | Sticky navigation |

**Shadow Philosophy**: Shadows use 2 layers max — a wide ambient layer and a tighter contact shadow. Individual opacity never exceeds 0.12. The goal is natural lift, not theatrical depth. Cards should feel like physical media laid on a surface.

## 7. Responsive Behavior

### Breakpoints
| Name | Width | Key Changes |
|------|-------|-------------|
| Mobile | <640px | Single column, stacked hero, nav collapse |
| Tablet | 640–1024px | 2-column portfolio, reduced padding |
| Desktop | 1024–1280px | 3-column portfolio, full layout |
| Wide | >1280px | Centered max-width, generous side margins |

### Collapsing Strategy
- Hero headline: 60px → 40px → 30px, letter-spacing scales proportionally
- Portfolio grid: 3-col → 2-col → 1-col
- Stats row: 4-col → 2x2 grid → stacked
- Brand logos: 5-col → 3-col → 2-col
- Navigation: horizontal → hamburger with full-screen overlay
- Section padding: 96px → 64px → 48px

### Touch Targets
- All buttons minimum 44px height
- Card tap areas are the full card surface
- Navigation links: 48px tap height on mobile

## 8. Accessibility & States

### Focus System
- All interactive elements: `2px solid #FF4D2D` outline, 2px offset
- Focus is never hidden — `:focus-visible` used to avoid visible ring on mouse click
- High contrast: `#111110` on `#fafaf9` exceeds WCAG AAA

### Interactive States
- **Default**: Standard appearance
- **Hover**: Cards lift (translateY -2px + shadow), buttons darken, links gain underline
- **Active**: scale(0.97) on buttons, darker background variant
- **Focus**: Coral outline ring
- **Disabled**: 40% opacity, cursor not-allowed

### Color Contrast
- Primary text (`#111110`) on canvas (`#fafaf9`): ~18:1 (WCAG AAA)
- Secondary text (`#6b6b6b`) on white: ~5.7:1 (WCAG AA)
- Coral CTA (`#FF4D2D`) on white: ~3.8:1 (WCAG AA for large text/UI)
- White text on coral button: ~3.8:1 (WCAG AA)

## 9. Agent Prompt Guide

### Quick Color Reference
- Page background: Near-White Canvas (`#fafaf9`)
- Alt background: Surface (`#f4f3f1`)
- Primary text: Near-Black (`#111110`)
- Secondary text: Mid Gray (`#6b6b6b`)
- Muted text: Muted Gray (`#9b9b9b`)
- Accent / CTA: Electric Coral (`#FF4D2D`)
- Accent dark: Coral Dark (`#D93A1E`)
- Accent pale: Coral Pale (`#FFF1EE`)
- Border: `1px solid rgba(0,0,0,0.08)`
- Card shadow: `rgba(0,0,0,0.05) 0px 2px 12px, rgba(0,0,0,0.03) 0px 1px 4px`

### Example Component Prompts
- "Build the hero section on `#fafaf9`. Name at 60px Inter weight 800, line-height 1.0, letter-spacing -2.0px, color `#111110`. Tagline at 20px weight 400, line-height 1.6, color `#6b6b6b`, max-width 520px. Two buttons: Primary coral (`#FF4D2D`, 12px 24px padding, 6px radius, white 600-weight text) and outline (1.5px solid `#111110`, same size)."
- "Create a portfolio grid: 3 columns, 20px gap, cards with 12px radius, `1px solid rgba(0,0,0,0.08)` border, card shadow. Cards are 9:16 aspect ratio with cover image. On hover: translateY(-2px), hover shadow (`rgba(0,0,0,0.08) 0px 8px 24px`), semi-transparent dark overlay with centered white view icon."
- "Design a stats strip: 4 columns, each card with 24px padding, `#fafaf9` background, `1px solid rgba(0,0,0,0.08)` border, 10px radius. Number at 48px Inter weight 800, monospace, `#111110`, letter-spacing -1.5px. Label at 13px weight 600 uppercase `#9b9b9b`, letter-spacing 0.08em."
- "Build a brand logo grid on `#f4f3f1` background: 5–6 columns, logos grayscale at 50% opacity by default, transition to full color at 100% opacity on hover. Cards: white bg, `1px solid rgba(0,0,0,0.08)` border, 8px radius, 20px 28px padding."
- "Create a testimonial card: `#f4f3f1` background, 12px radius, 28px 32px padding, `border-left: 3px solid #FF4D2D`. Quote text 18px Inter weight 400, line-height 1.6, `#111110`. Attributor name 14px weight 600 `#6b6b6b`."
- "Build sticky navigation: white background, `border-bottom: 1px solid rgba(0,0,0,0.08)`. Creator name left: 18px Inter weight 800 `#111110`. Nav links: 15px weight 500 `#6b6b6b`, hover `#111110`. Right: coral CTA button 'Work With Me' (#FF4D2D bg, white text, 6px radius, 10px 20px padding)."

### Iteration Guide
1. Keep coral (`#FF4D2D`) rare — it should feel like a highlight, not wallpaper. Use it for CTAs, hover states, active links, and accent borders only.
2. Near-black (`#111110`) and near-white (`#fafaf9`) carry the page — they have warm undertones, never use pure `#000` or `#fff` as primary surfaces.
3. Alternate sections between `#fafaf9` (canvas) and `#f4f3f1` (surface) — subtle rhythm without harsh color breaks.
4. Metrics and follower counts earn monospace, large weight (800), and their own stat cards — brands scan for these numbers first.
5. Portfolio cards should be media-first with minimal chrome. Let the content speak.
6. Uppercase eyebrow labels (`12px, weight 600, letter-spacing 0.1em`) before every major section heading create editorial hierarchy.
7. Letter-spacing tightens with size: -2.0px at 60px, -1.5px at 48px, -0.5px at 26px, normal at 16px.
8. The "Work With Me" or "Book Me" CTA must appear in the hero, nav, and at the bottom — brands should never have to hunt for how to contact you.

<!-- SEED: re-run /impeccable document once there's code to capture the actual tokens and components. -->

---
name: Walkadoodle
description: A warm, playful dog-walking service for families who treat their pets like family.
---

# Design System: Walkadoodle

## 1. Overview

**Creative North Star: "The Neighborhood Badge"**

Walkadoodle's visual system is built around the energy of a trusted neighborhood institution — the dog walker everyone knows by name, whose reputation travels by word of mouth, whose badge of quality is worn-in rather than polished-up. The medallion logo isn't an accident; it's the whole brand posture. Warm without being saccharine. Playful without being childish. Dependable enough that a protective pet owner hands over the leash.

The palette is unambiguously purple — committed, confident, community-rooted — with a warm gold ring accent that says "established" without saying "corporate." White space breathes; the purple does the talking. Imagery carries the emotional weight: real dogs, real moments, the specific joy of a happy animal mid-walk. Typography pairs a rounded, characterful display face with a clean humanist body. Headlines feel like they could have been hand-lettered on the side of a neighborhood shop; body copy is transparent and readable, never styled for its own sake.

Motion is responsive: alive enough to feel considered, restrained enough to let the content lead. Smooth hover feedback, clean transitions — no orchestrated entrances, no scroll choreography. The dogs are interesting enough on their own.

This system explicitly rejects the sanitized startup landing page (gradient hero, feature-card grid, stat counters) and the cold-corporate register (navy and gray, stock handshakes, faceless "social proof"). It equally rejects the opposite failure mode: cheap cutesy pet-brand energy — cartoon paw prints scattered like confetti, garish discount-store color. Warmth and charm must come from craft, not novelty.

**Key Characteristics:**
- Purple as a committed surface color (30–60% of key sections), not a ≤10% accent
- Real dog photography as the primary emotional carrier
- Rounded display type (Baloo 2) for headlines; transparent humanist body (Lato)
- Responsive motion — smooth feedback without choreographed section entrances
- Warm gold as a sparse quality signal, never a background
- White as the resting ground; purple does the committing

## 2. Colors

The palette is committed purple. The brand color carries the identity on every key surface — hero, CTA, key feature sections. Hedging with beige neutrals at the edges is explicitly prohibited.

### Primary

- **Brand Purple** (`~oklch(0.42 0.20 305)` — to be resolved during implementation; sample from logo wordmark): The dominant brand color, lifted directly from the Walkadoodle logo. Used on hero backgrounds, primary CTA buttons, active navigation states, and any section meant to carry the brand's full voice. At this lightness and chroma it reads as rich and confident — not dark-mode mysterious, not corporate navy.
- **Purple Deep** (`~oklch(0.32 0.18 305)` — to be resolved): Hover and pressed states for CTA buttons on white backgrounds. Same hue, dropped lightness. Never used as a standalone background.
- **Purple Light** (`~oklch(0.72 0.14 305)` — to be resolved): Tinted accents and hover highlights when Brand Purple would be too heavy. Used sparingly — its rarity is what makes the committed primary land.

### Secondary

- **Badge Gold** (`~oklch(0.72 0.10 75)` — to be resolved; derived from logo medallion ring): Muted warm gold, the secondary quality signal. Used for feature badges, rating accents, selected states, and focus rings. Never used as a section background or body text color — only as a sparse earned accent on white or purple surfaces.

### Neutral

- **Site White** (`#FFFFFF`): The primary resting background. Truly white — no warm tint, no sand. All warmth is carried by the purple, gold, type voice, and photography. A cream or beige background is prohibited.
- **Near-White Surface** (`~oklch(0.97 0.005 305)` — to be resolved): Cards, elevated containers, photo caption backgrounds. A near-imperceptible purple tint at negligible chroma. Cooler than sand, warmer than cool gray, and recognizably from the brand hue.
- **Ink** (`~oklch(0.18 0.04 305)` — to be resolved): Body text and high-emphasis UI text. A very dark purple-tinted near-black — warmer than pure `#000000`, readable on white and on Brand Purple backgrounds.
- **Muted Ink** (`~oklch(0.45 0.03 305)` — to be resolved): Secondary text, captions, metadata. Must clear 4.5:1 against Site White; do not lighten further.

**The Committed Purple Rule.** Purple is not a ≤10% accent. It carries the brand. A hero, a CTA section, a features band — any key surface should be willing to go full Brand Purple. A site where purple appears only on buttons has not committed to this identity.

**The No-Cream Rule.** The background is white (`#FFFFFF`). No warm tints, no sand, no beige, no cream. The body background staying clean and uncontested is what lets the purple and gold read. Any warm-tinted near-white body background is the AI default of 2026 and is prohibited.

## 3. Typography

**Display Font:** Baloo 2 (Google Fonts — `family=Baloo+2:wght@400;600;700;800`)
**Body Font:** Lato (Google Fonts — `family=Lato:wght@400;700`)

**Character:** Baloo 2 carries the logo's rounded warmth into every headline — the character of hand-lettering without the wobble, presence at large sizes without shouting. Lato disappears into the reading experience as good body type should: humanist proportions, optimal x-height, no agenda. The pairing works on a contrast axis (rounded display personality versus transparent humanist) rather than pairing two similar warm faces. No reflex-reject fonts are used.

### Hierarchy

- **Display** (Baloo 2, 800, `clamp(2.8rem, 7vw, 5.5rem)`, line-height 1.05, letter-spacing -0.02em): Hero headlines and primary section statements. The first thing a visitor reads; they carry the brand voice. `text-wrap: balance` on all display headings.
- **Headline** (Baloo 2, 700, `clamp(1.8rem, 4vw, 2.8rem)`, line-height 1.15): Secondary section headers and feature names. Baloo 2 at this size reads as warm and confident.
- **Title** (Baloo 2, 600, `clamp(1.2rem, 2.5vw, 1.6rem)`, line-height 1.3): Subheadings, card titles, service names. Lighter Baloo 2 weight; the roundness reads as friendliness.
- **Body** (Lato, 400, 1rem / 16px, line-height 1.7, max 65ch): All prose copy. Lato Regular is transparent and readable. Line length capped at 65ch. `text-wrap: pretty` on multi-sentence paragraphs to reduce orphans.
- **Body Strong** (Lato, 700, 1rem / 16px): In-line emphasis within body copy. Lato Bold has sufficient weight contrast to read without color.
- **Label** (Lato, 600, 0.8rem / 12.8px, letter-spacing 0.04em): UI labels, form field labels, navigation items, small metadata. Labels only — never all-caps on body copy.

**The Baloo-for-Headings Rule.** Baloo 2 appears only in Display, Headline, and Title roles. Body copy, labels, and UI chrome use Lato. One font's personality, one font's transparency — never mixed at the same hierarchy level.

## 4. Elevation

This system is soft-lifted: surfaces are flat by default, and depth is introduced sparingly through ambient purple-tinted shadows and tonal surface layering (Near-White Surface cards against Site White). Harsh, gray, opaque box shadows are prohibited — they belong to a different brand register. The intention is warmth and approachability, not material depth.

Depth hierarchy: base canvas (Site White) → subtle container (Near-White Surface with no shadow) → interactive card (Near-White Surface + ambient shadow) → modal/dialog (white + heavier purple-glow shadow + overlay).

**The Soft-Lift Rule.** A card earns a shadow only to separate it from its background — never for decorative layering. The shadow is a purple-tinted ambient glow (`0 4px 24px oklch(0.42 0.20 305 / 0.10)` — to be resolved at implementation to the equivalent hex), not a neutral gray drop shadow. If an element is intentionally flat, no shadow.

## 5. Components

*To be populated on the next `/impeccable document` run once components are built. Seed mode omits this section — there are no components to document yet.*

## 6. Do's and Don'ts

### Do:
- **Do** use Brand Purple as a committed section background — hero, CTA band, feature callout. The purple leads; confining it to buttons only betrays the identity.
- **Do** show real dogs in every image-bearing section. Photography is the primary emotional carrier for this brand. One decisive, well-chosen photo beats five mediocre ones.
- **Do** write alt text in the brand voice: "a fluffy goldendoodle mid-stride on a sunny sidewalk" not "dog walking photo."
- **Do** use Badge Gold sparingly as a quality signal — on feature badges, rating indicators, selected UI states — sparse enough that it reads as earned.
- **Do** keep body text containers to 65ch max-width. Readable prose is a trust signal.
- **Do** apply `text-wrap: balance` on all Display and Headline elements.
- **Do** honor `prefers-reduced-motion`: every hover transition and entrance animation must have a reduced-motion fallback (typically a crossfade or instant state).
- **Do** keep Baloo 2 exclusively for Display, Headline, and Title. Lato for everything else.
- **Do** use purple-tinted shadows (not neutral gray) when elevation is needed.

### Don't:
- **Don't** use a cream, sand, beige, or warm-tinted near-white body background. That warmth is carried by the color system and photography — the background stays white. Warm-neutral backgrounds are the AI default of 2026 and are forbidden.
- **Don't** build the generic SaaS template: gradient hero → three feature-card grid → stat counters → "Trusted by" logo wall. This is an explicitly named anti-reference. If a layout could appear on any startup landing page, it needs to be redesigned.
- **Don't** go cold corporate: no navy-and-gray palettes, no stock-photo handshakes, no faceless enterprise "social proof" language. This brand has a heartbeat.
- **Don't** be cutesy. No cartoon paw-print repeat patterns, no clip-art dog illustrations used decoratively, no garish pet-store colors. Charm comes from craft — real photography, considered type, committed color — not from novelty symbols scattered across the page.
- **Don't** treat purple as a ≤10% accent. If a section has no purple, ask why.
- **Don't** place a colored `<div>` placeholder where a dog photograph belongs. Zero imagery on an image-led brief is a design failure, not restraint.
- **Don't** use Baloo 2 for body copy, labels, or UI chrome — it is a display face. Lato handles everything below Title level.
- **Don't** use gradient text (`background-clip: text` with a gradient), glassmorphism as default card treatment, or side-stripe border accents on cards or callouts. These are cross-register absolute prohibitions.
- **Don't** add a small uppercase tracked kicker above every section heading ("OUR SERVICES", "WHY WALKADOODLE", "PRICING"). One deliberate kicker is brand voice; one above every section is AI grammar.
- **Don't** use border-left as a colored accent stripe on cards or callouts. Always rewrite with a background tint or full border.

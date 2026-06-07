# Design Decisions

**Last updated:** May 2026  
**Media Director:** Lindsay Shea  
**Status:** Active — site in development

---

## Brand Architecture

**Organization:** Caring Sensor Community  
**Product:** Routine Stability  

Relationship: The Caring Sensor Community is the nonprofit that stewards the mission. Routine Stability is the product people encounter. Analogous to Mozilla Foundation / Firefox.

---

## Visual Direction

### Emotional Tone Brief

Every design decision should answer: *does this feel calm, human, and trustworthy?*

The person using this product is worried about someone they love. The interface should make them feel quietly reassured — not surveilled, not alarmed, not managed.

- If a design element increases anxiety → remove it
- If a design element could appear in a hospital system → remove it  
- If a design element could appear in a security dashboard → remove it

### Color System

| Token | Value | Usage |
|-------|-------|-------|
| `--background` | `#0B0D12` | Page backgrounds |
| `--gradient-start` | `#1a1060` | Deep indigo |
| `--gradient-end` | `#2d1b69` | Violet |
| `--accent-primary` | `#7c3aed` | Violet — dots, indicators |
| `--accent-secondary` | `#a855f7` | Soft magenta — glows |
| `--text-primary` | `#ffffff` | Headlines, active labels |
| `--text-secondary` | `rgba(255,255,255,0.65)` | Body copy |
| `--text-tertiary` | `rgba(255,255,255,0.35)` | Labels, timestamps |
| `--card-bg` | `rgba(255,255,255,0.04)` | Glassmorphism surfaces |
| `--card-border` | `rgba(255,255,255,0.08)` | Card borders |

### Typography

| Role | Typeface | Notes |
|------|----------|-------|
| Display / Headlines | Instrument Serif | Large, loose tracking, high contrast. Warm without being decorative. |
| UI / Body | Inter or Geist | Clean, modern, invisible when working. |
| Monospace (times, labels) | JetBrains Mono | Used sparingly. Timestamps, section labels. |

**Why serif for headlines:** The serif is a strategic signal, not a style choice. It communicates time, dignity, and trust earned slowly — which is the entire product philosophy. Every competitor uses sans-serif. The serif is the differentiation.

### Motion Principles

Three motion behaviors. No others during MVP.

1. **Feed entry arrival:** `opacity 0→1` over 400ms, `translateY 6px→0`. Staggered 80ms between entries. Triggers on load.
2. **AI card reveal:** `blur(8px)→blur(0)` over 600ms, `opacity 0→1`. Triggers on scroll into view.
3. **Background ambient pulse:** Hero gradient breathes. Opacity oscillates `100%→92%` over 8-second cycle. Continuous. Sub-perceptible.

**Rule:** Nothing animates faster than 300ms. No loading spinners.

---

## Product Design

### The Family Feed

The hero interaction. A vertically stacked timeline of subtle daily signals.

**Feed entry anatomy:**
- Left: timestamp in monospace, `rgba(255,255,255,0.50)`, with 6px violet dot indicator (`#7c3aed`, 70% opacity)
- Center: activity label, full white, `letter-spacing: 0.02em`
- Right: subtle signal bar — 40px × 2px, `rgba(255,255,255,0.12)` background, `rgba(124,58,237,0.5)` fill
- Hover: `translateY(-1px)` over 200ms, dot brightens to 100%
- Dividers: `1px solid rgba(255,255,255,0.06)`
- Recency: older entries fade toward top (opacity decreasing)

**Demo family — Margaret:**
- Name: Margaret
- Location: Saint Paul
- Relationship: Mother of Lisa
- Routine anchor: Coffee at 7:15 AM without exception
- Neighbor: Carol, drops by Tuesdays

Demo feed entries:
```
7:12 AM — Morning coffee made
9:30 AM — Walk completed
12:08 PM — Quiet lunch hour
4:41 PM — Lisa checked in
6:55 PM — Evening activity detected
```

### AI Pattern Summary Card

**Card states and voice:**

*Stable:*  
"Margaret's morning looked familiar. She was up by seven, coffee made before the light changed. Routine feels steady today."

*Gentle attention:*  
"There was a quieter stretch around midday — nothing concerning, but worth a gentle check-in later this week."

*Meaningful shift:*  
"This week's pattern feels a little different from last week. Worth paying attention to over the next few days."

**Voice rules (non-negotiable):**
- No percentages, scores, or risk language
- No "we detected" or "alert"
- No second person directed at Margaret — the card speaks to Lisa, not about Margaret as a data point
- Temporal, not instantaneous (days and weeks, not minutes)
- Specific over vague ("Lunch was quieter than usual" not "some activity change detected")

**Card footer (permanent):** *"Updated daily. Not an alert. A reflection."*

---

## Hero Image — Margaret

**Selected image:** Elderly woman, three-quarter profile, silver hair, warm knit sweater, holding steaming coffee cup near kitchen window. Morning light. Anonymous but present.

**Gradient overlay (full-width behind Feed section):**
```css
background: linear-gradient(to right, 
  rgba(11,13,18,0.0) 0%, 
  rgba(11,13,18,0.25) 45%, 
  rgba(11,13,18,0.85) 100%
);
filter: brightness(1.2);
```

**Midjourney prompt (saved for future regeneration):**
```
early morning kitchen window, elderly woman seen from behind in far left corner, 
silver hair, warm knit sweater, hands wrapped around a coffee cup, soft natural 
light falling across a worn wooden counter, steam rising gently from cup center 
frame, blurred interior background with soft bokeh, warm amber and dusty grey 
tones, quiet domestic stillness, photorealistic, shallow depth of field, muted 
warm palette, gentle overexposed window light, shot on 35mm film, cinematic grain, 
dark vignette edges fading to near black on right side --ar 16:9 --style raw --v 6.1
```

---

## Site Structure

| Page | Purpose | Status |
|------|---------|--------|
| Landing | Hero, Feed preview, philosophy, waitlist | 🔄 In development |
| Family Feed Demo | Full interactive Feed experience | 🔲 Planned |
| About | Mark's founder essay | 🔲 Content needed |

---

## What to Avoid

- Hospital / clinical visual language
- Blue/white color palettes
- Alert badges, warning indicators, red/amber status
- Enterprise dashboard grid layouts
- Stock healthcare photography
- Icon sets that feel corporate or SaaS
- Any animation faster than 300ms
- Loading spinners
- Dense UI

---

*Design decisions are documented here as they are made. Major changes require a brief rationale note.*

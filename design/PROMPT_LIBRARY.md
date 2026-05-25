# Prompt Library

**Maintained by:** Lindsay Shea, Media Director  
**Last updated:** May 2026

A living record of prompts that worked — for Lovable, Midjourney, and Claude. Good prompts are craft. We save them the way a designer saves reference images.

---

## Lovable Prompts

### Full Site Rebuild Brief
*Use when starting a new Lovable project from scratch or doing a major rebuild.*

```
ROUTINE STABILITY — Full Site Rebuild from Scratch

You are building a complete, production-quality website for a startup called 
Routine Stability. This is a rebuild. Start completely fresh.

WHAT THIS PRODUCT IS
Routine Stability is a calm, AI-native interface that helps adult children 
understand the daily routine patterns of aging parents — without surveillance, 
without alarms, without clinical dashboards.

The core product is called the Family Feed — a vertically stacked timeline 
of subtle daily signals interpreted by a quiet AI voice called the Pattern Summary.

This is not a healthcare platform. Not a monitoring system. Not an enterprise 
dashboard. It is an emotionally intelligent interface for pattern awareness over time.

[See full prompt in design/lovable-prompts/full-rebuild.md]
```

---

### Family Feed Section — Image Background
*Use to add or update the Margaret background image in the Feed section.*

```
IMPORTANT: Do not rebuild or redesign anything. Make one targeted change to 
the Family Feed section only. Preserve all existing design, typography, layout, 
colors, and content exactly as they are.

CHANGE — Family Feed Background Image

Add the uploaded photo as a background image to the full width of the Family 
Feed section — behind both the feed timeline entries on the left AND the 
Pattern Summary card on the right.

Image implementation:
- position: absolute
- top: 0, left: 0, width: 100%, height: 100%
- object-fit: cover
- object-position: center
- z-index: 0

Apply this full-width gradient overlay:
background: linear-gradient(to right, 
  rgba(11,13,18,0.0) 0%, 
  rgba(11,13,18,0.25) 45%, 
  rgba(11,13,18,0.85) 100%
);
filter: brightness(1.2);

Pattern Summary card: add backdrop-filter: blur(20px), 
background: rgba(11,13,18,0.45)

Do not change anything else.
```

---

### Surgical Fix Protocol
*Use when making targeted changes to avoid Lovable drifting into a rebuild.*

Always open surgical prompts with:
```
IMPORTANT: Do not rebuild or redesign anything. Make [N] targeted change(s) only. 
Preserve all existing design, typography, layout, colors, and content everywhere 
except where explicitly specified below.
```

Always close surgical prompts with:
```
DO NOT CHANGE:
[list everything that must stay the same]
```

---

## Midjourney Prompts

### Margaret — Primary Hero Image

**Best result prompt:**
```
early morning kitchen window, elderly woman seen from behind in far left corner, 
silver hair, warm knit sweater, hands wrapped around a coffee cup, soft natural 
light falling across a worn wooden counter, steam rising gently from cup center 
frame, blurred interior background with soft bokeh, warm amber and dusty grey 
tones, quiet domestic stillness, photorealistic, shallow depth of field, muted 
warm palette, gentle overexposed window light, shot on 35mm film, cinematic grain, 
dark vignette edges fading to near black on right side --ar 16:9 --style raw --v 6.1
```

**Midjourney workflow (to stay within credit budget):**
1. Run initial prompt → get 4-image grid
2. V# on the best result only (one variation)
3. U# to upscale the winner only
4. Export full resolution

**Image requirements for Feed section:**
- Aspect ratio: 16:9
- Dark natural fade on right edge (so overlay gradient has less work to do)
- No faces or identifiable features preferred (anonymous but present)
- Warm amber morning light — must feel like 7:12 AM

---

## Claude Prompts

### Session Opening
When starting a new strategy session with Claude, paste this at the start:

```
This is a working session for the Caring Sensor Community founder journal.
My name is Mark Shea. I am the founder. Lindsay Shea is our media director.

Current priorities: [state what you're working on this session]

Please reference the CSC foundation document context when relevant. 
At the end of our conversation, offer a 3–5 bullet summary I can log in 
the journal index, and flag any action items clearly.
```

### Design Review Request
```
Please review [describe what you're sharing] as if you are a senior 
creative director and startup strategist. Give me:
- An honest score (1–10 by dimension if relevant)
- What's strongest and why
- What's weakest and why  
- The single highest-leverage change
- One concrete prompt I can use to address it
```

### GitHub Document Update
```
I need to update [document name] in the CSC foundation repository.
Here is the current version: [paste document]
Here is what changed or needs to be added: [describe]
Please rewrite the relevant section(s) only, preserving everything else.
```

---

## Prompt Writing Principles

From Lindsay's experience building the Routine Stability site:

**Be surgical, not vague.** "Make it look better" produces drift. "Increase feed entry line height by 40%" produces results.

**Always name what NOT to change.** Lovable will get creative if you don't fence it in. Every prompt that worked ended with an explicit DO NOT CHANGE list.

**One job per credit.** Don't bundle unrelated changes. If two things are in the same section, they can share a prompt. If they're in different sections, split them.

**Save what works immediately.** Good prompts are craft. Document them here before you forget what made them work.

---

*Add new prompts here as they're developed. Note what worked, what didn't, and why.*


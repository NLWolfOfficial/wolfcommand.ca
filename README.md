# NL WOLF PROJECT — OPERATING SYSTEM
Last updated: 2026-04-30

This repository contains the NL Wolf ecosystem.  
All AI assistants (Claude, ChatGPT, etc.) working in this project MUST follow this README as the source of truth for structure, naming, and workflow.

---

## 1. CORE WORKING PRINCIPLE

No improvisation.

Only:
- Execute requested changes
- Follow defined structure
- Ask before assuming anything (especially filenames, paths, or design changes)

No redesigning, no optimization suggestions unless explicitly requested.

---

## 2. REPOSITORY STRUCTURE

| Site | Repo | Purpose |
|------|------|---------|
| nlwolf.com | NLWolfOfficial/nlwolf.com | Identity Hub |
| wolfstandard.ca | NLWolfOfficial/wolfstandard.ca | Reviews + scoring system |
| wolfpacklounge.com | NLWolfOfficial/wolfpacklounge.com | Community hub |
| wolfcommand.ca | NLWolfOfficial/wolfcommand.ca | Gear database |

**Hosting:** GitHub — NLWolfOfficial  
**Deployment:** Cloudflare Pages — auto-deploys on every commit. No manual deploy needed.

**GitHub upload URLs:**
- `github.com/NLWolfOfficial/nlwolf.com/upload/main`
- `github.com/NLWolfOfficial/wolfstandard.ca/upload/main`
- `github.com/NLWolfOfficial/wolfpacklounge.com/upload/main`
- `github.com/NLWolfOfficial/wolfcommand.ca/upload/main`

**Images folder:** same URL + `/images`

---

## 3. FILE NAMING RULES (STRICT)

### HTML
`brand-model-variant.html`  
Lowercase, hyphens only. No spaces. No underscores.

### Images
`brand-model-01.jpg`  
`brand-model-02.jpg`  
AVIF allowed if that is what was specified at time of upload.

### Image folder
All review images go in: `/images/`

### Badge files (wolfstandard.ca root — not in /images/)
- `/badge-alpha.jpg`
- `/badge-standard.jpg`
- `/badge-approved.jpg`
- `/Wolf_Failed_clean.png`

---

## 4. REVIEW PAGE WORKFLOW (MANDATORY)

Before creating or modifying any review page:

1. State the exact HTML filename
2. State the exact image filenames
3. Wait for explicit confirmation from Tim
4. Then generate the full file

**No exceptions.**

Template file: `wolfstandard-review-template-v2.html`

---

## 5. INDEX FILES (SOURCE OF TRUTH)

These files must never be rebuilt from scratch — only edited:

| File | Site |
|------|------|
| index_NLWolf.html | nlwolf.com |
| index_Wolf_Standard.html | wolfstandard.ca |
| index_Wolf_Pack_Lounge.html | wolfpacklounge.com |
| index_Wolf_Command.html | wolfcommand.ca |

**Rule:** After every new review → update `index_Wolf_Standard.html` and push it.

---

## 6. WOLF STANDARD SCORING SYSTEM

Each product scored across 5 pillars (1–10 each):

- Durability
- Function
- Simplicity
- Value
- Rebuy Test

**Final Score** = average of all 5 × 10 (score out of 100)

| Score | Badge |
|-------|-------|
| 85–100 | Alpha Tier → badge-alpha.jpg |
| 70–84 | Wolf Standard → badge-standard.jpg |
| 50–69 | Wolf Approved → badge-approved.jpg |
| 0–49 | Wolf Rejected → Wolf_Failed_clean.png |

**Hard rule:** Rebuy score below 5 = automatic Wolf Rejected. No override. No exceptions.

---

## 7. PUBLISHED REVIEWS — wolfstandard.ca

| File | Badge | Score | Category | Images |
|------|-------|-------|----------|--------|
| leatherman-skeletool-cx.html | Alpha Tier | 86/100 | Field Kit | leatherman-skeletool-cx-01.jpg, leatherman-skeletool-cx-02.jpg |
| defense-grid-1-2.html | Alpha Tier | 92/100 | Gaming & Strategy | defense-grid-1-2-01.jpg, defense-grid-1-2-02.avif |

---

## 8. BRAND IDENTITY (DO NOT CHANGE)

### Colors
- Black: `#000000`
- Gold: `#B8860B`
- Blue: `#4AB2EF`
- Red: `#8B0000`

### Fonts
- Headers: Bebas Neue
- Labels: Barlow Condensed
- Body: Barlow

### Accessibility
Minimum text color on dark backgrounds: `#999999`

### Nav (identical on all sites)
- NL in Blue (#4AB2EF) | WOLF in White
- Blue bottom border
- Links: Identity Hub | The Standard | The Den | The Command | Join The Pack

---

## 9. 10 CATEGORIES (same across all sites)

01 Base Camp | 02 Mobility | 03 Command Center | 04 Field Kit  
05 Survival & Prep | 06 Body Armor | 07 Wolf Standard Finance  
08 Outdoors & Field | 09 Gaming & Strategy | 10 Downloads & Archive

---

## 10. OUTPUT RULES

When generating code:
- Always output complete files — no fragments
- Do not add commentary unless requested
- Do not change structure unless explicitly instructed
- Do not assume missing assets or paths
- Do not rename files — use the names Tim provides

---

## 11. COMMUNICATION RULE

If anything is unclear:
- STOP
- Ask one specific question
- Do not proceed with assumptions

---

## 12. SYSTEM BEHAVIOR

This README is the authority layer.

If a request conflicts with it:
- Flag the conflict
- Do not silently override rules
- Wait for direction

---

## END OF SYSTEM

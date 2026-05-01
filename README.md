# NL WOLF PROJECT — OPERATING SYSTEM
Last updated: 2026-05-01

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
| nlwolf.com | nlwolf_v3 | Identity Hub |
| wolfstandard.ca | wolfstandard.ca | Reviews + scoring system |
| wolfpacklounge.com | wolfpacklounge_v2 | Community hub |
| wolfcommand.ca | wolfcommand_v4 | Gear database |

**Hosting:** GitHub — NLWolfOfficial  
**Deployment:** Cloudflare Pages — auto-deploys on every commit. No manual deploy needed.

**GitHub upload URLs:**
- Root: `github.com/NLWolfOfficial/[REPO]/upload/main`
- Images: `github.com/NLWolfOfficial/[REPO]/upload/main/images`

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

## 13. CODE & BUILD APPROVAL RULE (MANDATORY — 2026-05-01)

No AI assistant may generate, output, or modify ANY HTML file, code file, or script unless Tim has replied in that exact conversation turn with:

**APPROVED**

That exact word. Nothing else qualifies.

Rules:
- Asking confirmation questions does NOT equal approval to build
- Context and conversation flow does NOT equal approval to build
- If APPROVED has not been typed, STOP and WAIT
- No exceptions. No "he probably means go ahead." STOP and WAIT.

Violation of this rule damages live sites and wastes resources. It will not be tolerated.

### REQUIRED FLOW
Step 1: AI provides filenames, paths, and required assets only
Step 2: Tim reviews and replies with APPROVED
Step 3: AI generates full file
If Step 2 does not occur → AI must STOP

---

## 14. PRINT / PDF RULE (MANDATORY — 2026-05-01)

Every guide, checklist, and review page across all four sites MUST include a `@media print` CSS block.

Rules:
- White background on print — no black, no dark colours
- Black or dark grey text on print — readable without colour
- Nav, footer, breadcrumb hidden on print
- Sidebar hidden on print — main content only
- Checklist boxes remain as printable squares
- `page-break-inside: avoid` on all checklist items, steps, and warning blocks
- This block is required in: all wolfcommand guides, all wolfstandard reviews, all wolfpacklounge pages, any content page on any of the four sites

This rule applies to the wolfstandard-review-template.html as well — that file needs the print block added the next time it is touched.

---

## 15. READABILITY STANDARDS (LOCKED — 2026-05-01)

These are non-negotiable across every page on all four sites. No exceptions.

**Text colours — minimum values:**
- Body / description text: `#c0c0c0` minimum. Never below this.
- Hero / intro text: `#c0c0c0` minimum.
- Section description text: `#c0c0c0` minimum.
- Item description text: `#c0c0c0` minimum.
- Labels / tags / meta text: `#555555` minimum.

**Section numbers (01, 02, 03 etc):**
- Always full `#4AB2EF` — NO opacity reduction. Ever.

**Font sizes — minimums:**
- Body / description text: `0.95rem` minimum. Never smaller.
- Item titles: `1.1rem` minimum.
- Section description: `1rem` minimum.

**Spacing:**
- Section margin-bottom: `4.5rem` minimum.
- Checklist item padding: `1.4rem 1.5rem` minimum.
- Step list gap: `2rem` minimum.

**Every new file built from any template must meet these standards before it is considered complete.**

---

## END OF SYSTEM

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
| nlwolf.com | nlwolf.com | Identity Hub |
| wolfstandard.ca | wolfstandard.ca | Reviews + scoring system |
| wolfpacklounge.com | wolfpacklounge.com | Community hub |
| wolfcommand.ca | wolfcommand.ca | Gear database |

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

Template file: `wolfstandard-review-template.html`

---

## 5. INDEX FILES (SOURCE OF TRUTH)

These files must never be rebuilt from scratch — only edited:

| File | Site |
|------|------|
| index.html | nlwolf.com |
| index.html | wolfstandard.ca |
| index.html | wolfpacklounge.com |
| index.html | wolfcommand.ca |

**Rule:** After every new review → update `index.html` on wolfstandard.ca and push it.
After every new guide or archive item → update `index.html` on wolfcommand.ca and push it.

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
Minimum text color on dark backgrounds: `#c0c0c0`

### Nav (identical on all sites)
- NL in Blue (#4AB2EF) | WOLF in White
- Blue bottom border
- Links: Identity Hub | The Standard | The Den | The Command | Join The Pack

---

## 9. 10 CATEGORIES (same across all sites)

01 Home Build | 02 Mobility | 03 Command Center | 04 Field Kit  
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

Every content page (guides, checklists, reviews) MUST also include a **Print / Save as PDF button** that triggers `window.print()`. Button must be hidden on print using `@media print { .print-btn { display: none; } }`.

---

## 14B. LATEST FROM THE PACK STRIP (MANDATORY — 2026-05-01)

All 4 site index pages must contain a "Latest From The Pack" strip showing the 3 most recently published items across the entire ecosystem.

Rules:
- Strip sits immediately after the hero section on all 4 index pages — NOT at the bottom, NOT above the footer. After the hero. First thing visible after the intro.
- Shows exactly 3 items — most recent first
- Each item has: NEW gold tag (on the two most recent), site badge, title, short description, direct link
- Remove the NEW tag from the oldest of the 3 when a new item is added
- Update all 4 index pages every time new content is published anywhere in the ecosystem
- Current 3 items (update this list when new content is published):
  1. Wolf Command — Offline Sovereign Security (keepass-yubikey-setup-guide.html)
  2. Wolf Standard — Defense Grid 1 & 2 (defense-grid-1-2.html)
  3. Wolf Standard — Leatherman Skeletool CX (leatherman-skeletool-cx.html)

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

## 16. FILE DELIVERY RULE (MANDATORY — 2026-05-01)

Every file Claude delivers must include BOTH locations. No exceptions.

**Format — always state both:**

GitHub (live site): `github.com/NLWolfOfficial/[repo]/upload/main`
Local (W: drive): `W:\[folder]\`

---

**W:\ — Root structure:**
- `W:\KeePass\`
- `W:\NL Wolf\` → Blog, FB Wolf Pack NL
- `W:\Older Stuff\`
- `W:\Wolf Pack Lounge\` → Backups, Bot Configs, Discord Backups, Emojis, files, Master Guides, OLD WPL Guides, WolfStandard, WPL Pics, YT vids and voice
- `W:\Wolf Standard\` → Accountability Files, ATIPP and Research, Review and Scoring Template, wolfstandard.ca
- `W:\WolfCommand\` → see full structure below
- `W:\YT\`

---

**W:\WolfCommand\ — Full structure:**

```
W:\WolfCommand\
│
├── 01_Home_Build\
│   ├── 01_Kitchen_Essentials\
│   ├── 02_Bathroom_Essentials\
│   ├── 03_Bedroom_Setup\
│   ├── 04_Laundry_and_Cleaning\
│   ├── 05_Tools_and_Repair\
│   ├── 06_Smart_Home\
│   └── 07_Security_and_Access\
│
├── 02_Mobility\
│   ├── 01_Vehicle_Loadout\
│   ├── 02_Tires_and_Wheels\
│   ├── 03_Navigation_and_Comms\
│   ├── 04_Power_and_Charging\
│   └── 05_Bike_and_Alternate\
│
├── 03_Command_Center\
│   ├── 01_PC_Builds_and_Components\
│   ├── 02_Monitors_and_Displays\
│   ├── 03_Networking\
│   ├── 04_Storage_and_NAS\
│   ├── 05_Peripherals\
│   ├── 06_Audio_and_Studio\
│   ├── 07_Security_and_Privacy\
│   └── 08_Cables_and_Power\
│
├── 04_Field_Kit\
│   ├── 01_Medical_and_IFAK\
│   ├── 02_Navigation\
│   ├── 03_Communication\
│   ├── 04_Cutting_and_Tools\
│   └── 05_Specialty_Tools\
│
├── 05_Survival_and_Prep\
│   ├── 01_Bug_Out_Bags\
│   ├── 02_Food_and_Water_Storage\
│   ├── 03_Shelter_and_Warmth\
│   ├── 04_Power_and_Light\
│   └── 05_Security_and_Defense\
│
├── 06_Body_Armor\
│   ├── 01_Plate_Carriers\
│   ├── 02_Ballistic_Plates\
│   ├── 03_Helmets\
│   └── 04_Soft_Armor\
│
├── 07_Finance\
│   ├── 01_Cold_Storage_and_Crypto\
│   ├── 02_Cash_and_Precious_Metals\
│   ├── 03_Banking_and_Accounts\
│   ├── 04_Insurance\
│   └── 05_Investment\
│
├── 08_Outdoors_and_Field\
│   ├── 01_Camping_and_Backpacking\
│   ├── 02_Hunting_and_Fishing\
│   ├── 03_Rucking_and_Fitness\
│   ├── 04_Winter_Operations\
│   └── 05_Water_Operations\
│
├── 09_Gaming_and_Strategy\
│   ├── 01_PC_Gaming_Setup\
│   ├── 02_Console_Setup\
│   ├── 03_Mobile_and_Handheld\
│   ├── 04_Streaming_Setup\
│   └── 05_Gaming_Chair_and_Desk\
│
└── 10_Downloads_and_Archive\
    ├── 01_Mobile_Game_Guides\
    ├── 02_AI_Tools_and_Workflows\
    ├── 03_Security_and_Privacy\
    ├── 04_Essential_Software\
    └── 05_Wolf_Pack_Resources\
```

If the correct local folder path is uncertain → STOP and ask before delivering.

---

## END OF SYSTEM

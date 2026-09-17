# LifePROAssist.AI — Design Handoff

**Figma File:** `Design_file_agent` · fileKey `8ZaovNEs0AMxJDUsGuknzB`  
**Date:** 2026-09-17  
**Author:** Karthik G

---

## Table of Contents

1. [Design Tokens](#design-tokens)
2. [Typography](#typography)
3. [Frame 01 — Welcome Screen (Desktop)](#frame-01--welcome-screen-desktop)
4. [Frame 02 — Welcome + Artifact Action Menu](#frame-02--welcome--artifact-action-menu)
5. [Frame 03 — AI Thinking / Loading State](#frame-03--ai-thinking--loading-state)
6. [Frame 04 — AI Response (JIRA Ticket List)](#frame-04--ai-response-jira-ticket-list)
7. [Frame 05 — Product Navigation Sidebar](#frame-05--product-navigation-sidebar)
8. [Frame 01 Mobile — Mobile 390px](#frame-01-mobile--mobile-390px)
9. [Component Inventory](#component-inventory)
10. [Interaction Notes](#interaction-notes)

---

## Design Tokens

### Colors

| Token | Value | Usage |
|-------|-------|-------|
| `--color-primary` | `#005071` | Brand primary, CTA backgrounds, links |
| `--color-primary-light` | `#0099CC` | Gradient end, hover states |
| `--color-dark` | `#0d1f27` | Body text, headings |
| `--color-muted` | `#5e7f8f` | Secondary text, subtitles |
| `--color-bg` | `#f7f9fb` | Page background |
| `--color-white` | `#ffffff` | Card backgrounds, input fields |

### Opacity Variants

| Usage | Value |
|-------|-------|
| Dark text muted | `rgba(13, 31, 39, 0.8)` |
| Dark text subtle | `rgba(13, 31, 39, 0.5)` |
| Muted text light | `rgba(94, 127, 143, 0.7)` |
| Border default | `rgba(0, 80, 113, 0.12)` |
| Border hover | `rgba(0, 80, 113, 0.2)` |
| Overlay bg | `rgba(0, 80, 113, 0.05)` |

### Semantic Gradients

| Token | Value | Usage |
|-------|-------|-------|
| `--gradient-brand` | `155deg, #005071 → #0099CC` | Artifact pill, AI avatar |
| `--gradient-purple` | `135deg, #7c3aed → #a855f7` | Generate BRD, ProductConfig.AI |
| `--gradient-blue` | `135deg, #0284c7 → #38bdf8` | Generate BDD, PDDAssist.AI |
| `--gradient-amber` | `135deg, #b45309 → #f59e0b` | Generate Mods |
| `--gradient-green` | `135deg, #059669 → #34d399` | Generate Test Cases, SAA |
| `--gradient-rose` | `135deg, #be123c → #fb7185` | ProductConfig.AI Rate Agent |
| `--gradient-cyan` | `135deg, #0891b2 → #22d3ee` | Pixora.AI |

---

## Typography

**Font Family:** `Yantramanav` (Google Fonts)  
**Weights used:** Bold (700), Medium (500), Regular (400), Light (300)

| Style | Size | Weight | Letter Spacing | Usage |
|-------|------|--------|----------------|-------|
| Hero heading | 38.4px | Bold | -0.6px | Welcome title |
| Section label | 16px | Bold | — | Sidebar product name |
| Card title | 14px | Bold | — | Nav card titles, CTAs |
| Body | 14px | Regular | — | User messages, intro text |
| Body light | 14px | Light | — | AI response body, subtitles |
| Caption | 13px | Regular | — | Mobile card text |
| Label | 12px | Light | — | Nav card subtitles |
| Overline | 10.4px | Medium | 0.832px | Sidebar section label (uppercase) |
| Micro | 11px | Light | — | Loading sub-label, char count |
| Avatar text | 9px | Bold | — | "KG" avatar initials |

---

## Frame 01 — Welcome Screen (Desktop)

**Node:** `2:7` · **Canvas:** `1366 × 719 px`

### Header

| Property | Value |
|----------|-------|
| Background | `#ffffff` |
| Height | `52px` |
| Padding | `px-16 py-12` |
| Logo | Bold 18px `#005071` |
| Zoom control pill | Border `rgba(0,80,113,0.12)`, `8px` radius, `32px` height |
| Icon buttons | `32 × 32px`, `6px` padding, `rgba(13,31,39,0.7)` fill |
| User avatar | `28px` circle, `#005071` bg, "KG" `9px Bold` white, `14px` border-radius |
| Username label | `14px Regular #0d1f27` |

### Hero Section

| Property | Value |
|----------|-------|
| Title | "Welcome to LifePROAssist.AI" · `38.4px Bold #0d1f27` · tracking `-0.6px` |
| Subtitle | `14px Light #5e7f8f` · centered |
| Max-width | `768px` · centered |

### Prompt Card Grid

| Property | Value |
|----------|-------|
| Grid | 2 columns × 2 rows |
| Container | `768px` wide, `10px` gap |
| Card size | `379 × 50px` |
| Card bg | `#ffffff` |
| Card border | `1px solid rgba(0,80,113,0.12)` |
| Card radius | `8px` |
| Icon badge | `32 × 32px`, `8px` radius, gradient bg |
| Text | `14px Regular rgba(13,31,39,0.8)` |
| Chevron | `14px rgba(13,31,39,0.4)` |

### Chat Input

| Property | Value |
|----------|-------|
| Width | `768px` |
| Height | `97px` |
| Background | `#ffffff` |
| Border | `1px solid rgba(0,80,113,0.12)` |
| Border radius | `12px` |
| Padding | `px-16 pt-12 pb-8` |
| Placeholder | `14px Light rgba(13,31,39,0.4)` |

#### Chat Toolbar (left → right)

| Button | Icon | Label | Active State |
|--------|------|-------|-------------|
| Attach | `paperclip` | "Attach" | — |
| Browse Prompts | `folder` | "Browse Prompts" | — |
| Deep Thinking | `brain` | "Deep Thinking" | Toggle — bg `#e5eef2`, `#005071` dot indicator |
| Insights | `chart-column` | "Insights" | — |
| Clear | `trash-2` | "Clear" | — |

All toolbar items: `12px Regular rgba(13,31,39,0.6)`, icon `14px`, gap `6px`

### Artifact Pill (Floating)

| Property | Value |
|----------|-------|
| Size | `104.5 × 48px` |
| Background | `linear-gradient(155deg, #005071, #0099CC)` |
| Border radius | `24px` |
| Icon | Rocket `16px` white |
| Label | "Artifact" `13px Bold` white |
| Shadow (default) | `0px 4px 12px rgba(0,80,113,0.35)` |
| Position | `position: absolute; bottom: 80px; right: 24px` |

---

## Frame 02 — Welcome + Artifact Action Menu

**Node:** `2:169` · **Canvas:** `1366 × 719 px`

Extends Frame 01. The Artifact pill is in its **expanded** state with an action menu floating above it.

### Artifact Pill (Expanded State)

| Property | Value |
|----------|-------|
| Shadow | `0px 8px 24px rgba(0,80,113,0.5), 0px 2px 6px rgba(0,80,113,0.22)` |

### Action Menu

Stacked vertically above the Artifact pill, 4 items ordered top → bottom:

| Action | Gradient | Circle size |
|--------|----------|-------------|
| Generate BRD | `135deg, #7c3aed → #a855f7` | `44px` |
| Generate BDD | `135deg, #0284c7 → #38bdf8` | `44px` |
| Generate Mods | `135deg, #b45309 → #f59e0b` | `44px` |
| Generate Test Cases | `135deg, #059669 → #34d399` | `44px` |

Each menu item layout (right-to-left):
- **Circle button:** `44px` diameter, gradient bg, `22px` radius, white icon `16px`
- **Label pill:** white bg, `box-shadow: 0px 2px 8px rgba(0,0,0,0.12)`, `10px` radius, `px-12 py-6`, `13px Medium #0d1f27`
- Gap between pill and circle: `8px`

---

## Frame 03 — AI Thinking / Loading State

**Node:** `2:362` · **Canvas:** `1366 × 719 px`

### User Message Bubble

| Property | Value |
|----------|-------|
| Background | `#005071` |
| Text | "Generate BRD" · `14px Regular` white |
| Border radius | `12px 12px 4px 12px` (tl / tr / br / bl) |
| Padding | `px-12 py-8` |
| Max-width | `320px` |
| Alignment | Right-aligned with user avatar |

### User Avatar (inline)

| Property | Value |
|----------|-------|
| Size | `28px` circle |
| Background | `#005071` |
| Text | "KG" `9px Bold` white |
| Border radius | `14px` |

### AI Avatar

| Property | Value |
|----------|-------|
| Size | `28px` circle |
| Background | `linear-gradient(135deg, #005071, #0088b3)` |
| Icon | Spark `14px` white |

### AI Loading Card

| Property | Value |
|----------|-------|
| Size | `288 × 120.5px` |
| Background | `#ffffff` |
| Border | `1px solid rgba(0,80,113,0.12)` |
| Border radius | `16px 14px 12px 4px` (tl / tr / br / bl) |
| Padding | `px-16 py-12` |

#### Loading Card Contents

| Element | Spec |
|---------|------|
| AI logo | `30px` |
| "Thinking" label | `14px Medium #005071` |
| Animated dots | 3 × `6px` circles `rgba(0,80,113,0.7)`, pulsing animation |
| Sub-label | "Gathering relevant data sources…" · `11px Light rgba(94,127,143,0.7)` |
| Progress bar track | `4px` tall, `100%` wide, `rgba(94,127,143,0.1)` bg, `4px` radius |
| Progress bar fill | `#005071`, `~33%` width, animated left-to-right |
| Skeleton line 1 | `8px` tall, `100%` wide, `rgba(94,127,143,0.12)` bg, `4px` radius |
| Skeleton line 2 | `8px` tall, `70%` wide, `rgba(94,127,143,0.12)` bg, `4px` radius |
| Gap between skeleton lines | `6px` |

---

## Frame 04 — AI Response (JIRA Ticket List)

**Node:** `2:528` · **Canvas:** `1366 × 719 px`

### AI Response Bubble

| Property | Value |
|----------|-------|
| Width | `563px` |
| Background | `#ffffff` |
| Border | `1px solid rgba(0,80,113,0.12)` |
| Border radius | `12px 12px 4px 12px` (tl / tr / br / bl) |
| Padding | `px-16 py-12` |

### Response Content

| Element | Spec |
|---------|------|
| Intro sentence | `14px Regular #005071` |
| Body text | `14px Light rgba(13,31,39,0.8)` |
| Bullet list gap | `8px` between items |

#### JIRA Ticket List

| Ticket | Status | Summary |
|--------|--------|---------|
| LIFE-4821 | `[In Progress]` | Recalculate dividend accumulation for PAR policies |
| LIFE-4805 | `[In Review]` | Add paid-up additions (PUA) option |
| LIFE-4790 | `[Done]` | Fix reversionary bonus rounding |
| LIFE-4772 | `[Blocked]` | Cash dividend option not honoring election |
| LIFE-4758 | `[To Do]` | Expose PAR dividend scale as configurable rate table |

### AI Action Row

4 icon buttons aligned left below response content:

| Button | Icon | Size |
|--------|------|------|
| Thumbs up | `thumbs-up` | `14px` |
| Thumbs down | `thumbs-down` | `14px` |
| Copy | `copy` | `14px` |
| Download | `download` | `14px` |

Each button: `26 × 26px` container, `6px` padding, `rgba(13,31,39,0.4)` icon fill, `hover: rgba(0,80,113,0.08)` bg

---

## Frame 05 — Product Navigation Sidebar

**Node:** `2:686` · **Canvas:** `1366 × 719 px`

### Overlay

| Property | Value |
|----------|-------|
| Background | `rgba(13, 31, 39, 0.1)` |
| Backdrop blur | `blur(1px)` |
| Coverage | Full viewport behind sidebar |

### Sidebar Panel

| Property | Value |
|----------|-------|
| Size | `320 × 658px` |
| Background | `#ffffff` |
| Border-left | `1px solid rgba(0,80,113,0.12)` |
| Box shadow | `0px 25px 25px rgba(0,0,0,0.25)` |
| Position | Right edge of viewport |
| Padding | `px-16 py-20` |

### Sidebar Header

| Element | Spec |
|---------|------|
| Section label | "SWITCH PRODUCT" · `10.4px Medium uppercase letter-spacing: 0.832px rgba(13,31,39,0.5)` |
| Product name | "LifePRO Suite" · `16px Bold #005071` |
| Close button | `✕` icon `16px rgba(13,31,39,0.6)`, top-right |

### Navigation Cards

Container: `287px` wide, `16px` gap between cards

Each card:

| Property | Value |
|----------|-------|
| Width | `287px` |
| Border | `1px solid rgba(0,80,113,0.12)` |
| Border radius | `12px` |
| Padding | `px-16 py-14` |
| Layout | Row: icon badge · text block · arrow |

| # | Product | Gradient | Subtitle |
|---|---------|----------|---------|
| 1 | **ProductConfig.AI** | `#7c3aed → #a855f7` | "Intelligent product template configuration" |
| 2 | **PDDAssist.AI** | `#0284c7 → #38bdf8` | "Deep analytics and data exploration" |
| 3 | **Smart Agent Assist (SAA)** | `#059669 → #34d399` | "Guided workflows for service agents" |
| 4 | **ProductConfig.AI Rate Agent** | `#be123c → #fb7185` | "Automated rate table management & pricing" |
| 5 | **Pixora.AI** | `#0891b2 → #22d3ee` | "Low-code app orchestration and integration" |

Icon badge: `40 × 40px`, `12px` radius, gradient bg, `box-shadow: 0px 4px 8px rgba(0,0,0,0.15)`  
Title: `14px Bold #0d1f27`  
Subtitle: `12px Light #5e7f8f`  
Arrow: `14px rgba(13,31,39,0.4)`

### Sidebar Footer

| Property | Value |
|----------|-------|
| Button label | "View all solutions" |
| Background | `rgba(0, 80, 113, 0.05)` |
| Border | `1px solid rgba(0,80,113,0.2)` |
| Border radius | `12px` |
| Text | `14px Medium #005071` |
| Width | `287px` |
| Height | `44px` |

---

## Frame 01 Mobile — Mobile 390px

**Node:** `28:4` · **Canvas:** `390 × 844 px`

### Mobile Header

| Property | Value |
|----------|-------|
| Height | `52px` |
| Padding | `px-16 py-12` |
| Background | `#ffffff` |
| Logo | `18px Bold #005071` |
| Avatar | `28px` circle `#005071` bg, "KG" `9px Bold` white, `14px` radius |

### Welcome Section

| Property | Value |
|----------|-------|
| Heading | `28px Bold #0d1f27` tracking `-0.6px`, centered, full-width |
| Subtitle | `14px Light rgba(13,31,39,0.5) + #5e7f8f`, centered |
| Vertical gap | `8px` below heading |

### Suggestion Cards

4 stacked full-width cards:

| Property | Value |
|----------|-------|
| Width | `100%` (minus `px-16` page padding) |
| Padding | `12px` |
| Border | `1px solid rgba(0,80,113,0.12)` |
| Border radius | `10px` |
| Gap between cards | `8px` |
| Icon badge | `32 × 32px`, `8px` radius, gradient bg |
| Text | `13px Regular rgba(13,31,39,0.8)` |
| Chevron | `14px rgba(13,31,39,0.4)` |

### Chat Input Area

| Property | Value |
|----------|-------|
| Padding | `px-16 pt-12 pb-8` |
| Input bg | `#ffffff` |
| Input border | `1px solid rgba(0,80,113,0.12)` |
| Input radius | `10px` |
| Placeholder | `14px Light rgba(13,31,39,0.4)` |
| Send button | `32 × 32px` circle `#005071` at `30%` opacity, arrow-up icon white |

### Mobile Toolbar (icon-only, no labels)

| Icon | Active State |
|------|-------------|
| `paperclip` | — |
| `folder` | — |
| `brain` | `bg: #e5eef2`, `#005071` dot below icon |
| `chart-column` | — |
| `trash-2` | — |

Character count: `11px Light rgba(13,31,39,0.4)` · right-aligned

### Artifact Pill (Mobile)

| Property | Value |
|----------|-------|
| Size | `104 × 48px` |
| Background | `linear-gradient(155deg, #005071, #0099CC)` |
| Border radius | `24px` |
| Icon | Rocket `16px` white |
| Label | "Artifact" `13px Bold` white |
| Position | `position: absolute; bottom: 34px; right: 16px` |

---

## Component Inventory

| Component | Frames | Notes |
|-----------|--------|-------|
| App Header | All desktop | White bg, logo, zoom, icons, avatar |
| Prompt Card | 01, 02 | `379×50px` desktop / full-width mobile |
| Chat Input | All | Different toolbar label visibility |
| Artifact Pill | All | Same gradient, different shadow on expanded |
| Artifact Action Menu | 02 | Overlay, 4 gradient circles |
| User Message Bubble | 03, 04 | `#005071` bg, `12/12/4/12` radius |
| AI Loading Card | 03 | Animated dots + progress bar + skeleton |
| AI Response Bubble | 04 | White bg, action row below |
| Product Nav Sidebar | 05 | Overlay + panel, 5 nav cards |
| User Avatar | All | `28px`, `#005071`, "KG", `14px` radius |
| AI Avatar | 03, 04 | `28px`, brand gradient, spark icon |
| Nav Card | 05 | `287px`, icon badge + title + subtitle + arrow |

---

## Interaction Notes

### Artifact Pill
- **Default:** `box-shadow: 0px 4px 12px rgba(0,80,113,0.35)`
- **Expanded/hover:** `box-shadow: 0px 8px 24px rgba(0,80,113,0.5), 0px 2px 6px rgba(0,80,113,0.22)` + action menu appears above

### Deep Thinking Toggle
- **Off:** Plain icon, no background
- **On:** `background: #e5eef2`, dot indicator `#005071` below icon

### Loading Animation (Frame 03)
- 3 dots pulse sequentially with staggered delay
- Progress bar animates left-to-right, loops at 100%
- Skeleton lines shimmer (opacity 0.12 → 0.2 → 0.12)

### Sidebar
- Trigger: click product name / logo area in header
- Entry animation: slide-in from right
- Overlay: fade-in `rgba(13,31,39,0.1)` + `blur(1px)`
- Close: ✕ button or click outside overlay

### Card Hover States
- Prompt cards, Nav cards: `border-color: rgba(0,80,113,0.2)`, subtle `box-shadow: 0px 2px 8px rgba(0,80,113,0.08)`

---

*Figma File:* `https://www.figma.com/design/8ZaovNEs0AMxJDUsGuknzB/Design_file_agent`

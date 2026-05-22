# AquaGuard — Business Model Canvas HTML Page
## Prompt for Claude Code

---

## TASK

Generate a single, self-contained `AquaGuard_BMC.html` file — a professional,
print-ready Business Model Canvas document for the AquaGuard project.

The output must be ONE `.html` file with all CSS and JS embedded inline.
No external dependencies except Google Fonts.

---

## PROJECT CONTEXT

AquaGuard is a mobile-based emergency rescue support system for flood disasters,
built by a student team at Ho Chi Minh City University of Technology (HCMUT).

**Core purpose**: Connect flood-affected residents with rescue teams via:
- One-tap SOS with auto GPS
- Real-time rescue tracking (2s updates, <200ms latency)
- Multi-role coordination: citizen + rescuer + admin in one platform
- Offline resilience when network infrastructure fails

**NOT a weather alert app** — flood alerts are secondary.
The primary value is two-way emergency rescue coordination.

**Current status**: MVP complete. iOS app + React Web dashboard + Node.js backend.
OISP 2025 First Prize + EPICS 2026 First Prize + $500 USD grant received.
548+ survey respondents across 22 provinces. ~100 registered test users.

---

## DESIGN DIRECTION

### Aesthetic
- **Theme**: Professional, clean, modern — suitable for investor pitch AND academic submission
- **Tone**: Refined minimal with strong typographic hierarchy
- **Color palette**:
  - Primary navy: `#1B2A4A`
  - Accent teal: `#1D9E75`
  - Accent blue: `#378ADD`
  - Accent purple: `#7F77DD`
  - Accent amber: `#EF9F27`
  - Accent coral: `#D85A30`
  - Light background: `#F8F9FB`
  - Card background: `#FFFFFF`
  - Border: `#E2E6ED`
  - Text primary: `#1B2A4A`
  - Text secondary: `#64748B`

### Typography
- **Display / headings**: `DM Sans` (Google Fonts) — clean, modern, geometric
- **Body**: `Inter` (Google Fonts) — readable, professional
- Import: `https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600&family=Inter:wght@400;500&display=swap`

### Layout
- Max width: 1100px, centered
- Section breaks with clear visual separation
- Phase tabs with smooth transition
- Print-friendly: `@media print` hides navigation, expands all phases

### NEW badge style
- Background: `#E1F5EE`, color: `#085041`, font-size: 9px, padding: 2px 5px, border-radius: 3px
- For Phase 3 NEW badges: background `#EEEDFE`, color `#3C3489`

---

## PAGE STRUCTURE

The HTML page has these sections in order:

```
1. Header
2. Phase Navigation Tabs (Phase 1 / Phase 2 / Phase 3)
3. BMC Grid (9 blocks) — changes per tab
4. Roadmap Section (always visible below tabs)
5. Delta Comparison Table (always visible)
6. Footer
```

---

## SECTION 1 — HEADER

```
Logo: "AG" in a circle (navy background, white text)
Title: AquaGuard
Subtitle: Business Model Canvas
Tagline: A Mobile-Based Emergency Rescue Support System
Right side: HCMUT · March 2026
```

---

## SECTION 2 — PHASE NAVIGATION

Three tab buttons:
- Phase 1 — MVP & Research
- Phase 2 — Full Deployment
- Phase 3 — AI + Drone

Active tab: underline accent, navy text.
Inactive: gray text.
Switching tabs re-renders the BMC grid below with smooth fade transition.

---

## SECTION 3 — BMC GRID (9 BLOCKS)

Standard BMC layout. Use CSS Grid:
- Row 1: Key Partners (2 cols) | Key Activities (2 cols) | Value Propositions (2 cols, spans 2 rows) | Customer Relationships (2 cols) | Customer Segments (2 cols, spans 2 rows)
- Row 2: Key Partners continues | Key Resources (2 cols) | [VP continues] | Channels (2 cols) | [CS continues]
- Row 3 (footer): Cost Structure (5 cols) | Revenue Streams (5 cols)

Each block has:
- Top accent border (3px, color per block — see colors below)
- Block label (uppercase, 9px, letter-spacing)
- Bullet list of items (11px, line-height 1.5)
- [NEW] badge inline on applicable items

Block accent colors:
- Key Partners: `#378ADD` (blue)
- Key Activities: `#1D9E75` (teal)
- Value Propositions: `#7F77DD` (purple) — slightly different background
- Key Resources: `#EF9F27` (amber)
- Customer Relationships: `#D4537E` (pink)
- Channels: `#639922` (green)
- Customer Segments: `#D85A30` (coral)
- Cost Structure: `#E24B4A` (red)
- Revenue Streams: `#639922` (green)

---

## BMC CONTENT — PHASE 1: MVP & Research

**Phase label**: Phase 1 · MVP & Research
**Subtitle**: Academic project at HCMUT — core rescue features validated with real users

### Key Partners
- HCMUT — academic supervisors, labs, research support
- Google Maps API — geolocation and map infrastructure
- Firebase / Cloud providers — backend and database services
- Vietnam Meteorological & Hydrological Service (NCHMF) — weather data
- Thiền viện Vạn Hạnh — frontline rescue charity endorsement
- Quỹ Đất Lành (Canada) — international humanitarian backing
- OSM Vietnam — open-source mapping and routing data
- EPICS in IEEE / OISP — award credentials and institutional trust

### Key Activities
- iOS SwiftUI app development — SOS, GPS tracking, flood map
- Node.js backend + PostgreSQL 16 + Firebase + WebSocket infrastructure
- SOS lifecycle system: pending → assigned → in_progress → resolved
- Real-time GPS tracking at 2s intervals, <200ms latency
- React Web dashboard for rescue team admins
- Field testing across 22 provinces — structured feedback loops
- 548+ user survey research and analysis
- Grant writing — UNDP, OCHA, EU DG ECHO, AusAid applications

### Value Propositions
- One-tap SOS — auto GPS capture, no manual location description needed
- Live rescue tracking — victim and rescuer see each other's real-time position
- Pre/in/post-flood lifecycle: preparedness → rescue → family reunification → audit
- Multi-role coordination — citizen + rescuer + admin in one platform
- Structured audit trail — every SOS logged with timestamps and JSONB snapshots
- Offline resilience — auto-reconnect with 3s backoff, HTTP polling fallback
- Community-validated — 548+ survey respondents, 91 field users, 22 provinces
- Open-source core — adaptable to any flood-prone region globally

### Key Resources
- iOS SwiftUI app + React 19 Web dashboard + Node.js + PostgreSQL + Firebase
- OSRM routing + Leaflet flood visualization + Firestore flood zones
- 548+ user survey dataset across 22 provinces — unique competitive insight
- Multidisciplinary 5-student team (AI & IT, UTS/HCMUT)
- OISP 2025 First Prize + EPICS 2026 First Prize + $500 USD grant
- Endorsement letters: Thiền viện Vạn Hạnh + Quỹ Đất Lành
- 1,400+ community followers, 18,000+ content views

### Customer Segments
- Residents in flood-prone areas (Mekong Delta, Central Highlands, Coast)
- Local rescue teams — commune and district level (test users)
- Local government pilot partners
- Academic reviewers and competition judges

### Customer Relationships
- Community self-service — app download + push notifications
- In-app feedback and field testing loops
- Academic visibility — OISP + EPICS publications and lab presentations
- Social media engagement — 1,400+ followers on Facebook + Zalo

### Channels
- iOS App Store + TestFlight — direct beta download
- React Web PWA — browser access, no install required
- University demo events and academic conferences (OISP, EPICS)
- Social media — Facebook page + Zalo community
- QR codes on village notice boards — offline to online bridge

### Cost Structure
- Cloud infrastructure — $200–800/month, auto-scales during off-season
- Team: $0 (volunteer phase) — stipends planned as grants grow
- Mobile development — iOS ongoing updates ~$2,000–5,000/quarter
- Community outreach — workshops + printed materials $300–1,000/quarter
- Security audits — annual data protection compliance $1,000–3,000/year
- Legal & admin — company registration, IP protection ~$500–1,000/year

### Revenue Streams
- Academic research grants — HCMUT and partner universities
- EPICS in IEEE prize money — $500 received (proof of concept)
- NGO and innovation program grants
- Competition prize money — academic + humanitarian competitions $500–10,000/entry

---

## BMC CONTENT — PHASE 2: Full Deployment

**Phase label**: Phase 2 · Full Deployment
**Subtitle**: App complete on iOS + Android + Web PWA. Active rescue coordination in real flood events.

### Key Partners
- All Phase 1 partners — retained and scaled
- Red Cross Vietnam — volunteer rescue network [NEW]
- Provincial People's Committees — government procurement [NEW]
- Viettel / VNPT — SMS/USSD fallback for offline flood zones [NEW]
- UNDP / OCHA / EU DG ECHO / AusAid — humanitarian grant bodies [NEW]
- Vietnam Women's Union — grassroots distribution network [NEW]

### Key Activities
- All Phase 1 activities — retained
- Android app launch — full feature parity with iOS [NEW]
- Web PWA full rollout for rescue teams [NEW]
- White-label provincial deployment system [NEW]
- Multi-province rescue coordination at national scale [NEW]
- Government tender preparation and procurement [NEW]
- Post-disaster audit trail analysis and structured reporting [NEW]
- B2B flood alert API — data sold to telcos and weather apps [NEW]

### Value Propositions
- One-tap SOS — auto GPS, no manual location needed
- Live rescue tracking — victim + rescuer see each other real-time
- Full pre/in/post-flood lifecycle coordination
- Multi-role platform — citizen + rescuer + admin unified
- Structured audit trail — every SOS timestamped, JSONB logged
- Offline resilience — auto-reconnect, HTTP polling fallback
- White-label deployment for provincial governments [NEW]
- Community-validated — 548+ respondents, 22 provinces (proven) [NEW]
- B2B alert API for telcos and weather platforms [NEW]

### Key Resources
- All Phase 1 resources — retained
- Android app codebase [NEW]
- Scaled cloud infrastructure (AWS / Google Cloud) [NEW]
- First full-time engineering and operations team [NEW]
- Government data integration pipelines [NEW]
- Established user base and brand trust (1,400+ community) [NEW]
- Endorsement letters from credible institutions on file [NEW]

### Customer Segments
- Residents in flood-prone areas — Mekong Delta, Central Vietnam, Coast
- Local rescue teams and volunteer groups
- Farmers and rural workers — agricultural flood risk
- Provincial People's Committees — coordination dashboard [NEW]
- National agencies — MONRE, MARD, CCFC [NEW]
- NGOs — Red Cross VN, CARE, Oxfam [NEW]

### Customer Relationships
- Community self-service — app + push notifications
- Per-province government relationship manager [NEW]
- NGO technical working group + dedicated API documentation [NEW]
- Post-disaster follow-up and satisfaction surveys [NEW]
- Community ambassador program — village-level adoption drives [NEW]

### Channels
- iOS App Store + Android Play Store + TestFlight
- Web PWA — no install friction for rescue coordinators
- Government procurement — provincial white-label agreements [NEW]
- QR codes on village notice boards
- Red Cross Vietnam + Women's Union distribution networks [NEW]
- Academic conferences — OISP, EPICS, IFRC/OCHA forums [NEW]

### Cost Structure
- Cloud infrastructure — $200–800/month scaled to users
- Android app development — ~$2,000–5,000/quarter [NEW]
- Government engagement — travel + training $500–2,000/quarter [NEW]
- Community outreach — workshops + materials $300–1,000/quarter
- Full-time team salaries — from stipends to full pay [NEW]
- Security audits + compliance — $1,000–3,000/year
- Disaster ops on-call — 24/7 during peak season $500–2,000/event [NEW]
- Legal + company registration + banking ~$500–1,000/year [NEW]

### Revenue Streams
- Government white-label licensing — $50,000–200,000/province/year [PRIMARY] [NEW]
- NGO SaaS platform subscriptions — $5,000–20,000/org/year [NEW]
- Humanitarian grants — UNDP, OCHA, EU DG ECHO, AusAid [NEW]
- B2B alert API — flood data sold to telcos and weather apps [NEW]
- Freemium consumer — offline maps, priority alerts $2–5/month [NEW]
- Competition prize money — $500–10,000/entry

---

## BMC CONTENT — PHASE 3: AI + Drone

**Phase label**: Phase 3 · AI + Drone Integration
**Subtitle**: Drone mesh WiFi for connectivity-loss zones. AI rescue dispatch and flood prediction. Southeast Asia expansion.

### Key Partners
- All Phase 2 partners — retained and scaled
- Drone manufacturers and UAV research laboratories [NEW]
- Starlink / satellite providers — aerial mesh network backbone [NEW]
- Vietnam Civil Aviation Authority — UAV flight clearance [NEW]
- UN OCHA and ASEAN disaster management bodies [NEW]
- AI and ML research labs — model development partners [NEW]
- Insurance companies — anonymized flood data B2B licensing [NEW]
- Regional governments — Philippines, Indonesia, Thailand [NEW]

### Key Activities
- All Phase 2 activities — retained
- Drone mesh WiFi deployment — aerial connectivity for disaster zones [NEW]
- Drone supervision of active rescue operations [NEW]
- FANET (Flying Ad-hoc Network) management and edge computing [NEW]
- Starlink satellite integration for drone mesh backbone [NEW]
- AI rescue dispatch — ML routing optimization for rescue teams [NEW]
- AI flood prediction — historical SOS data hotspot mapping and risk scoring [NEW]
- Insurance data anonymization and B2B API licensing [NEW]
- Multi-country app localization — PH, ID, TH [NEW]

### Value Propositions
- One-tap SOS — auto GPS, no manual location needed
- Live rescue tracking — victim + rescuer real-time
- Full pre/in/post-flood lifecycle coordination
- Drone mesh WiFi — restores connectivity when infrastructure fails [NEW]
- Drone rescue supervision — aerial situational awareness for commanders [NEW]
- AI dispatch — optimal rescue team routing and resource allocation [NEW]
- AI flood prediction — pre-position resources before disaster peaks [NEW]
- Scalable globally — open-source core, adaptable to any flood region [NEW]
- Insurance risk modeling API — anonymized flood extent data [NEW]

### Key Resources
- All Phase 2 resources — retained
- Drone fleet and UAV communication hardware [NEW]
- Satellite communication modules — Starlink integration [NEW]
- AI/ML models — dispatch optimization, flood prediction, risk scoring [NEW]
- Anonymized historical SOS dataset — unique proprietary asset [NEW]
- Regional engineering and operations teams [NEW]
- Multi-country data platform and analytics infrastructure [NEW]

### Customer Segments
- All Phase 2 segments — retained and scaled
- Residents in connectivity-loss disaster zones (no infrastructure) [NEW]
- National emergency management agencies across SEA [NEW]
- Insurance companies — property and life risk modeling [NEW]
- UN and ASEAN disaster management bodies [NEW]
- International NGOs — Oxfam, CARE, IFRC global operations [NEW]

### Customer Relationships
- All Phase 2 relationships — retained
- AI-personalized flood risk alerts and recommendations [NEW]
- Drone operations support team for government deployments [NEW]
- B2G account management for regional government clients [NEW]
- Insurance B2B data partnership management [NEW]

### Channels
- All Phase 2 channels — retained
- B2G direct sales to national government agencies [NEW]
- UN and ASEAN partner distribution networks [NEW]
- IFRC and OCHA humanitarian forums and conferences [NEW]
- Insurance industry conferences and data marketplaces [NEW]

### Cost Structure
- All Phase 2 costs — retained and scaled
- Drone hardware procurement and maintenance [NEW]
- Satellite connectivity fees — Starlink subscription [NEW]
- AI/ML infrastructure — training compute and inference serving [NEW]
- UAV flight operations and regulatory compliance [NEW]
- Regional operations, localization, and support teams [NEW]
- FANET R&D — edge computing and aerial network protocols [NEW]

### Revenue Streams
- All Phase 2 streams — retained
- SaaS licensing to SEA regional governments [NEW]
- Insurance data licensing — anonymized flood extent B2B API [NEW]
- Drone-as-a-Service — per deployment or annual readiness retainer [NEW]
- AI analytics premium tier — prediction and risk scoring for authorities [NEW]
- UN and ASEAN climate resilience program funding [NEW]
- Open-source community support contracts [NEW]

---

## SECTION 4 — ROADMAP

Always visible below the BMC tabs. Title: "Product & Business Roadmap"

Layout: vertical timeline with 3 phases side by side as columns,
OR a vertical stepped layout with phase left + milestones right.

**Use a 2-column grid per phase: Product milestones | Business milestones**

### Phase 1 — Foundation (MVP & Research)

**Product milestones**:
- iOS app (SwiftUI) — SOS, GPS tracking, flood map live
- React Web dashboard for rescue admins
- Node.js + PostgreSQL 16 + Firebase + WebSocket backend
- 4-level flood zone severity classification system
- Offline resilience — auto-reconnect + HTTP polling fallback
- OSRM routing + Leaflet map visualization

**Business milestones**:
- 548+ survey respondents across 22 provinces
- 91 field users, ~100 registered testers active
- OISP 2025 First Prize won
- EPICS 2026 First Prize + $500 USD grant received
- Endorsements: Thiền viện Vạn Hạnh + Quỹ Đất Lành secured
- 1,400+ followers, 18,000+ content views

### Phase 2 — Deployment (Full Product · Real Rescue)

**Product milestones**:
- Android app launch — full feature parity with iOS
- Web PWA rollout — browser access, no install needed
- White-label system for provincial government deployment
- Multi-province national-scale rescue coordination
- Post-disaster audit trail and analytics reporting module
- B2B flood alert API — data sold to telcos and weather apps

**Business milestones**:
- Company legally registered — IP protection, banking
- First provincial government contract signed ($50K–200K/year)
- UNDP / OCHA / EU DG ECHO grant applications active
- NGO SaaS subscriptions — Red Cross VN, CARE, Oxfam
- First full-time salaried team members
- IFRC and OCHA humanitarian forum participation

### Phase 3 — AI + Drone (Intelligent Infrastructure · SEA Expansion)

**Product milestones**:
- Drone mesh WiFi — aerial network for connectivity-loss disaster zones
- Drone rescue supervision — real-time aerial situational awareness
- Starlink satellite integration — FANET backbone established
- AI rescue dispatch — ML routing for optimal team deployment
- AI flood prediction — historical SOS data hotspot mapping
- Multi-country localization — Philippines, Indonesia, Thailand

**Business milestones**:
- SaaS licensing to SEA regional governments
- Insurance data B2B API — anonymized flood extent licensing live
- Drone-as-a-Service model launched
- UN and ASEAN climate resilience program funding secured
- Open-source core released for global humanitarian adoption
- AI premium analytics tier launched for authorities

---

## SECTION 5 — DELTA COMPARISON TABLE

Title: "Evolution Delta — What Changes Across Phases"

6 rows × 4 columns: Block | Phase 1 | Phase 2 | Phase 3

| Block | Phase 1 · MVP | Phase 2 · Deployment | Phase 3 · AI + Drone |
|---|---|---|---|
| Key Partners | HCMUT, Google APIs, Vạn Hạnh, Quỹ Đất Lành, NCHMF, OSM VN | + Red Cross VN, Provincial Gov, Viettel/VNPT, UNDP/OCHA/EU DG ECHO | + Drone manufacturers, Starlink, Aviation Authority, ASEAN bodies, Insurance cos, SEA govs |
| Key Activities | iOS dev, backend build, SOS system, field research, grant writing | + Android launch, Web PWA, white-label system, gov procurement, B2B API | + Drone mesh WiFi, AI dispatch, AI flood prediction, FANET, multi-country localization |
| Value Propositions | SOS + GPS, live tracking, multi-role platform, offline resilience, audit trail | + White-label for provinces, B2B alert API, proven community validation | + Drone connectivity layer, aerial supervision, AI dispatch, AI prediction, insurance API |
| Customer Segments | Pilot users, rescue test teams, academic reviewers | + Provincial gov, national agencies (MONRE/MARD/CCFC), NGOs, farmers | + Connectivity-loss residents, SEA national agencies, insurers, UN/ASEAN, global NGOs |
| Revenue Streams | Research grants, prize money ($500 received) | + Gov white-label $50K–200K/province, NGO SaaS $5K–20K/org, B2B API, freemium | + SEA SaaS licensing, insurance data API, Drone-as-a-Service, AI premium tier |
| Key Resources | iOS app, student team, survey data (548+), prize credentials, endorsements | + Android app, scaled cloud, full-time team, gov pipelines, brand trust | + Drone fleet, Starlink modules, AI/ML models, proprietary SOS dataset, regional teams |

Style this as a clean HTML table with:
- Header row: navy background, white text
- Alternating row colors: white / light gray (#F8F9FB)
- Phase 2 cells: light teal left border (#1D9E75)
- Phase 3 cells: light purple left border (#7F77DD)
- Font size: 12px body, 11px uppercase headers

---

## SECTION 6 — FOOTER

```
AquaGuard · HCMUT · March 2026
Built by: Nguyen Minh Quan and team
Supervisors: Dr. Võ Thanh Hằng · MSc. Bùi Xuân Giang
Awards: OISP 2025 First Prize · EPICS 2026 First Prize
```

---

## TECHNICAL REQUIREMENTS

### File output
- Single file: `AquaGuard_BMC.html`
- All CSS inline in `<style>` tag
- All JS inline in `<script>` tag
- Only external dependency: Google Fonts

### Interactivity
- Phase tabs: click to switch BMC content with smooth fade (opacity transition 0.2s)
- All 3 BMC phases fully rendered in HTML, toggled via JS (display none/block)
- Roadmap and Delta table always visible

### Print support
```css
@media print {
  .tab-nav { display: none; }
  .bmc-phase { display: block !important; page-break-after: always; }
  .roadmap-section { page-break-before: always; }
  .delta-section { page-break-before: always; }
}
```

### Responsive
- Desktop: full grid layout (10 columns BMC)
- Mobile (< 768px): single column stacked layout
- Tablet: 2-column simplified grid

### BMC grid implementation
Use CSS Grid for the 9-block layout:
```css
.bmc-grid {
  display: grid;
  grid-template-columns: repeat(10, 1fr);
  grid-template-rows: auto auto auto;
  gap: 6px;
}
.block-partners   { grid-column: 1 / 3; grid-row: 1 / 3; }
.block-activities { grid-column: 3 / 5; grid-row: 1 / 2; }
.block-vp         { grid-column: 5 / 7; grid-row: 1 / 3; }
.block-relations  { grid-column: 7 / 9; grid-row: 1 / 2; }
.block-segments   { grid-column: 9 / 11; grid-row: 1 / 3; }
.block-resources  { grid-column: 3 / 5; grid-row: 2 / 3; }
.block-channels   { grid-column: 7 / 9; grid-row: 2 / 3; }
.block-costs      { grid-column: 1 / 6; grid-row: 3 / 4; }
.block-revenue    { grid-column: 6 / 11; grid-row: 3 / 4; }
```

---

## PROMPT TO PASTE INTO CLAUDE CODE TERMINAL

```
Read this file completely before writing any code.

Generate a single file called AquaGuard_BMC.html based on
all specifications in this document.

Requirements:
1. Single self-contained HTML file — all CSS and JS inline
2. Only external dependency: Google Fonts (DM Sans + Inter)
3. Three BMC phases switchable via tab navigation
4. Full BMC 9-block grid for each phase using CSS Grid
5. Roadmap section with 2-column product/business milestones
6. Delta comparison table across all 3 phases
7. Print-ready with @media print support
8. Responsive for mobile, tablet, desktop
9. All content from this document must appear exactly as written
10. [NEW] badges styled as specified
11. Navy + teal color scheme as specified
12. Professional, pitch-ready visual quality

Do not simplify or omit any content.
Output only the HTML file. No explanation needed.
```

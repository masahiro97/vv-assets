# VaccineVets Website Design Spec
> Framer UI rebuild guide. Inspired by Bond Vet, Small Door Vet, Hims.

---

## Design System (already set in Framer)

### Colors
| Style Path | Hex | Usage |
|---|---|---|
| `/Brand/Ink Black` | #131B23 | Text, logo |
| `/Bright Ocean` | #3490E0 | CTA buttons, accent |
| `/Bright Ocean Hover` | #1E6EBE | Button hover |
| `/Brand/Bright Ocean Light` | rgba(52,144,224,0.1) | Badge bg, light accent |
| `/Brand/Green` | #00A676 | Secondary accent, pricing highlight |
| `/Brand/Green Hover` | #00855E | Green hover |
| `/Porcelain` | #F9F7F3 | Page background, card bg |
| `/Brand/Vanilla Custard` | #EDDEA4 | Warm accent sections |
| `/Brand/Ink Black` | #131B23 | Dark text |

### Typography
| Style | Font | Size | Usage |
|---|---|---|---|
| `/Hero Title` | DM Serif Display | 64px | Hero headline |
| `/Hero Subtitle` | Inter 400 | 20px | Hero subheadline |
| `/Section Title` | DM Serif Display | 44px | Section headlines |
| `/Section Label` | Inter 600 | 13px uppercase | Category labels (blue) |
| `/Section Desc` | Inter 400 | 18px | Section descriptions |
| `/Card Title` | Inter 600 | 20px | Card headings |
| `/Card Desc` | Inter 400 | 15px | Card body text |
| `/Price` | DM Serif Display | 48px | Pricing numbers |
| `/Body` | Inter 400 | 16px | General body text |
| `/Nav Link` | Inter 500 | 15px | Navigation links |
| `/Nav Button` | Inter 600 | 15px white | CTA button text |

### Design Tokens
- **Border Radius**: Cards 16px, Buttons 100px (pill), Images 12px
- **Card Shadow**: `0 4px 16px rgba(0,0,0,0.06)`
- **Card Hover Shadow**: `0 8px 24px rgba(0,0,0,0.1)`
- **Section Padding**: 80px top/bottom (desktop), 40px (mobile)
- **Content Max Width**: 1200px
- **Nav Height**: 72px
- **Nav Border Bottom**: 1px solid rgba(0,0,0,0.06)

---

## Page Layout: HOME

### 1. Navigation (sticky, all pages)
```
[Logo: "Vaccine Vets" DM Serif 24px] --- [Locations] [Blog] [FAQ] [Contact] --- [Find a Clinic (pill, Bright Ocean)]
```
- Height: 72px
- Background: white
- Border bottom: 1px solid rgba(0,0,0,0.06)
- Logo links to /
- CTA button: 44px height, pill shape, Bright Ocean bg, white text

### 2. Hero Section
```
[Left: Text]                    [Right: Image (clinic photo, rounded 16px)]
  SECTION_LABEL: "PET VACCINES"
  HERO_TITLE: "Affordable pet vaccines,\nmade easy."
  HERO_SUBTITLE: "Licensed vets at local dog parks every weekend.\nNo appointment needed."
  [Find a Clinic Near You (pill button, Bright Ocean)] [Learn More (text link)]
```
- Background: Porcelain (#F9F7F3)
- Layout: 2 columns (55% text / 45% image)
- Padding: 80px top, 100px bottom
- Image: clinic1.jpg, border-radius 16px, subtle shadow
- Badge above title: "FREE RABIES VACCINE" in Bright Ocean Light bg

### 3. Trust Bar (logos/stats)
```
[6 locations] --- [Licensed Vets] --- [500+ pets vaccinated] --- [Weekend clinics]
```
- Background: white
- Layout: 4 columns, centered
- Icons: simple, minimal
- Text: Card Desc style
- Padding: 40px top/bottom
- Border top/bottom: 1px solid rgba(0,0,0,0.06)

### 4. Next Clinics (UpcomingClinics component)
```
SECTION_LABEL: "UPCOMING CLINICS"
SECTION_TITLE: "Find one near you"
[UpcomingClinics component - already built, use componentId: lMioySo]
```
- Background: white
- Padding: 80px top/bottom

### 5. How It Works
```
SECTION_LABEL: "HOW IT WORKS"
SECTION_TITLE: "Three steps, zero stress"
SECTION_DESC: "No waiting rooms, no appointments..."

[1. Walk Up]          [2. Choose Package]      [3. Done - Go Play!]
 Icon (green circle)   Icon (green circle)      Icon (green circle)
 Card Title             Card Title               Card Title
 Card Desc              Card Desc                Card Desc
```
- Background: Porcelain
- 3 column cards with Porcelain bg, white card bg
- Cards: padding 32px, border-radius 16px, shadow
- Step numbers in green circles (48px)
- Padding: 80px top/bottom

### 6. Packages & Pricing
```
SECTION_LABEL: "PACKAGES & PRICING"
SECTION_TITLE: "Simple pricing, serious savings"
SECTION_DESC: "Every package includes a free rabies vaccine..."

[Basic $55]          [Plus $95 - POPULAR]      [Complete $135]
 Porcelain bg         Bright Ocean bg           Porcelain bg
 Label                White label               Label
 Price (DM Serif)     White Price               Price
 Description          White Description          Description
 [Choose Basic]       [Choose Plus]              [Choose Complete]
  outline button       white button               outline button
```
- Background: white
- 3 equal-width cards, gap 24px
- Popular card: Bright Ocean bg, all text white
- Other cards: Porcelain bg, standard text
- Each card has CTA button at bottom
- Card padding: 40px, border-radius 16px
- Padding: 80px top/bottom

### 7. Feature Cards (photo grid)
```
[Walk-ins Welcome]   [Licensed Vets]   [Affordable Care]
 Full photo bg        Full photo bg      Full photo bg
 Frosted overlay      Frosted overlay    Frosted overlay
 at bottom            at bottom          at bottom
```
- 3 columns, height 440px
- Images: clinic1.jpg, pet1.jpg, clinic2.jpg
- Frosted glass text overlay at bottom: rgba(255,255,255,0.85), border-radius 12px
- Padding: 80px top/bottom

### 8. Reviews
```
SECTION_TITLE: "Loved by pet families"

[Quote card 1]   [Quote card 2]   [Quote card 3]
 "Quote text..."   "Quote text..."   "Quote text..."
 - Name            - Name            - Name
   Role              Role              Role
```
- Background: Porcelain
- 3 column cards, white bg, shadow, border-radius 16px
- Quote text in Card Title (italic if possible)
- Card padding: 32px, height: 280px
- Padding: 80px top/bottom

### 9. Instagram Section
```
SECTION_LABEL: "FOLLOW US ON INSTAGRAM"
[@vaccinevets]

[Photo 1]  [Photo 2]  [Photo 3]
```
- 3 images, border-radius 12px, height 380px
- Different images: pet1.jpg, pet2.jpg, pet3.jpg
- Hover: subtle scale(1.02) effect
- Padding: 80px top/bottom

### 10. Host CTA Banner
```
SECTION_LABEL: "HOST A CLINIC"
SECTION_TITLE: "Bring Vaccine Vets to your location"
SECTION_DESC: "We partner with dog parks, pet stores..."
[Get Started (pill button, Bright Ocean)]
```
- Background: Vanilla Custard (#EDDEA4) - warm accent!
- Border-radius: 20px
- Centered text, padding 60px
- Margin: 0 auto, max-width 960px

### 11. FAQ Accordion
```
SECTION_TITLE: "Frequently asked questions"
[Accordion items - 6 Q&As]
```
- Background: white
- Max-width: 720px centered
- Clean accordion with + / - icons
- Padding: 80px top/bottom

### 12. Footer
```
[Vaccine Vets logo]  [Quick Links]  [Help]  [Legal]  [Connect]
                      Home           FAQ     Privacy   Instagram
                      Locations      Contact Terms     Facebook
                      Blog           Host    Access.   Email

[divider line]
[Copyright 2026 Vaccine Vets. All rights reserved.]
```
- Background: Ink Black (#131B23) - dark footer!
- Text: white / rgba(255,255,255,0.6) for links
- Padding: 60px top, 40px bottom
- Logo in white version (logovvwhite.png)

---

---

## Mobile Responsive (Breakpoints)

Framerでは Desktop / Tablet / Mobile の3ブレークポイントを設定。

### Breakpoints
| Device | Width | Columns |
|---|---|---|
| Desktop | 1200px | 3 col grid |
| Tablet | 810px | 2 col grid |
| Mobile | 390px | 1 col stack |

### Global Mobile Rules
- **Content padding**: 20px left/right (Desktop: 0)
- **Section padding**: 60px top/bottom (Desktop: 80px)
- **Nav height**: 60px (Desktop: 72px), hamburger menu
- **CTA button**: full-width on mobile (`width: 100%`)

### Section-by-Section Mobile Adjustments

#### Nav
- Desktop: horizontal links + pill CTA
- Mobile: logo left + hamburger right → overlay menu (full screen, white bg)
- Menu items stacked vertically, 48px tap targets
- CTA button at bottom of menu, full-width

#### Hero
- Desktop: 2 columns (text left / image right)
- Tablet: 2 columns (50/50)
- Mobile: **stack vertical** — image on top (full width, 240px height), text below
- Hero Title: 64px → **36px** mobile
- Hero Subtitle: 20px → **17px** mobile
- Padding: 80px → **48px** mobile

#### Trust Bar
- Desktop: 4 columns horizontal
- Mobile: **2x2 grid** (2 columns, 2 rows)
- Icon + text stacked vertically in each cell

#### Upcoming Clinics
- Component handles its own responsiveness
- Cards stack vertically on mobile

#### How It Works
- Desktop: 3 columns
- Tablet: 3 columns (narrower)
- Mobile: **1 column stack**, cards full-width
- Gap: 30px → 16px

#### Packages & Pricing
- Desktop: 3 columns
- Tablet: 3 columns (narrower padding)
- Mobile: **1 column stack**, Popular card first (reorder!)
- Card padding: 40px → 24px
- Price font: 48px → 40px

#### Feature Cards (photo grid)
- Desktop: 3 columns, 440px height
- Tablet: 3 columns, 320px height
- Mobile: **1 column stack**, 280px height each
- Frosted overlay: same treatment

#### Reviews
- Desktop: 3 columns
- Tablet: 2 columns + 1
- Mobile: **horizontal scroll** (snap scroll) or 1 column stack
- Card height: auto on mobile

#### Instagram
- Desktop: 3 photos
- Mobile: **horizontal scroll** (3 photos, snap), 280px height
- Or 1 column stack

#### Host CTA Banner
- Padding: 60px → 32px mobile
- Border-radius: 20px → 12px mobile
- Title: 44px → 28px mobile

#### FAQ Accordion
- Max-width: 720px → full-width mobile
- Touch-friendly tap targets (48px+ height per question)

#### Footer
- Desktop: horizontal columns
- Mobile: **1 column stack**, each group stacked
- Logo at top, copyright at bottom
- Link groups collapsible (optional)
- Padding: 60px → 40px mobile

### Typography Scale (Mobile Override)
| Style | Desktop | Mobile |
|---|---|---|
| Hero Title | 64px | 36px |
| Section Title | 44px | 28px |
| Section Desc | 18px | 16px |
| Price | 48px | 40px |
| Card Title | 20px | 18px |
| Card Desc | 15px | 14px |
| Nav Link | 15px | 16px (larger tap target) |

### Touch / UX Guidelines
- All interactive elements: minimum 44x44px tap target
- Buttons: full-width on mobile, 48px height
- Card gap: 16px on mobile (24px desktop)
- Image border-radius: 12px on mobile (16px desktop)
- Horizontal scroll sections: scroll-snap-type: x mandatory
- No hover effects on mobile (tap only)

---

## Page: LOCATIONS
1. Nav (same)
2. Hero: "Our Locations" + map or description
3. Location Cards (6): 3x2 grid, photo bg + frosted overlay with name
4. CTA: "Don't see your neighborhood? Host a Clinic"
5. Footer

## Page: BLOG
1. Nav
2. Hero: "Blog" title
3. Featured Article (large card, full-width image)
4. Article Grid (3 columns) - connected to CMS
5. Footer

## Page: FAQ
1. Nav
2. Hero: "Frequently Asked Questions"
3. Accordion sections (2 groups of 3)
4. CTA: "Still have questions? Contact Us"
5. Footer

## Page: CONTACT
1. Nav
2. Hero: "Get in Touch"
3. HubSpot Form (componentId: H5wdaQK)
4. Contact info (email, social links)
5. Footer

## Page: HOST A CLINIC
1. Nav
2. Hero: "Host a Vaccine Clinic" + benefits
3. How It Works (3 steps)
4. Requirements / What we provide
5. Apply Now CTA + HubSpot booking link
6. Footer

---

## Assets (GitHub: masahiro97/vv-assets)
- clinic1-5.jpg — clinic photos
- host1-3.jpg — hosting photos
- pet1-4.jpg — pet photos
- logo.png — dark logo
- logovvwhite.png (in Marketing-Design folder) — white logo for dark footer

## CMS (already set up)
- Articles Collection (qBZRCemR4): 5 articles with full content
- Fields: Title, Date, Image, Content

## Code Components (already built)
- DynamicHero (ZZDxULT) — configurable hero
- HubSpotForm (H5wdaQK) — contact form
- UpcomingClinics (lMioySo) — live clinic schedule

---

## Route Ops → Lovable 連携計画

### 概要
Route Opsでロケーションのstageが `active` or `test_open` に変わったら、Lovable（Supabase）にWebhookでpushし、vaccinevets.comのLocationsページに自動反映する。

### アーキテクチャ
```
Route Ops DynamoDB Stream
  → Lambda (webhook-sync)
    → Lovable Supabase Edge Function (sync-location)
      → public_locations テーブルに upsert/delete
        → Lovable Locations ページで表示
```

### Route Ops側（実装する）
1. **CDK**: DynamoDB Stream トリガー Lambda 追加
2. **Lambda `webhook-sync`**:
   - Stream eventから `NewImage` / `OldImage` を取得
   - stageが `active` or `test_open` に変更 → Supabase Edge Functionに `upsert` POST
   - stageがそれ以外に変更（or 削除）→ `delete` POST
   - 送信データ: `id`, `name`, `addr`, `lat`, `lng`, `pattern`, `slot`, `place_id`, `stage`
3. **環境変数**: `LOVABLE_SYNC_URL`, `LOVABLE_SYNC_TOKEN`（GitHub Secrets経由）

### Lovable/Supabase側（実装する）
1. **Supabase テーブル `public_locations`**:
   - `id` (text, PK) — Route OpsのロケーションULID
   - `name` (text)
   - `addr` (text)
   - `lat` (float)
   - `lng` (float)
   - `pattern` (text) — e.g. "Every Saturday"
   - `slot` (text) — s1=Morning, s2=Midday, s3=Afternoon, s4=Evening
   - `place_id` (text) — Google Places ID（写真取得用）
   - `stage` (text) — active / test_open
   - `updated_at` (timestamptz)

2. **Supabase Edge Function `sync-location`**:
   - POST, Bearer token認証
   - Body: `{ "action": "upsert" | "delete", "location": {...} }`
   - upsert → `public_locations` にinsert or update
   - delete → `public_locations` から該当IDを削除

3. **Locationsページ更新**:
   - `public_locations` テーブルからデータ取得
   - 各ロケーションカード表示:
     - 拠点名
     - 営業時間（pattern + slot → "Every Saturday, Morning (9am-12pm)" 等に変換）
     - Google Map埋め込み（lat/lng）
     - Google Places写真（place_id）
   - slotの表示変換:
     - s1 = "Morning (9:00 AM – 11:00 AM)"
     - s2 = "Midday (11:00 AM – 1:00 PM)"
     - s3 = "Afternoon (1:00 PM – 3:00 PM)"
     - s4 = "Evening (3:00 PM – 5:00 PM)"

### 実装順序
1. Lovable: Supabaseテーブル + Edge Function作成
2. Route Ops: webhook-sync Lambda + CDK追加
3. Route Ops: 既存active/test_openロケーションの初期同期（backfill）
4. Lovable: Locationsページ更新
5. テスト: Route Opsでstage変更 → vaccinevets.com反映確認

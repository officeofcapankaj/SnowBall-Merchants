# SnowBall Merchants - Yarn & Fabric E-commerce Website

## Project Overview
- **Project Name**: SnowBall Merchants
- **Type**: E-commerce website (Single-page application with multiple sections)
- **Core Functionality**: A comprehensive online catalog for yarn and fabric products with shopping cart and order placement
- **Target Users**: Retail buyers, crafters, textile businesses, fashion designers

---

## UI/UX Specification

### Layout Structure

**Header (Fixed)**
- Logo: "SnowBall Merchants" with snowflake icon
- Navigation: Home | Yarn | Fabric | About | Contact
- Cart icon with item count badge
- Mobile: Hamburger menu

**Hero Section**
- Full-width banner with layered background
- Headline: "Premium Yarns & Fabrics for Every Creation"
- Subtext: "Discover our curated collection of quality textiles"
- CTA Button: "Explore Collection"

**Yarn Catalog Section**
- Section title: "Our Yarn Collection"
- Filter sidebar (left): Material type, Weight, Price range
- Product grid (right): 3 columns desktop, 2 tablet, 1 mobile

**Fabric Catalog Section**
- Section title: "Premium Fabrics"
- Filter sidebar (left): Material, Type, Color family
- Product grid (right): 3 columns desktop, 2 tablet, 1 mobile

**Shopping Cart (Slide-out Panel)**
- Right-side sliding panel
- Item list with quantity controls
- Subtotal calculation
- Checkout button
- Empty cart message when no items

**Order Form Modal**
- Customer details: Name, Email, Phone, Address
- Order summary
- Submit order button

**Footer**
- Company info, Quick links, Contact details
- Social media icons
- Copyright

### Responsive Breakpoints
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px

### Visual Design

**Color Palette**
- Primary: #1a3a4a (Deep Teal)
- Secondary: #f8f4f0 (Warm Cream)
- Accent: #c9a87c (Golden Tan)
- Highlight: #8b5e3c (Warm Brown)
- Text Primary: #2d2d2d
- Text Secondary: #666666
- White: #ffffff
- Success: #4a7c59
- Error: #a64b4b

**Typography**
- Headings: "Playfair Display", serif
- Body: "Source Sans 3", sans-serif
- Logo: "Playfair Display", serif, 700 weight
- H1: 48px / 36px mobile
- H2: 32px / 28px mobile
- H3: 24px / 20px mobile
- Body: 16px
- Small: 14px

**Spacing System**
- Section padding: 80px vertical, 5% horizontal
- Card padding: 24px
- Grid gap: 24px
- Element spacing: 16px

**Visual Effects**
- Box shadows: 0 4px 20px rgba(0,0,0,0.08)
- Hover shadows: 0 8px 30px rgba(0,0,0,0.12)
- Border radius: 12px (cards), 8px (buttons), 4px (inputs)
- Transitions: 0.3s ease for all interactive elements
- Subtle texture overlay on hero section

### Components

**Product Card**
- Image container (aspect ratio 4:3)
- Category badge (yarn/fabric)
- Product name
- Material details
- Price per unit
- "Add to Cart" button
- Hover: lift effect with shadow

**Filter Panel**
- Collapsible sections
- Checkbox options with counts
- Price range slider
- Clear filters button

**Cart Item**
- Product thumbnail
- Name and variant
- Quantity selector (+/-)
- Line total
- Remove button

**Buttons**
- Primary: Teal background, cream text
- Secondary: Transparent with teal border
- Accent: Golden tan background
- Hover: Darken 10%, scale 1.02

**Form Inputs**
- Border: 1px solid #ddd
- Focus: Border color #1a3a4a, subtle shadow
- Padding: 12px 16px
- Label above input

---

## Functionality Specification

### Product Data

**Yarn Types (12 products)**
1. Merino Wool - 100% merino, DK weight, $18.99
2. Cashmere Blend - 70% cashmere/30% silk, Lace weight, $45.99
3. Organic Cotton - 100% organic cotton, Worsted, $12.99
4. Alpaca Supreme - 100% baby alpaca, Bulky, $28.99
5. Bamboo Silk - 70% bamboo/30% silk, Fingering, $22.99
6. Linen Natural - 100% Belgian linen, DK, $19.99
7. Synthetic Blend - 80% acrylic/20% wool, Worsted, $8.99
8. Angora Cloud - 100% angora, Fingering, $35.99
9. Hemp Cord - 100% hemp, Heavy, $9.99
10. Silk Thread - 100% mulberry silk, Lace, $52.99
11. Recycled Wool - 100% recycled wool, Aran, $14.99
12. Mohair Fluff - 100% kid mohair, Lace, $29.99

**Fabric Types (12 products)**
1. Egyptian Cotton - 100% cotton, 150 GSM, $24.99/m
2. Pure Silk Charmeuse - 100% silk, 19 momme, $89.99/m
3. Belgian Linen - 100% organic linen, 200 GSM, $49.99/m
4. Japanese Denim - 100% cotton, 14oz, $38.99/m
5. Velvet Luxe - 100% polyester velvet, $32.99/m
6. French Terry - 85% cotton/15% polyester, 280 GSM, $22.99/m
7. Silk Satin - 100% silk, 12 momme, $75.99/m
8. Canvas Heavy - 100% cotton, 400 GSM, $18.99/m
9. Chiffon Sheer - 100% polyester, $15.99/m
10. Flannel Warm - 100% cotton, 180 GSM, $19.99/m
11. Tweed Classic - 80% wool/20% poly, $45.99/m
12. Jersey Knit - 95% cotton/5% elastane, $21.99/m

### Core Features

**Product Catalog**
- Display all products in grid format
- Category tabs: All | Yarn | Fabric
- Filter by material type
- Filter by price range
- Sort by: Name, Price Low-High, Price High-Low

**Shopping Cart**
- Add products to cart
- Adjust quantities (min 1)
- Remove items
- Calculate subtotal
- Persist cart in localStorage
- Show cart item count in header

**Order Placement**
- Open checkout modal
- Form validation (required fields)
- Submit order (store in localStorage)
- Show success confirmation
- Clear cart after order

### User Interactions
- Smooth scroll to sections
- Filter updates product grid instantly
- Cart panel slides from right
- Modal overlays with backdrop
- Toast notifications for actions

### Data Handling
- Products stored in JavaScript array
- Cart stored in localStorage
- Orders stored in localStorage
- Form validation with error messages

### Edge Cases
- Empty cart message
- No products matching filter
- Form validation errors
- Prevent duplicate cart items (update quantity instead)

---

## Acceptance Criteria

### Visual Checkpoints
- [ ] Header is fixed and shows cart count
- [ ] Hero section has layered background effect
- [ ] Product cards have hover lift animation
- [ ] Filter panel collapses on mobile
- [ ] Cart slides in smoothly from right
- [ ] Modal has proper overlay and close functionality
- [ ] All colors match the specified palette
- [ ] Typography uses specified fonts
- [ ] Responsive at all breakpoints

### Functional Checkpoints
- [ ] Can filter yarn products by material
- [ ] Can filter fabric products by type
- [ ] Can sort products by price
- [ ] Can add product to cart
- [ ] Cart persists on page refresh
- [ ] Can adjust quantity in cart
- [ ] Can remove items from cart
- [ ] Checkout form validates required fields
- [ ] Order submission shows success message
- [ ] Cart clears after order placement

---

## Technical Implementation
- Single HTML file with embedded CSS and JavaScript
- No external frameworks (vanilla JS)
- Google Fonts for typography
- SVG icons embedded
- CSS custom properties for theming
- LocalStorage for data persistence
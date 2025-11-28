# Design Guidelines: Zeeshan's Portfolio Website

## Design Approach
**Reference-Based: Modern Developer Portfolio Aesthetic**
Drawing inspiration from Linear's clean minimalism, Vercel's technical sophistication, and contemporary AI company landing pages (OpenAI, Anthropic). The design will embody a futuristic developer aesthetic with glass morphism, subtle gradients, and refined typography.

## Typography System
- **Primary Font**: 'Inter' or 'SF Pro Display' (Google Fonts CDN)
- **Accent Font**: 'JetBrains Mono' for code-related elements
- **Hierarchy**:
  - Hero Headline: text-5xl to text-7xl, font-bold
  - Section Headings: text-3xl to text-4xl, font-semibold
  - Subheadings: text-xl to text-2xl, font-medium
  - Body Text: text-base to text-lg, font-normal
  - Small Text/Captions: text-sm, font-light

## Layout System
**Spacing Primitives**: Tailwind units of 4, 6, 8, 12, 16, 20, 24
- Consistent section padding: py-20 desktop, py-12 mobile
- Component spacing: gap-8 for grids, gap-6 for lists
- Container: max-w-7xl with px-6 to px-8

## Core Sections & Components

### 1. Hero Section (Full viewport height: min-h-screen)
- **Layout**: Two-column split on desktop (60/40), stacked on mobile
- **Left Column**: Name (text-6xl), dynamic rotating tagline showcasing different skills, dual CTA buttons with backdrop-blur glass effect
- **Right Column**: Professional photo with gradient border/glow effect, floating card aesthetic
- **Background**: Subtle animated gradient mesh or dot grid pattern
- **CTAs**: Primary "View Projects" + Secondary "Contact Me" with blurred backgrounds

### 2. About Section
- **Layout**: Single column, max-w-4xl centered
- **Structure**: 
  - Brief intro paragraph highlighting No-Code + AI expertise
  - Education badge (Southeast University CSE)
  - Key achievements grid: 3 stat cards (50+ Tools Built, Bangladesh Based, Web3 Interest)
- **Stats Cards**: Glass morphism cards with backdrop-blur, subtle borders

### 3. Skills & Tools Section
- **Layout**: Two subsections
  - **AI Platforms**: Horizontal scroll cards or 4-column grid showcasing tool logos/names (Replit AI, Cursor AI, GitHub Copilot, Vercel AI SDK, Framer AI, Dora AI, Typedream AI)
  - **Technologies**: Badge/pill layout for HTML, CSS, JavaScript, React, React Native
- **Card Style**: Minimal borders, glass effect, hover lift animation

### 4. Projects Showcase
- **Layout**: Masonry grid or 3-column card grid
- **Card Structure**:
  - Project thumbnail/icon placeholder
  - Project title
  - Brief tech stack tags
  - GitHub link icon
- **GitHub CTA**: Prominent "View All 50+ Tools on GitHub" button with external link icon
- **Grid**: grid-cols-1 md:grid-cols-2 lg:grid-cols-3, gap-8

### 5. Services Section
- **Layout**: 2-column grid on desktop, single column mobile
- **Services Cards**:
  - Website Development (AI & No-Code)
  - Mobile App Development (React Native, Expo)
  - AI Tools & Automation
  - Web3/Blockchain Solutions
- **Card Design**: Icon at top, heading, description, glass morphism with subtle gradients

### 6. Contact Section
- **Layout**: Centered, max-w-2xl
- **Structure**:
  - Heading: "Let's Build Something Amazing"
  - Two primary contact methods as large, interactive cards:
    - WhatsApp card with direct link (+8801860645994)
    - Email card (zeeshan9or@gmail.com)
  - GitHub profile link
- **Cards**: Glass effect with icon, label, and hover scale animation

### 7. Footer
- Minimal design: Name, tagline, social links (GitHub), copyright
- Single row layout, py-8

## Component Library

### Glass Morphism Cards
- backdrop-blur-lg with semi-transparent backgrounds
- Subtle border (border-opacity-20)
- Rounded corners: rounded-xl to rounded-2xl

### Buttons
- Primary: Solid with backdrop-blur for hero/image contexts
- Secondary: Ghost/outline style
- Rounded: rounded-full or rounded-lg
- Padding: px-8 py-3 for CTAs

### Icons
**Font Awesome CDN** for:
- Social icons (GitHub, WhatsApp, Email)
- Service icons (Code, Mobile, AI, Blockchain)
- External link indicators
- Tech stack icons where available

### Badges/Pills
- Technology tags: rounded-full, px-4 py-2, text-sm
- Semi-transparent backgrounds with borders

## Animations & Interactions
- Hero tagline: Rotating text animation cycling through roles
- Cards: Subtle hover lift (translate-y-2) with transition-all duration-300
- Gradient backgrounds: Slow animated gradient shifts
- Scroll fade-in for sections (stagger effect)
- Glass morphism shimmer on hover

## Images

### Hero Section Image
- **Description**: Professional photo of Zeeshan wearing a navy suit in a modern indoor environment
- **Placement**: Right side of hero section (desktop), centered (mobile)
- **Treatment**: Floating card with gradient border glow, rounded-2xl, subtle shadow
- **Size**: Approximately 400-500px width on desktop

### Project Thumbnails (Placeholders)
- Generic tech/code illustrations or gradient backgrounds
- Aspect ratio: 16:9 or 4:3
- Can be replaced with actual project screenshots later

## Responsive Breakpoints
- Mobile: < 768px (single column, stacked layouts)
- Tablet: 768px - 1024px (2-column where appropriate)
- Desktop: > 1024px (full multi-column layouts)

## Performance Considerations
- Lazy load project cards
- Optimize hero image with appropriate formats
- Minimal animation overhead
- Icon font/SVG sprites

## SEO Structure
- Semantic HTML5: header, main, section, footer
- H1 for name, H2 for section headings
- Meta description highlighting skills and expertise
- Open Graph tags for social sharing

This design creates a sophisticated, modern portfolio that positions Zeeshan as a cutting-edge developer while maintaining professional credibility and excellent user experience across all devices.
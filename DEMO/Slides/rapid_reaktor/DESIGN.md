---
name: Rapid Reaktor
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#393939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1c1b1b'
  surface-container: '#201f1f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353534'
  on-surface: '#e5e2e1'
  on-surface-variant: '#b9caca'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#849495'
  outline-variant: '#3a494a'
  surface-tint: '#00dce5'
  primary: '#e9feff'
  on-primary: '#003739'
  primary-container: '#00f5ff'
  on-primary-container: '#006c71'
  inverse-primary: '#00696e'
  secondary: '#f2fffc'
  on-secondary: '#003732'
  secondary-container: '#00fae7'
  on-secondary-container: '#006f66'
  tertiary: '#fef8ff'
  on-tertiary: '#3c0090'
  tertiary-container: '#e5d7ff'
  on-tertiary-container: '#751fff'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#63f7ff'
  primary-fixed-dim: '#00dce5'
  on-primary-fixed: '#002021'
  on-primary-fixed-variant: '#004f53'
  secondary-fixed: '#08fdea'
  secondary-fixed-dim: '#00decd'
  on-secondary-fixed: '#00201d'
  on-secondary-fixed-variant: '#005049'
  tertiary-fixed: '#e9ddff'
  tertiary-fixed-dim: '#d1bcff'
  on-tertiary-fixed: '#23005b'
  on-tertiary-fixed-variant: '#5700c9'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353534'
typography:
  h1:
    fontFamily: Inter
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.2'
    letterSpacing: -0.02em
  h2:
    fontFamily: Inter
    fontSize: 32px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: -0.01em
  h3:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.5'
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.5'
  mono-label:
    fontFamily: Space Grotesk
    fontSize: 14px
    fontWeight: '500'
    lineHeight: '1.2'
    letterSpacing: 0.05em
  mono-data:
    fontFamily: Space Grotesk
    fontSize: 13px
    fontWeight: '400'
    lineHeight: '1.4'
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 4px
  xs: 8px
  sm: 16px
  md: 24px
  lg: 32px
  xl: 48px
  gutter: 20px
  margin: 32px
---

## Brand & Style

The design system is engineered to evoke a sense of absolute control, precision, and rapid response. It balances the stark minimalism of modern enterprise software with a high-tech "command center" aesthetic. The interface must feel like a precision instrument—authoritative, silent, and highly efficient. 

The visual style leverages **Glassmorphism** to create depth and hierarchy without relying on heavy shadows, utilizing semi-transparent surfaces and blurred backdrops to maintain a sense of lightness despite the dark color palette. A subtle underlying grid pattern reinforces the feeling of a structured, technical environment. The target audience—Security Operations Center (SOC) analysts—requires a UI that minimizes cognitive load while highlighting critical threats through high-contrast accents.

## Colors

The palette is anchored in a deep, nocturnal foundation. The primary background uses a dark navy (#0A192F) to provide atmospheric depth, while surfaces and containers utilize a dark charcoal (#121212) for a flatter, more focused workspace. 

Cyan (#00F5FF) serves as the primary action color and high-priority indicator, providing a vibrant "glow" effect against the dark base. Teal (#14FFEC) acts as a secondary accent, typically used for healthy system states and data visualizations. A deep violet tertiary color is reserved for complex data categorization. Status colors follow industry standards: critical alerts in high-saturation red, warnings in amber, and neutral states in mid-tone grays to ensure the user's eye is drawn only to what matters.

## Typography

This design system utilizes **Inter** for all primary interface elements to ensure maximum legibility and a professional, systematic tone. Headlines feature tighter letter-spacing and heavier weights to command attention.

For technical callouts, IP addresses, logs, and metadata, **Space Grotesk** is employed. Its geometric, technical character mimics a monospace font's utility while maintaining the modern aesthetic of the design system. All monospace-style labels should be set in uppercase with slight tracking to enhance the "high-tech" feel. Line heights are generous in body text to prevent fatigue during long monitoring sessions.

## Layout & Spacing

The layout is built on a **fluid 12-column grid** that maximizes screen real estate, essential for information-dense SOC dashboards. The spacing rhythm is based on a 4px/8px incremental scale, ensuring consistent alignment of technical data.

Margins are kept wide (32px) to allow the content to breathe, while internal component gutters are tighter (20px) to keep related data points grouped. Elements should generally span 3, 4, 6, or 12 columns. In complex data views, a "compact mode" is available which reduces the base spacing unit to 2px for high-density log viewing.

## Elevation & Depth

Visual hierarchy is achieved through **tonal layering and glassmorphism** rather than traditional drop shadows. 

1.  **Base Layer:** The deepest layer (#0A192F navy), often featuring a subtle 24px dot-grid pattern in 5% opacity cyan.
2.  **Surface Layer:** Primary cards and containers using a semi-transparent charcoal (#121212) with a `backdrop-filter: blur(12px)`.
3.  **Border Definition:** Surfaces are defined by 1px solid borders in a low-opacity cyan or gray (e.g., `rgba(0, 245, 255, 0.15)`).
4.  **Interactive Layer:** Active elements or hovered cards increase their border opacity and gain a subtle outer glow (cyan) to indicate focus. 

This approach creates a "stacked glass" effect that feels futuristic and maintains clarity in a dark environment.

## Shapes

The design system adopts a **Soft (Level 1)** roundedness profile. A base radius of 4px (0.25rem) is used for buttons, input fields, and small UI components. Larger containers and cards use a radius of 8px (0.5rem). 

This subtle rounding prevents the interface from feeling too aggressive or "brutalist" while maintaining a precise, engineered appearance. Sharp corners are strictly reserved for internal data table dividers and grid-based decorators to reinforce the technical nature of the product.

## Components

### Buttons
Primary buttons use a solid Cyan (#00F5FF) fill with dark navy text. Secondary buttons are "ghost" style with a 1px Cyan border and transparent background. All buttons feature a 4px corner radius.

### Input Fields
Inputs use a dark, semi-transparent fill with a subtle bottom-border in mid-gray. On focus, the border transitions to Cyan and a faint glow is applied. Labels are set in Space Grotesk, uppercase.

### Cards
Cards are the primary container for data. They feature the glassmorphism effect (backdrop blur) and a 1px border. Card headers should have a subtle 1px divider separating the title from the content.

### Chips & Tags
Used for status and categories. They use a low-opacity fill of the status color (e.g., 10% Red for "Critical") with a high-saturation text color and border.

### Data Tables
Tables are high-density. Row hovering should trigger a subtle background highlight. Use Space Grotesk for numerical data and Inter for descriptive text.

### Additional Components
- **The "Reaktor" Pulse:** A subtle, animated cyan ring used for real-time threat detection indicators.
- **Node Graph Connectors:** Ultra-thin (1px) cyan lines with 40% opacity to map relationships between security entities.
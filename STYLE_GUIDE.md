# Style Guide

## 🎨 Visual Design System

This document outlines the design system and style guidelines for Geek Protocol's web presence.

## Color System

### Primary Colors

```css
--bg: #070717           /* Primary background */
--bg2: #0b0a18          /* Secondary background */
--panel: #101027        /* Card/panel background */
--panel2: #14132b       /* Secondary panel */
--text: #e5e7eb         /* Primary text */
--muted: #9ca3af        /* Secondary text */
--accent: #22d3ee       /* Primary accent (cyan) */
--accent2: #a78bfa      /* Secondary accent (purple) */
--border: rgba(255,255,255,.12)  /* Border color */
```

### Usage Guidelines

- **Backgrounds**: Use gradient combinations for depth
- **Text**: Maintain WCAG AA contrast ratios minimum
- **Accents**: Use for CTAs, links, and important highlights
- **Borders**: Subtle and translucent for modern look

## Typography

### Font Stack

```css
font-family: ui-sans-serif, system-ui, -apple-system, 
             Segoe UI, Roboto, Arial, "Apple Color Emoji", 
             "Segoe UI Emoji";
```

### Heading Scale

| Element | Size | Weight | Line Height |
|---------|------|--------|-------------|
| h1 | 3rem (48px) | Bold | 1.1 |
| h2 | 1.6rem (25.6px) | Bold | 1.2 |
| h3 | 1.05rem (16.8px) | Bold | 1.3 |
| Body | 1rem (16px) | Normal | 1.75 |

### Special Typography

- **Kicker text**: 0.9rem, muted color, uppercase
- **Small notes**: 0.92rem, muted color
- **Chips/Tags**: 0.9rem, normal weight

## Spacing System

Base unit: 4px

Common spacing values:
- xs: 8px
- sm: 12px
- md: 16px
- lg: 22px
- xl: 34px
- 2xl: 56px

## Components

### Buttons & Chips

```css
.chip {
  padding: 8px 12px;
  border-radius: 999px;
  border: 1px solid var(--border);
  background: rgba(255,255,255,.03);
}

.chip:hover {
  background: rgba(255,255,255,.06);
}
```

### Cards & Sections

```css
.section {
  border: 1px solid var(--border);
  border-radius: 18px;
  padding: 22px;
  background: linear-gradient(180deg, 
              rgba(255,255,255,.04), 
              rgba(255,255,255,.02));
}
```

### Callouts

```css
.callout {
  border: 1px solid rgba(34,211,238,.22);
  background: rgba(34,211,238,.08);
  border-radius: 16px;
  padding: 14px 16px;
}
```

## Layout Patterns

### Grid System

Desktop (>980px):
```css
.grid {
  display: grid;
  grid-template-columns: 280px 1fr;
  gap: 22px;
}
```

Mobile (<980px):
```css
.grid {
  grid-template-columns: 1fr;
}
```

### Max Width Content

All content: `max-width: 1040px`

## Effects & Shadows

### Box Shadows

```css
--shadow: 0 0 28px rgba(34,211,238,.22);   /* Primary accent glow */
--shadow2: 0 0 18px rgba(167,139,250,.18); /* Secondary accent glow */
```

### Hover Transitions

All interactive elements should have smooth transitions:
```css
transition: all 0.2s ease;
```

## Responsive Design

### Breakpoints

- **Mobile**: < 560px
- **Tablet**: 560px - 980px
- **Desktop**: > 980px

### Mobile Considerations

- Stack grid layouts vertically
- Increase touch target sizes (minimum 44x44px)
- Adjust font sizes for readability
- Simplify navigation for small screens

## Accessibility

### Color Contrast

All text must meet WCAG AA standards:
- Normal text: 4.5:1 minimum
- Large text: 3:1 minimum

### Focus States

All interactive elements must have visible focus indicators:
```css
:focus-visible {
  outline: 2px solid var(--accent);
  outline-offset: 2px;
}
```

### Keyboard Navigation

- All interactive elements accessible via Tab
- Skip links for main content
- Logical tab order

## Animation Guidelines

### Subtle Animations

Use sparingly and respect `prefers-reduced-motion`:

```css
@media (prefers-reduced-motion: no-preference) {
  .animated {
    transition: transform 0.3s ease;
  }
}
```

### Scroll Behavior

```css
html {
  scroll-behavior: smooth;
}
```

## Best Practices

### Do's ✅

- Use system fonts for performance
- Maintain consistent spacing
- Keep borders subtle and translucent
- Use gradients for depth, not decoration
- Test on multiple devices and browsers
- Ensure accessibility standards are met

### Don'ts ❌

- Don't use pure black backgrounds
- Don't overuse animations
- Don't ignore mobile experience
- Don't sacrifice readability for style
- Don't use low-contrast color combinations

## Code Formatting

### CSS Organization

1. CSS Variables
2. Reset/Base styles
3. Layout
4. Components
5. Utilities
6. Media queries

### Naming Conventions

- Use descriptive class names
- Prefer semantic names over presentational
- Keep names short but meaningful

## Resources

- [WCAG Guidelines](https://www.w3.org/WAI/WCAG21/quickref/)
- [Color Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [CSS Guidelines](https://cssguidelin.es/)

---

**Maintaining consistency across all Geek Protocol properties**

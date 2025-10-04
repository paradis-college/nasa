# Copilot Instructions for NASA Space Weather Educational App

## Project Overview

This repository contains an educational web application about space weather, developed for the NASA Space Apps challenge "Stellar Stories". The application helps students and the general public understand how space weather affects daily life through interactive storytelling and simulations.

## Project Structure

- **`index.html`** - Interactive flipbook presenting "Stellar Stories" that explains space weather through narrative perspectives (farmer, pilot, astronaut, student)
- **`hub.html`** - Main interactive hub featuring:
  - Multiple educational simulations (solar flares, power grid, aurora, etc.)
  - Calendar integration with NASA DONKI API for real space weather events
  - Kid-friendly interface with gamified elements

## Technical Stack

- **Pure HTML/CSS/JavaScript** - No frameworks or build tools
- **NASA DONKI API** - Space Weather Database Of Notifications, Knowledge, Information
- **Client-side only** - Static files that can be served directly

## Code Style & Conventions

### JavaScript
- Use `'use strict';` at the beginning of script blocks
- Prefer `const` for immutable values
- Use arrow functions for callbacks: `array.forEach(item => ...)`
- Use template literals for HTML generation: `` `<div>${variable}</div>` ``
- Use descriptive function names: `escapeHtml()`, `makeContent()`, `setPage()`

### HTML/CSS
- **Inline styles** - CSS is embedded in `<style>` tags within HTML files
- **CSS custom properties** - Use CSS variables for theming: `var(--bg)`, `var(--text)`, etc.
- **Color schemes** - Support both dark and light modes using `@media (prefers-color-scheme: light)`
- **Accessibility** - Always include:
  - `aria-label` for meaningful regions
  - `aria-hidden="true"` for decorative elements
  - `role` attributes for navigation and interactive elements
  - Keyboard navigation support

### Design Principles
- **Kid-friendly** - Use emojis, playful colors, and simple language
- **Educational** - Focus on making space weather concepts accessible and engaging
- **Responsive** - Mobile-first design with proper viewport settings
- **Visual appeal** - Gamified UI with animations, gradients, and modern design

## API Usage

### NASA DONKI API
- **Base URL**: `https://api.nasa.gov/DONKI/`
- **Default API Key**: `o9FIZEgU2itrew0k9Y2qA9RhmeL49feU2B7fGZRR` (demo key)
- **Endpoints used**:
  - `/FLR` - Solar Flares
  - `/CME` - Coronal Mass Ejections
  - `/WSAEnlilSimulations` - Solar wind simulations
  - `/HSS` - High Speed Streams
  - `/GST` - Geomagnetic Storms
  - `/RBE` - Radio Blackouts
  - `/SEP` - Solar Energetic Particles
  - `/notifications` - Event notifications

## Key Features to Maintain

1. **Flipbook Navigation** (index.html)
   - Page turning with smooth 3D transforms
   - Keyboard navigation (arrow keys)
   - Touch/click zones for navigation
   - Status display showing current page

2. **Router System** (hub.html)
   - Hash-based routing: `#simulators`, `#about`, `#calendar`
   - Tab navigation with `aria-current` states
   - Dynamic section showing/hiding

3. **Calendar Integration** (hub.html)
   - Month view with NASA event data
   - Date range queries to DONKI API
   - Event details modal with JSON display
   - Event type color coding

## Development Guidelines

### When Adding Features
- Keep the kid-friendly, educational tone
- Ensure accessibility (ARIA labels, keyboard nav)
- Test in both light and dark color schemes
- Maintain the single-file architecture
- Use semantic HTML elements

### When Modifying Styles
- Update CSS custom properties rather than hardcoding colors
- Test responsive behavior on mobile viewports
- Preserve the gamified visual style (gradients, shadows, animations)
- Keep consistent with existing design patterns

### When Working with Data
- Handle API errors gracefully with user-friendly messages
- Use `escapeHtml()` for any user-generated or API content
- Format dates consistently (ISO format for API, human-readable for display)
- Cache API responses when appropriate to reduce requests

## Testing Considerations

Since this is a static site with no build process:
- **Manual testing** is the primary method
- Test in multiple browsers (Chrome, Firefox, Safari)
- Test on mobile devices and different screen sizes
- Verify API integration with live NASA DONKI endpoints
- Check accessibility with screen readers
- Validate keyboard navigation works throughout

## Educational Context

The application targets:
- **Elementary/middle school students** learning about space weather
- **Teachers** looking for interactive educational resources
- **General public** interested in space weather phenomena

Content should be:
- Age-appropriate and engaging
- Scientifically accurate but simplified
- Connected to real-world impacts (farming, aviation, satellites, etc.)
- Interactive and hands-on where possible

## External Resources

- NASA DONKI API Documentation
- Scratch projects for extended learning
- Roblox games referenced in the flipbook
- Links should open in new tabs for external resources

# SupremeCSS

A premium, copy-paste component library for the web. SupremeCSS provides production-ready interface components built on a single monochrome token system, with accessible markup, built-in light and dark themes, and small self-contained interaction scripts.

Browse the component gallery, preview each component live, and copy the HTML, CSS and JavaScript that fit your product.

## Features

- **Copy-paste ready.** Every component is delivered as semantic HTML, scoped CSS and optional JavaScript. There is no package to install.
- **Dark mode built in.** All colours, surfaces and borders are read from CSS custom properties, so light and dark themes stay consistent without per-component overrides.
- **Zero framework dependency.** Components are plain CSS and small scripts. Icons are the only external asset, loaded from Lucide.
- **Accessible defaults.** Controls are keyboard operable, focus states are visible, icon-only buttons carry labels, and overlays close with Escape.
- **Respects user preferences.** Motion is disabled automatically when the operating system requests reduced motion.
- **Standalone downloads.** Any component can be downloaded as a single HTML file that already includes the base tokens.

## Project structure

SupremeCSS is delivered as a single, self-contained HTML file:

```
supremecss.html   Documentation site, component gallery and all component sources
```

The file contains the Home, Documentation, Components and About pages, and a shared footer. Open it in a browser to explore the library locally.

## Getting started

### 1. Open the gallery

Open `supremecss.html` in any modern browser. The page opens on the Home section. Select **Components** in the top bar to browse the gallery.

### 2. Add the base tokens

Each component depends on a shared set of base tokens that define colour, typography, radius, spacing and motion. Add them once per page:

1. In the gallery, select **Copy base CSS** in the top bar.
2. Paste the result into a `<style>` element in your document `<head>`.

```html
<!doctype html>
<html lang="en" data-theme="light">
<head>
  <meta charset="utf-8">
  <style>
    /* paste "Copy base CSS" here */
  </style>
</head>
<body>
  <!-- your components -->
</body>
</html>
```

### 3. Add a component

Open a component in the gallery and use the **Code** tab to copy its HTML, CSS and JavaScript. Copy all places every part in one block, and **Download** saves a standalone HTML file.

## Icons

Icons are provided by [Lucide](https://lucide.dev), pinned to version 0.469.0. Include the script once, then call `lucide.createIcons()` after your markup is on the page:

```html
<script src="https://unpkg.com/lucide@0.469.0/dist/umd/lucide.min.js"></script>
<i data-lucide="check"></i>
<script>lucide.createIcons();</script>
```

Components that use icons require this script. Standalone downloads that use icons include it automatically.

## Theming

### Dark mode

Set the `data-theme` attribute on the `<html>` element to force a theme:

```html
<html data-theme="dark">
```

The theme toggle in the top bar saves the user's choice in `localStorage` under the key `sc-theme`. When no choice is saved, the page follows the operating system colour scheme.

### Design tokens

Components read their colours from the following CSS custom properties. Override them in your own stylesheet, after the base tokens, to re-theme the library for your brand.

| Token | Purpose | Light | Dark |
| --- | --- | --- | --- |
| `--bg` | Page background | `#ffffff` | `#0b0b0d` |
| `--fg` | Primary text | `#0f0f12` | `#fafafa` |
| `--card` | Card and panel surface | `#ffffff` | `#111113` |
| `--muted` | Subtle fills and tracks | `#f5f5f7` | `#1d1d20` |
| `--muted-fg` | Secondary text | `#6b7280` | `#a1a1aa` |
| `--border` | Dividers and outlines | `#e5e7eb` | 10% white |
| `--primary` | Primary actions and selection | `#18181b` | `#fafafa` |
| `--destructive` | Errors and destructive actions | `#dc2626` | `#ef4444` |

## Components

The library contains dozens of components across ten categories.

| Category | Components |
| --- | --- |
| **Actions** | Button, Icon Button, Ripple Button, Loading Button, Split Button, Like Button, Bookmark Button, Toggle, Toggle Group |
| **Forms** | Input, Floating Label, Search Input, Password Input, Password Strength, Number Stepper, Tags Input, Rating, Segmented Control, Switch, Checkbox, Radio Group, Select, Input OTP, Textarea, Multi-Step Form, Input Group |
| **Data Display** | Card, Glow Card, Fan Stack Cards, Reveal Cards Grid, Product Card, Profile Card, Pricing Card, Animated Counter, Flip Card, Gradient Border Card, Avatar Group, Table, Timeline, Heatmap, Tree View, QR Card |
| **Feedback** | Alert, Toast, Progress, Skeleton, Spinner, Animated Check, Live Indicator, Typing Indicator, Confetti |
| **Overlays** | Sheet, Popover, Dropdown Menu, Tooltip, Hover Card, Command Palette |
| **Navigation** | Accordion, Tabs, Breadcrumb, Pagination, Filter Chips, Filter Tabs, Progress Steps |
| **Layout** | Marquee, Bento Grid |
| **Charts** | Bar Chart, Donut Chart, Line Chart, Progress Ring, Sparkline |
| **Content** | Typography, Typewriter, Message, Scrolling Messages, Code Block, Callout, Testimonial, Kbd |
| **Widgets** | Music Player, Stopwatch, Poll, Color Picker, Audio Waveform, Password Generator, Notification Bell |

## Accessibility

- Select, Command Palette and Search support the arrow keys, Enter to confirm and Escape to close.
- Icon-only buttons include an `aria-label` describing their action.
- Interactive elements show a visible focus ring when reached by the keyboard.
- Animations are reduced when the operating system requests reduced motion.

## Browser support

SupremeCSS targets current evergreen browsers. Several components use `color-mix()`, which requires a browser released in 2023 or later. Older browsers display components with reduced colour variation but remain usable.

## Keyboard shortcuts

| Shortcut | Action |
| --- | --- |
| `Ctrl/⌘ + K` | Open component search |
| `←` / `→` | Previous or next component |
| `F` | Toggle full screen preview |
| `Esc` | Close overlays and exit full screen |

## Contributing

Contributions, bug reports and suggestions are welcome. Please open an issue describing the problem or proposal, and include the component name, the browser and operating system you are using, and steps to reproduce any defect.

## License

License to be confirmed. Add the chosen licence file to the repository before publishing.

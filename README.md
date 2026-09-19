# Liquid Glass — a Jellyfin theme

A frosted-glass ("Liquid Glass") theme for the Jellyfin web client, inspired by Apple's design language. Performance-first: glass blur is applied only to floating chrome (header, drawer, dialogs, login card) at a modest 16px radius, while content surfaces use cheap translucent solids — smooth 60fps scrolling even on modest hardware.

## Features

- Aurora gradient backdrop with layered glass panels
- Glass restricted to floating layers only (following HIG-style guidance) — cards, buttons and lists stay cheap to render
- Capsule primary buttons, rounded cards, subtle hover lift (translate only, no image re-rasterization)
- iOS-style grouped inset lists on settings pages
- Responsive: phone / tablet / foldable (folded & unfolded) / desktop / TV layouts
- Safe-area aware (notches), ≥44px touch targets, TV focus rings
- Respects `prefers-reduced-transparency` and `prefers-reduced-motion` (scoped so dialogs never break)
- Built-in, encoding-independent rewrite of all Material Icons glyph rules (fixes icon mojibake like `îŸ½` in Safari and some WebViews, where Jellyfin's icon CSS — raw UTF-8 bytes served without charset — is decoded as Latin-1)

## Install

Dashboard → General → Branding → Custom CSS, either paste the whole file, or import it:

```css
@import url("https://cdn.jsdelivr.net/gh/aoxzh/jellyfin-liquid-glass@main/liquid-glass.css");
```

## Compatibility

Targets the classic jellyfin-web class names; works on Jellyfin 10.9+ including 12.x. Applies to web and web-wrapped clients (Android/iOS apps).

## License

MIT

# iOS Navigation Patterns

## Tab Bar (Primary Navigation)

The tab bar provides access to main app destinations.

- **Position**: Bottom of screen, always visible (except modals/keyboards)
- **Items**: 2-5 tabs maximum
- **Overflow**: Use "More" tab if >5 destinations needed
- **Selected state**: Fill color indicates active tab
- **Labels**: 10-11pt SF text
- **Background**: Slightly translucent with background blur ("frosted glass")

**Behavior**:
- Each tab remembers its navigation state
- Tapping active tab returns to root screen of that tab
- Tab bar hidden during modals and keyboard display

## Navigation Bar (Contextual Navigation)

- **Back button**: Top-left, allows return to previous screen
- **Actions**: Top-right, context-specific actions
- **Title**: Center (scrolled state) or left-aligned large title (unscrolled)

**Scroll Behavior**:
- Large title collapses to compact centered title on scroll
- Search bar can move or hide on scroll
- Smooth animated transitions between states

## Navigating Back

| Method | Context |
|--------|---------|
| "Back" button (top-left) | Standard navigation |
| Swipe right from left edge | Standard navigation |
| "Cancel" / "Done" button | Modal views |
| Swipe down on content | Modals, fullscreen media |

## Modal Sheets

Use modals for focused tasks that shouldn't interrupt context completely.

- Slides up from bottom
- Previous screen visible (recessed) in background
- Dismiss via: close button, swipe down, or completing task

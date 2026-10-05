# Accessibility Audit

## Baseline Audit

- Tool: Lighthouse 13.5.0, Accessibility category
- Tested: October 4, 2026, at `http://127.0.0.1:8765/`
- Score: 83/100
- Automated findings:
  - Insufficient contrast for the navigation links and footer text (`#555` on `#333`) and the form heading (`#999` on `#eee`).
  - Heading hierarchy skipped from the page's `h1` to `h3` headings.
  - The page did not have a main landmark.
- Source review also identified form controls without persistent labels, a clickable `div` instead of a keyboard-operable button, placeholder navigation links, and removed focus outlines.

## Fixes

- Replaced generic layout containers with navigation, header, main, section, and footer landmarks; added a skip link and corrected section headings to `h2`.
- Linked the navigation to the home, about, and contact sections.
- Added visible labels and autocomplete attributes to all form fields, and changed the send control to a real submit button.
- Improved text contrast, added a dark overlay behind the hero title, and provided visible keyboard focus indicators.
- Marked the decorative phone icon as hidden from assistive technology.
- Preserved the original page copy.

## Follow-up Audit

- Tool: Lighthouse 13.5.0, Accessibility category
- Score: 100/100
- Failed automated accessibility checks: none

Lighthouse is an automated check and cannot establish that every interaction is usable with assistive technology. A screen-reader usability test was not performed. The contact form retains its original placeholder action (`#`) and does not send messages to a backend.

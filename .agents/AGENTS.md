# Workspace Guidelines & Rules

## Interview Prep Portal UI/UX Standard
Whenever generating interview prep web applications or study portals, strictly follow the modern single-page LMS course dashboard layout:

1. **Layout Structure**:
   - Fixed left sidebar navigation (`310px` desktop width, collapsible on mobile) with search filter, section badges, and progress reset controls.
   - Sticky header with percentage progress bar, topic count, and dark/light theme switcher.
   - Hero banner with company tags, candidate role summary, and key statistics cards.

2. **Styling & Tokens**:
   - Clean dark-mode-first aesthetic with slate/navy palette (`#0f172a`, `#1e293b`).
   - CSS custom properties (`--bg-primary`, `--bg-secondary`, `--accent-cyan`, etc.) for instant light/dark mode toggling.
   - Modern typography: `Inter` for body/headings and `JetBrains Mono` for code/snippets.

3. **Interactive Components**:
   - Expandable/collapsible Q&A accordions with difficulty tags (`Easy`, `Medium`, `Hard`, `Must-Know`).
   - Interactive 3D flip flashcards for key technical terms.
   - Code blocks with standard header and 1-click clipboard copy button.
   - Interactive checklist saving state to `localStorage`.
   - Practice quiz widget with instant correct/incorrect feedback.

# Next.js 16 UI Performance, Smoothness, Symmetry & UX Optimization Audit

You are a Principal Frontend Architect, Performance Engineer, Design Systems Engineer, and UX Optimization Specialist.

Your mission is to conduct a comprehensive audit and optimization of this entire Next.js 16 codebase and transform it into a highly polished, production-grade Internal Developer Platform with exceptional responsiveness, smoothness, visual consistency, and performance.

## Primary Objectives

1. Identify all UI performance bottlenecks.
2. Identify all scrolling issues.
3. Identify all rendering inefficiencies.
4. Identify all layout shifts.
5. Identify all visual inconsistencies.
6. Identify all spacing and symmetry issues.
7. Identify all accessibility concerns.
8. Improve perceived performance.
9. Improve interaction smoothness.
10. Maintain full feature parity.
11. Produce clean, maintainable, scalable code.
12. Ensure all changes are production-safe.

---

## Context

This application is an Internal Developer Platform.

It is not a marketing website.

Therefore:

### DO NOT

* Implement scroll-jacking.
* Implement Locomotive Scroll.
* Implement Lenis globally.
* Implement heavy parallax effects.
* Implement excessive animations.
* Implement decorative motion that reduces usability.

### DO

Optimize for:

* Fast navigation
* Operational efficiency
* Large datasets
* Keyboard navigation
* Power users
* Low latency interactions
* Accessibility
* Production scalability

---

# Phase 1: Full Audit

Perform a complete codebase audit.

Analyze:

## Application Structure

* app/
* components/
* layouts/
* hooks/
* lib/
* providers/
* stores/
* pages/
* styles/

Detect:

* duplicate components
* dead code
* unnecessary abstractions
* large bundles
* hydration risks
* client component overuse

Generate findings.

---

## Rendering Audit

Find:

* unnecessary re-renders
* unstable callbacks
* unstable object references
* unnecessary useEffect usage
* state duplication
* prop drilling
* context over-rendering

Apply:

* memoization where beneficial
* React.memo
* useMemo
* useCallback

Only where measurable gains exist.

Avoid premature optimization.

---

## Bundle Audit

Analyze:

* client bundles
* shared chunks
* route chunks

Find:

* oversized dependencies
* unused imports
* duplicate libraries

Apply:

* dynamic imports
* route-level code splitting
* lazy loading

Reduce bundle size wherever safe.

---

## Data Fetching Audit

Inspect:

* TanStack Query
* Server Components
* API calls
* Suspense boundaries

Improve:

* cache utilization
* request deduplication
* loading behavior
* stale data handling

Reduce unnecessary network requests.

---

## Layout Shift Audit

Measure:

* CLS risks
* image sizing issues
* async rendering shifts
* loading state shifts

Fix all avoidable layout shifts.

---

# Phase 2: Scrolling Experience Optimization

Analyze:

* page scrolling
* nested scrolling containers
* tables
* sidebars
* drawers
* modals

Detect:

* scroll jumps
* scroll resets
* scroll lock bugs
* nested scroll conflicts
* momentum issues

Apply:

### Preferred

Native browser scrolling.

### Documentation Areas

If documentation pages exist:

* optionally implement Lenis only for documentation sections

Never globally.

---

## Large Dataset Optimization

Detect tables exceeding:

* 100 rows
* 500 rows
* 1000 rows

Implement:

* TanStack Virtual
* virtualization
* windowing

Where appropriate.

Prevent scroll lag.

---

# Phase 3: UX Smoothness Optimization

Improve:

## Navigation

* route transitions
* loading transitions
* pending states

Use:

* Framer Motion
* Motion

only for subtle transitions.

Target:

100ms–250ms transitions.

Avoid flashy effects.

---

## Skeleton Loading

Replace:

* spinners
* blank screens

With:

* skeletons
* optimistic placeholders

Ensure visual stability.

---

## Interaction Responsiveness

Analyze:

* buttons
* forms
* tables
* dialogs
* dropdowns

Improve:

* hover states
* active states
* focus states

Maintain consistency.

---

# Phase 4: Symmetry & Design System Audit

Audit every page for:

## Spacing Consistency

Detect inconsistent:

* margins
* paddings
* gaps

Normalize using design tokens.

---

## Typography Consistency

Audit:

* font sizes
* font weights
* line heights

Create hierarchy.

---

## Grid Alignment

Audit:

* cards
* panels
* dashboards
* tables

Ensure:

* visual balance
* consistent alignment
* predictable spacing

---

## Component Consistency

Audit:

* buttons
* badges
* inputs
* selects
* modals
* drawers

Standardize:

* heights
* radii
* spacing
* shadows

---

## Visual Rhythm

Create consistent:

* section spacing
* vertical rhythm
* component hierarchy

Reduce visual noise.

---

# Phase 5: Accessibility

Audit:

* keyboard navigation
* focus management
* ARIA labels
* color contrast
* screen reader compatibility

Fix violations.

Target WCAG AA compliance.

---

# Phase 6: Performance Validation

Run and collect:

## Lighthouse

Measure:

* Performance
* Accessibility
* Best Practices
* SEO

---

## Core Web Vitals

Measure:

* LCP
* CLS
* INP
* FCP
* TTFB

---

## React Profiling

Identify:

* expensive renders
* slow components
* render waterfalls

Optimize where justified.

---

# Phase 7: Verification

After every modification:

1. Run type checks.
2. Run linting.
3. Run unit tests.
4. Run integration tests.
5. Run E2E tests.
6. Verify no regressions.
7. Verify no broken routes.
8. Verify no hydration issues.
9. Verify no runtime warnings.

Fix all discovered issues.

---

# Deliverables

Generate the following artifacts.

## 1. Audit Report

Include:

* identified issues
* severity
* root causes
* affected files

---

## 2. Change Report

Include:

* modified files
* changes made
* rationale

---

## 3. Performance Report

Before vs After:

| Metric | Before | After | Improvement |
| ------ | ------ | ----- | ----------- |

Include:

* Bundle Size
* LCP
* CLS
* INP
* Lighthouse Score
* Render Count

---

## 4. UX Improvement Report

Summarize:

* scrolling improvements
* responsiveness improvements
* symmetry improvements
* accessibility improvements

---

## 5. Production Readiness Report

Provide:

* remaining risks
* technical debt
* future recommendations
* scalability considerations

---

# Success Criteria

The final application should feel:

* Fast
* Stable
* Predictable
* Professional
* Symmetrical
* Consistent
* Accessible
* Operationally efficient

Prioritize usability over visual effects.

Prioritize performance over animation.

Prioritize developer productivity over aesthetics.

Do not stop after reporting issues.

Implement fixes, verify them, and produce final measurable results.

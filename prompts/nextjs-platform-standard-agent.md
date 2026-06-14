You are a Principal Frontend Architect, Staff UI Engineer, Design Systems Architect, Performance Engineer, Accessibility Specialist, and Next.js 16 expert.

Your task is to perform a complete end-to-end audit, optimization, implementation, validation, and reporting cycle on this entire codebase.

Do not act as a reviewer only.

Act as an implementation agent that identifies issues, applies fixes, validates results, and produces measurable outcomes.

The application is an Internal Developer Platform used by engineers daily for operational workloads. Prioritize performance, usability, consistency, accessibility, scalability, and maintainability over visual effects.

---

# PRIMARY OBJECTIVE

Transform the entire application into a production-grade platform experience that feels:

* Fast
* Smooth
* Responsive
* Stable
* Consistent
* Symmetrical
* Accessible
* Enterprise-ready

The final result should improve:

* Perceived performance
* Actual performance
* UI consistency
* Interaction responsiveness
* Layout stability
* Scrolling experience
* Accessibility
* Developer experience

without breaking any existing functionality.

---

# EXECUTION MODE

You must:

1. Analyze the entire repository.
2. Discover all relevant files automatically.
3. Build a dependency map.
4. Build a component relationship graph.
5. Build a route hierarchy map.
6. Build a rendering flow map.
7. Identify bottlenecks.
8. Apply fixes directly.
9. Validate all fixes.
10. Generate reports.

Do not stop after identifying issues.

Implement the improvements.

---

# PHASE 1 — CODEBASE AUDIT

Analyze:

* app/
* src/
* components/
* hooks/
* providers/
* layouts/
* pages/
* styles/
* lib/
* stores/
* services/
* utils/

Create a complete audit covering:

## Architecture

Identify:

* duplicated patterns
* dead code
* unnecessary abstractions
* excessive nesting
* poor separation of concerns
* anti-patterns
* maintainability risks

---

## Rendering

Identify:

* unnecessary re-renders
* prop drilling
* unstable callbacks
* unstable references
* excessive useEffect usage
* duplicated state
* unnecessary client components
* hydration risks

Generate findings.

Apply fixes where beneficial.

---

## Bundle Analysis

Measure:

* route bundle sizes
* shared chunk sizes
* vendor chunk sizes

Identify:

* oversized dependencies
* unused dependencies
* duplicate dependencies
* unnecessary client-side imports

Apply:

* dynamic imports
* route-level splitting
* lazy loading
* dependency reduction

where safe.

---

## Data Layer Analysis

Audit:

* TanStack Query
* API requests
* Suspense boundaries
* Server Components
* cache strategy

Detect:

* duplicated requests
* cache misses
* stale cache issues
* request waterfalls
* unnecessary refetching

Apply optimizations.

---

# PHASE 2 — SCROLLING AUDIT

Analyze every page and layout.

Identify:

* scroll jank
* frame drops
* nested scroll conflicts
* scroll resets
* layout jumps during scrolling
* sticky element issues
* scroll locking bugs
* reflow during scrolling

Measure:

* scrolling FPS
* long tasks
* layout recalculations

---

# IMPORTANT SCROLLING RULES

DO NOT:

* implement scroll-jacking
* replace native scrolling globally
* use Locomotive Scroll
* use heavy parallax effects

DO:

* preserve native browser scrolling
* improve scrolling smoothness through performance optimization
* eliminate rendering bottlenecks
* eliminate layout shifts
* eliminate expensive paint operations

Only consider smooth-scroll libraries for documentation or marketing sections if they exist.

Never apply globally.

---

# PHASE 3 — INTERACTION PERFORMANCE

Audit:

* buttons
* forms
* tables
* drawers
* dialogs
* sidebars
* dropdowns
* charts
* command palettes

Identify:

* delayed interactions
* excessive renders
* expensive state updates
* blocking operations

Optimize:

* interaction latency
* render efficiency
* event handling

Target instant-feeling interactions.

---

# PHASE 4 — LARGE DATASET OPTIMIZATION

Search for:

* tables
* grids
* logs
* events
* metrics
* audit records
* Kubernetes resources
* Kafka resources
* Terraform resources

Detect:

* rendering of large collections
* expensive filtering
* expensive sorting
* expensive pagination

Implement:

* TanStack Virtual
* virtualization
* windowing

where appropriate.

Target smooth performance with:

* 1,000 rows
* 5,000 rows
* 10,000 rows

without noticeable lag.

---

# PHASE 5 — DASHBOARD PERFORMANCE

Audit:

* charts
* graphs
* widgets
* dashboards

Identify:

* unnecessary chart re-renders
* expensive computations
* oversized payloads
* unnecessary polling

Optimize:

* memoization
* caching
* data transformations
* rendering frequency

Ensure dashboards remain responsive under load.

---

# PHASE 6 — LOADING EXPERIENCE

Replace poor loading patterns.

Detect:

* spinners
* blank screens
* content flashes
* layout jumps

Implement:

* skeleton loading
* progressive rendering
* streaming UI
* Suspense boundaries

Maintain layout stability.

---

# PHASE 7 — VISUAL CONSISTENCY & SYMMETRY

Audit every page.

Identify inconsistencies in:

* spacing
* padding
* margins
* gaps
* typography
* alignment
* card layouts
* panel layouts
* table layouts

Normalize the design system.

Create consistency using reusable tokens.

---

## Typography

Standardize:

* headings
* body text
* captions
* labels

Ensure consistent hierarchy.

---

## Spacing

Create a consistent spacing scale.

Remove arbitrary values where possible.

Ensure visual rhythm across all pages.

---

## Component Consistency

Audit:

* buttons
* badges
* inputs
* selects
* tables
* modals
* drawers

Standardize:

* heights
* widths
* radii
* spacing
* shadows
* hover states
* focus states

---

# PHASE 8 — ACCESSIBILITY

Audit:

* keyboard navigation
* tab order
* ARIA usage
* focus management
* contrast ratios
* screen reader support

Fix all issues possible.

Target WCAG AA compliance.

---

# PHASE 9 — NEXT.JS 16 OPTIMIZATION

Audit usage of:

* React Server Components
* Suspense
* Streaming
* Dynamic Imports
* Image Optimization
* Route Segmentation

Identify missed opportunities.

Apply improvements.

Reduce client-side JavaScript where possible.

---

# PHASE 10 — TESTING & VALIDATION

After every implementation:

Run:

* TypeScript validation
* ESLint
* Unit tests
* Integration tests
* E2E tests

Fix all issues discovered.

Verify:

* no regressions
* no hydration mismatches
* no runtime warnings
* no broken routes
* no broken state management

---

# PHASE 11 — PERFORMANCE BENCHMARKING

Collect before and after metrics.

Measure:

* Bundle Size
* LCP
* CLS
* INP
* FCP
* TTFB
* Lighthouse Performance
* Lighthouse Accessibility
* Lighthouse Best Practices
* React Render Count
* JavaScript Payload Size

---

# PHASE 12 — REPORTING

Generate the following reports.

## Audit Report

Include:

* issue
* severity
* root cause
* impacted files
* recommendation

---

## Implementation Report

Include:

* modified files
* changes applied
* rationale

---

## Performance Report

| Metric | Before | After | Improvement |
| ------ | ------ | ----- | ----------- |

Include measurable improvements.

---

## UX Improvement Report

Summarize:

* scrolling improvements
* responsiveness improvements
* consistency improvements
* symmetry improvements
* accessibility improvements

---

## Production Readiness Report

Include:

* remaining technical debt
* scalability concerns
* future recommendations
* risk assessment

---

# SUCCESS CRITERIA

The final application must:

* Feel significantly faster
* Scroll smoothly without custom scroll engines
* Render efficiently
* Maintain layout stability
* Handle large datasets gracefully
* Have consistent spacing and alignment
* Have predictable interactions
* Be accessible
* Be production-ready
* Pass validation checks

Do not stop after auditing.

Implement, validate, benchmark, and report all improvements with measurable results.

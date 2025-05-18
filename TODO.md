# TODO List (Prioritized)

**Instructions:**
- Complete each task in order. After each, scan the entire project (every file, byte, and feature) to ensure it works as intended. Only mark as done if fully verified. If a task cannot be completed due to errors or missing input, skip it and return later unless it is necessary to move the project forward.

---

## 1. Core Data & Persistence
- [x] Persist product/category edits from admin overlays (move from local state to backend/file/database)
- [x] Add backend or file/database for products, categories, and content
- [ ] Implement API endpoints for CRUD operations (products, categories, etc.)
- [x] **Add a 'Done' button in admin overlays that asks if you are done. If yes, saves, refreshes the server and the webpage; if no, just exits admin mode.** (Verified working)

## 2. Payment Integration
- [ ] Replace dummy payment logic in `src/lib/paymentService.ts` with real payment integration (Stripe, PayPal, Square, etc.)
- [ ] Add order confirmation email or notification after successful payment

## 3. Admin/Product Management Enhancements
- [ ] Add authentication/authorization for admin actions (beyond password gate)
- [ ] Order management/admin dashboard
- [ ] Inventory management (optional, but important for scaling)

## 4. Gallery & Content
- [ ] Implement real gallery content (currently uses static/dummy data)
- [ ] Add admin editing for gallery items

## 5. General/Missing Features
- [ ] User account system (optional, for order history, etc.)
- [ ] Error handling and user feedback for all forms
- [ ] Accessibility audit and improvements
- [ ] Responsive/mobile UI polish
- [ ] SEO improvements (meta tags, Open Graph, etc.)
- [ ] Analytics integration (optional)

---

## Need to Remember: Shop Item Availability Pattern
- All shop sections (current and future) should use the following pattern for product availability:
    - Each product has an `available` toggle in admin mode.
    - Unavailable items are shown in grayscale, show color on hover, display 'Unavailable' instead of price, and disable/hide 'Add to Cart'.
    - The price is retained in the data for future use.
    - This pattern should be applied to all new shop sections as they are added.

---

## Suggestions & Opportunities (from code review)
- [ ] Use Next.js <Image /> for all images to leverage built-in optimizations.
- [ ] Audit for ARIA roles, keyboard navigation, and color contrast to improve accessibility.
- [ ] Add unit/integration tests (e.g., Jest, React Testing Library).
- [ ] Expand README with project-specific info, setup, and contribution guidelines.
- [ ] Add user feedback for cart actions (e.g., toasts/snackbars).
- [ ] Ensure custom API routes are protected (auth, validation).
- [ ] Remove unused lock files and standardize on a single package manager.

---

(Add more project-wide TODOs below as needed) 
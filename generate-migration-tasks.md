Rule 2: Generate a Granular Task List from the Blueprint.
You must convert the high-level blueprint into a detailed, sequential, and checkable task list. This becomes the project's single source of truth for execution.
File: generate-migration-tasks.md
code
Markdown
# AI Command: Generate Migration Task List

**Objective:** Take the `Migration-Blueprint.md` as input and generate a detailed, step-by-step implementation plan.

**Source File:**
- `@Migration-Blueprint.md`

**Instructions:**
Generate a new markdown document named `Migration-Tasks.md`. The list should be hierarchical and follow this precise structure:

**1. Phase 1: Database and Data Setup**
    - [ ] 1.1. Execute the v4 Schema DDL to create the database structure.
    - [ ] 1.2. Write a data migration script (e.g., Python or SQL) to transfer and transform data from the old tables to the new v4 tables.
    - [ ] 1.3. Execute the data migration script and verify data integrity with row counts.

**2. Phase 2: View-by-View Implementation (Repeat for each view in the Blueprint)**
    - [ ] 2.1. **Implement `dashboard` View:**
        - [ ] 2.1.1. Refactor and add the `total_hospitals` data source query.
        - [ ] 2.1.2. Refactor and add the `site_details` data source query (parameterized by site type).
        - [ ] 2.1.3. Build the UI layout with containers, cards, and input filters (date, user, site type).
        - [ ] 2.1.4. Wire the `onchange` events of the filters to update view arguments and refresh data.
    - [ ] 2.2. **Implement `reports_view` View:**
        - [ ] 2.2.1. Refactor and add the `attendance_data` data source query.
        - [ ] 2.2.2. ... (continue for all components of this view)
    - [ ] 2.3. **Implement `generic_form_view` View:**
        - [ ] 2.3.1. ... (continue for all views)

**3. Phase 3: Application Orchestration & Finalization**
    - [ ] 3.1. Implement the main application shell with navigation components.
    - [ ] 3.2. Link all views together using `navigation` actions in the `onclick` events.
    - [ ] 3.3. Conduct final end-to-end testing of all user flows.

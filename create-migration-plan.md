Rule 1: Generate the Migration Blueprint.
You must create a comprehensive blueprint that clarifies what you're migrating, for what new architecture, and why the changes are being made.
File: create-migration-plan.md
code
Markdown
# AI Command: Generate Migration Blueprint

**Objective:** Analyze the provided legacy system files and the target architecture specification to produce a complete Migration Blueprint.

**Source Files:**
- `@pneumocare-fp_proxy.json`
- `@pneumocare-fp_datasource.json`
- `@pneumocare-fp_page.json`
- `@pneumocare-tasks.json`
- `@pneumocare-questions.json`

**Target Architecture:**
- A single, unified JSON structure (`@SmartJoules_Mobile_App_new_app.json`).
- A single, normalized PostgreSQL database.

**Instructions:**
Generate a markdown document named `Migration-Blueprint.md` that contains the following three sections:

**SECTION 1: V3 System Deconstruction**
1.1. **Application Flow:** List all pages and the primary navigation structure.
1.2. **Data Source Catalog:** Create a table with columns: `v3_id`, `label`, `type`, `tables_queried`, `parameters`.
1.3. **Page-Widget-Data Map:** For each page, list its widgets and the `dataSourceId` they depend on.
1.4. **Workflow Analysis:** Briefly describe the purpose of each process defined in `pneumocare-process.json` (e.g., "Add Hospital", "Distributor Visit").

**SECTION 2: Refined v4 Database Schema**
2.1. **Critique of v3 Schema:** Identify at least three major flaws in the legacy data structure (e.g., lack of normalization, inconsistent naming, poor data types).
2.2. **Proposed v4 Schema (DDL):** Provide the complete PostgreSQL DDL for the new, unified schema. This must include:
    - Standardized snake_case naming.
    - Normalized tables for entities like `sites` and `visit_feedback`.
    - Strong data types (`TIMESTAMP`, `INTEGER`, `POINT`, `ENUM`).
    - Foreign key constraints and indexes.

**SECTION 3: View Consolidation Plan**
3.1. Propose a new, consolidated view structure for the v4 app.
3.2. Create a mapping table: `v3 Page(s)` -> `v4 View ID` -> `Justification for Consolidation`.

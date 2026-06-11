# TW x Learning Product Strategy

## Ecosystem Diagram

![MOE Educator Platform Ecosystem](../../assets/moe-educator-platform-ecosystem.svg)

The diagram above shows how the MOE educator platform ecosystem fits together — from the identity and data infrastructure layer, through the learning products, down to the two key surfaces: **Teacher's Workspace (TW)** and the **Professional Learning Space (PLS)**.

---

## Glow Strategy

### What Worked

- **AI microlearning format resonated** — Bites and job aids proved useful for just-in-time, contextual consumption
- **Content creation tooling** — The Glow Content Creator reduced production friction for curators and made it feasible for more teams to produce content
- **Standalone discovery** — Educators could find and consume Glow content independently without needing to go through the LMS
- **nLDS event logging** — Glow activity is being captured in the nLDS Data Warehouse, creating a foundation for learning analytics

### What Did Not Work

- **Fragmented entry points** — Glow sits standalone today; educators must context-switch between TW and Glow rather than encountering learning content in their natural workflow
- **No signal loop** — Content recommendations are not informed by what is actually happening in classrooms (student data, lesson context, teacher workload signals)
- **Cold-start discoverability** — Without contextual triggering, surfacing the right Glow bite to the right teacher at the right moment has been largely manual
- **LMS–Glow duplication risk** — With LMS (Sana / nLDS) and Glow operating independently, there is a risk of overlapping content libraries and unclear ownership

### Future Plans

- **Integrate Glow content into TW via CI** — Modular content (LMS courses + Glow bites) will be surfaced in-context by Contextual Intelligence, removing the need for deliberate navigation
- **Unified content layer** — Move toward a single modular content library accessible from both TW and the Professional Learning Space
- **Signal-driven personalisation** — Use Honeyjar data (teacher signals within TW) to drive relevant Glow content recommendations through the CI pipeline
- **PLS integration (envisioned)** — Glow bites will appear alongside LMS courses in the Professional Learning Space to support structured professional development pathways

---

## CI Strategy

### Capabilities Layer for TW

Contextual Intelligence (CI) is the core intelligence layer inside Teacher's Workspace. It operates as a **Signal → Match → Surface** pipeline:

| Stage | What it does |
|-------|-------------|
| **Signal** | Ingests contextual data from Honeyjar (interim TW data store) — lesson plans, student insights, workflow state, calendar context |
| **Match** | Matches signals against the modular content library and relevant resources |
| **Surface** | Proactively surfaces the right content, insight, or action in the teacher's current workflow — without requiring a search |

CI is what transforms TW from a productivity tool into an **intelligent assistant** — the difference between a teacher having to look for help versus help finding the teacher.

**Key design principles:**
- CI does not replace teacher judgement; it reduces the cognitive load of knowing where to look
- Relevance is contextual, not just interest-based — signals come from live classroom and workflow data, not just a user profile
- The surface layer is embedded in existing TW workflows, not a separate "recommendations" tab

### Use Cases

| Use case | Signal | Content surfaced |
|----------|--------|-----------------|
| **Lesson prep** | Teacher opens a lesson plan for a specific topic | Relevant Glow bites, LMS modules, or curated resources matched to topic and level |
| **Student struggles** | Student insights flag a cohort dipping in a subject area | Targeted intervention resources, peer teaching approaches, or PD content on differentiated instruction |
| **After COVAA feedback** | Lesson observation logged in PLS | CI surfaces PD content matched to the specific competency flagged in feedback |
| **Workflow nudge** | Teacher has not completed a recurring admin task | Relevant workflow template or checklist surfaced at the right moment |
| **New educator onboarding** | Low experience signal from profile + school context | Curated learning pathway of foundational Glow bites and LMS modules |
| **PD planning** | Teacher or HOD opens the PD planning workflow | CI suggests relevant LMS courses aligned to school goals and individual growth areas |


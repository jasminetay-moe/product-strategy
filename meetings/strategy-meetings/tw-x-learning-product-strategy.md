# TW x Learning Product Strategy

## Ecosystem Diagram

![MOE Educator Platform Ecosystem](../../assets/moe-educator-platform-ecosystem.svg)

The diagram above shows how the MOE educator platform ecosystem fits together — from the identity and data infrastructure layer, through the learning products, down to the two key surfaces: **Teacher's Workspace (TW)** and the **Professional Learning Space (PLS)**.

---

## Glow Strategy

### What Worked

- Organic engagement rates are higher than the existing LMS (OPAL2.0), proving receptivity towards the concept of an AI-enabled microlearning format.

### What Didn't Work

- **Fragmented positioning across the learning vertical** — confusing for teachers to know when to go to which platform (between OPAL2.0 and Glow).
- **Cold-start discoverability** — without contextual triggering, the right content rarely found the right teacher at the right moment.
- **Content supply** — insufficient volume and coverage of quality content to sustain engagement and meet diverse teacher needs.

### Future Plans

- Use the Glow content modality as the foundation for a future modular content approach.
- Integrate modular content with TW/CI, which introduces signal-driven discoverability and solves the fragmentation problem by surfacing learning in the context of teachers' daily workflow.

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


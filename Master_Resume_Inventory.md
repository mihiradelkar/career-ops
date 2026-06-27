# Master Resume — Bullet & Metric Inventory

**Source:** all 220 resume PDFs in the project folder, text extracted and parsed (3,610 bullet instances).
**Baseline of truth:** `Mihir_Adelkar_SWE.pdf` (your designated master) + your verified corrections.
**How to read frequency:** "(NN files)" = how many of the 220 variants carry that claim. High frequency = battle-tested phrasing, low frequency = appears rarely (scrutinize for drift or inflation). **You decide what's canonical** — nothing here is auto-merged.

---

## ⚠️ DECISION POINTS — resolve these first

These are the claims where files disagree with each other or with your verified truth. A naive merge would launder the wrong number into your source of truth.

| # | Claim | What the files say | Verified / master | Action needed |
|---|-------|--------------------|-------------------|---------------|
| 1 | **Wasalt registered users** | `500K+` in **all** files that cite it | You corrected this to **750K+** | Decide canonical → almost certainly **750K+**; then fix everywhere |
| 2 | **"500K+ users" reuse** | Pasted onto unrelated bullets ("enterprise apps," "5+ full-stack apps," "Java/Spring apps serving 500K+ users") | The figure belongs to **Wasalt only** | Strip from non-Wasalt bullets — generic reuse is indefensible in interview |
| 3 | **"1B+ messages/day" (Kafka)** | In **28 files**, attached to many different contexts | **Not in your master at all** | **Biggest inflation risk.** Verify it's real for *one specific* system, or drop it |
| 4 | **$30K hardware savings** | `$30K` in 8 SRE/DevOps variants (Cisco, Clay_BE, SRE, SRE_2, Devops2, Google_SRE) | Not in master | Keep only if defensible; it's consistent ($30K) but unverified here |
| 5 | **10,000 concurrent users (Wasalt load test)** | 1 file (Wasalt enterprise variant) | Not in master | Singleton — verify or drop |
| 6 | **Infra cost reduction (Wasalt)** | `45%+` (13 files, matches master) vs `40%` drift in a few | Master = **45%+** | Lock to **45%+** |

---

## EXPERIENCE

### KeelWorks Foundation — Full-Stack Developer (Aug 2025–Present)
**Canonical bullets are metric-free in the master and most variants — keep it that way unless a number is genuinely defensible.**
- Own end-to-end development of **KeelCompass**, internal workforce engagement forum; React UI + Node/PostgreSQL microservices, partnering with PM and design *(consistent across files)*
- Automated end-to-end deployment pipeline (GitHub Actions on AWS EKS), unblocking same-day deploys
- Delivered reusable component library + coding standards adopted across the team

⚠️ A few aggressive variants attach metrics to KeelWorks (daily-user counts, "$900K annually," "95% accuracy"). These do **not** appear in the master and look inflated for an internal forum — **recommend excluding** unless you can defend each one.

### Freelancing (Dabadu.ai / XRM) — Software Engineer (May–Sep 2023)
- Resolved production defects across XRM automotive dealership CRM; restored reliable deployments *(consistent)*
- Refactored legacy JavaScript → TypeScript, introduced SonarCloud quality gates, **reducing production bugs 20%** *(77 files — well-established)*

### NeoSOFT Technologies — Software Engineer (Jun 2021–May 2023)
*This is where the densest accomplishments and the most metric drift live. Grouped by underlying project:*

**Wasalt — real-estate CRM migration** *(your flagship distributed-systems story)*
- Audited real-estate CRM (**400–500ms avg, 2s spikes**); designed full architecture + migration plan
- Built pre-configured gRPC/Kafka microservices boilerplate
- Coordinated **20+ engineers** (13 files) over **6 months** (11 files) — **12 services migrated** (12 files), **7x faster inter-service calls** (10 files), **45%+ infra cost reduction** via AWS rightsizing (13 files)
- ⚠️ User count: see Decision Point #1 (**750K+**, not 500K+)

**mf-shell / Console — open-source boilerplates**
- Built mf-shell (Webpack Module Federation micro-frontend composition) + Console (multi-tenant admin, RBAC)
- Adopted as org-wide scaffolding by **15+ internal teams** (52 files); **50+ roles** via RBAC (32 files)

**Nesto — Homepage Builder CMS + multi-tenant CRM**
- React + Node.js + AWS Lambda; enabled marketing to self-serve page/promotion updates *(consistent, low metric density)*

**CI/CD + observability**
- New Relic APM dual dashboards (eng metrics + stakeholder health), **cutting MTTR 25 → 15 min** (67 files — very well-established)

**Classroom analytics (Django)**
- Django analytics engine aggregating per-student data, Next.js dashboard for live attendance/quiz/engagement

**GraphQL/REST APIs + caching**
- GraphQL/REST with PostgreSQL + Redis caching serving users, **cutting response times 70%** (64 files) / **sub-100ms** (64 files); **85% test coverage** via Jest/Cypress (52 files)

**Mentoring**
- Mentored **8 junior developers** (113 files — your single most-repeated claim); bi-weekly knowledge-sharing seminars

---

## RECENT PROJECTS

### Healthcare Prior Authorization AI
- Replaced **3–5 day** manual reviews (45 files) with **5–10 sec** automated decisions
- Clinical NLP → FHIR R4 mapping at **95%+ extraction accuracy on test dataset** (46 files)
- MCP architecture for context-aware LLM reasoning; confidence scores + audit trails
- *Stack: Python, FastAPI, Claude API, FHIR R4, MCP, Pinecone, Streamlit*

### CVE Intelligence System
- Distributed microservices for real-time CVE ingestion (Kafka streaming)
- RAG pipeline (Pinecone + Llama 3) for plain-English vulnerability queries
- AWS EKS + Terraform IaC + Istio service mesh; Prometheus/Grafana + Jenkins CI/CD
- *Stack: Go, Node.js, Kafka, Pinecone, Llama 3, AWS EKS, Terraform, Istio*

### AdsGency AI (current bridge role — appears in only a few recent variants)
- LangGraph-based YouTube ad generation workflow; SSE replacing HTTP polling; parallel multi-image generation; Celery/Redis async queues; Google Ads API integration
- ⚠️ Underrepresented across the 220 files (most predate this role). If AdsGency should be on the master as current employment, it needs proper bullets built from verified work — not mined from the old variants.

---

## RARE / SINGLETON CLAIMS TO SCRUTINIZE
Claims appearing in only 1–2 files — most are JD-specific stretches, not core truth:
- "10,000 concurrent users" load test (1 file)
- "$900K annually" / KeelWorks daily-user metrics (1–2 files)
- "1B+ daily requests with 99.9% uptime" (Apple_FS variant)
- Assorted "5+ full-stack applications," "Architected cloud-native data applications serving 500K+ users" — generic scale claims with the borrowed 500K figure

**Rule of thumb:** if a metric lives in ≤2 of 220 files and isn't in the master, it was invented for one application. Default to excluding from the master.

---

## RECOMMENDED CANONICAL SET (for your sign-off)
The high-frequency, master-aligned numbers — safe to treat as your source of truth once you confirm:
`Wasalt 750K+ users` · `400–500ms→ baseline, 2s spikes` · `20+ engineers` · `6 months` · `12 services` · `7x inter-service` · `45%+ infra cost` · `MTTR 25→15 min` · `response time −70% / sub-100ms` · `85% test coverage` · `15+ teams (mf-shell)` · `50+ roles (RBAC)` · `bugs −20% (Dabadu)` · `8 junior devs mentored` · `prior-auth 3–5 day→5–10 sec, 95%+ accuracy`

**Drop or verify before including:** `1B+ messages/day` · `$30K savings` · `10,000 concurrent` · any KeelWorks metric.

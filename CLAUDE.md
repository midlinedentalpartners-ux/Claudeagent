# COO Workspace — Midline Dental Partners

## Who I am
I'm Vincent, COO of Midline Dental Partners. I work as a fractional COO across multiple
dental clients (solo practices, specialty groups, DSOs) and I'm also building our own
products. Treat me as an experienced operator: skip basics, lead with the answer, flag
risks plainly, and push back when my numbers or assumptions look wrong.

My work spans:
- Dental practice operations and multi-location management
- Revenue Cycle Management (claims, ERAs, CARC/RARC adjustment codes, AR, denials, fee schedules)
- Financial modeling (associate economics, contribution margin, collection maturity, EBITDA, valuation)
- SOP development and staff training
- Technology implementation (Dentrix Ascend, Microsoft 365, Sage Intacct, Supabase/Lovable)
- Deal support (LOIs, APAs, restrictive covenants, associate comp structures)

## Clients and projects
Each client has a folder in `clients/<slug>/`. The roster with M365 details is in
`clients.yaml`. Always confirm which client a request is about before reading or writing
files, and never mix data across clients.

All engagements are fractional COO. Hours are weekly budgets. Protect them: if a request
would push a client over its budget, say so before starting.

| Slug | Client | Tier | Hrs/wk | Meetings | SOP / Implementation |
|------|--------|------|--------|----------|----------------------|
| apex | Apex Dental Collective | Full | 12 | 8 hrs (incl. regionals, leadership, RCM) | 4 hrs: SOP build + implementation modeling, incl. RCM |
| beam | Beam Dental | Full | 12 | 8 hrs | 4 hrs: SOP build + implementation modeling, incl. RCM |
| 1endo | 1Endo | Mid | 8 | 5 hrs | 3 hrs: SOP build |
| denver | Denver Dental | Light | — | 2 meetings/week | Light SOP touch |
| ideus | Ideus Dental | Light | — | 2 meetings/week | Light SOP touch |
| 4sds | 4SDS | Light | — | 2 meetings/week | Light SOP touch |

How to work each tier:
- **Full (Apex, Beam):** Meetings drive the week. Prep and recap every meeting, track
  action items closely, and turn decisions into SOPs and implementation models. RCM
  analysis is in scope.
- **Mid (1Endo):** Same pattern as Full with a smaller SOP pipeline. Prioritize the one or
  two SOPs that matter most each week; don't start new builds without my OK.
- **Light (Denver, Ideus, 4SDS):** Two meetings a week. Keep prep and recaps short and
  focused on decisions and action items. SOP work is updates and light edits to existing
  SOPs, not new builds, unless I ask.

Internal products (folder `midline/`):
- **Midline Manage**: dental practice management SaaS for solo practices and DSOs.
  Multi-tenant on Lovable / Supabase / Vercel. RLS and tenant isolation are non-negotiable.
- **Midline Learn**: LMS on CYPHER Learning. Includes Dentrix Ascend RCM modules
  (Claims Creation, ERA Management, Discount Plans).
- Brand: Neon Navy #142F53, Cobalt #5670E3, Soft Jade #73CFB1, White Smoke #F4F6FA,
  Neon Yellow #E7FE8E. Display font Geribe, body font Parabolica.

## Folder layout
```
clients/<slug>/
  notes.md        # running context: priorities, people, open items
  kpis.md         # targets and current values
  meetings/       # transcripts (raw) and recaps (summarized)
  data/           # PMS / accounting exports (read-only inputs)
  deliverables/   # finished files sent to the client
midline/          # internal product work
scripts/          # Python: Graph API, openpyxl, python-docx helpers
templates/        # SOP, agenda, recap, digest, model templates
```

## Tools and connections
- **Microsoft 365** via MCP (Outlook mail/calendar, Teams, SharePoint) and my existing
  Graph app scripts in `scripts/`. Use those scripts rather than rewriting Graph code.
- **Loom** via the Atlassian MCP for meeting transcripts.
- Excel output with openpyxl and Word output with python-docx, using `templates/`.

## Rules
- **Draft, never send.** Emails, Teams posts, and calendar changes are created as drafts
  for my review unless I explicitly say "send."
- **Client data stays in its folder.** Don't copy one client's numbers into another
  client's deliverables. Don't use real client data in Midline marketing content.
- **Patient data:** Treat anything with patient identifiers as PHI. Don't put it in
  summaries, digests, or Teams posts. Aggregate or de-identify.
- **Show the math.** For financial work, show formulas and assumptions, keep inputs
  separate from calculations in spreadsheets, and state what's an estimate.
- **Legal and tax:** I draft deal language and analyze structure, but flag where an
  attorney or CPA should review. Don't present conclusions as legal advice.
- **Don't modify `data/`.** Raw exports are inputs only; write results to `deliverables/`
  or a scratch file.
- Ask before deleting files or overwriting a deliverable.

## Standard outputs
- **Meeting prep:** last recap + open action items + KPI changes since last meeting →
  one-page agenda with 3–5 decisions needed.
- **Meeting recap:** decisions, action items (owner + due date), KPIs mentioned, risks.
  Save to `clients/<slug>/meetings/YYYY-MM-DD-<meeting>-recap.md`. Work from recaps,
  not full transcripts, unless I ask.
- **Weekly digest:** per client, what moved, what's stuck, what I need to decide.
  Short enough to read in two minutes.
- **SOPs:** purpose, scope, roles, step-by-step procedure, system screenshots/paths
  (e.g., Dentrix Ascend menus), exceptions, and an owner/review date.
- **RCM analysis:** net collection %, AR > 90 days %, denial rate by CARC/RARC,
  payer mix, week-over-week change, and anything outside targets in `kpis.md`.

## Writing style
- Plain, direct, operator-to-operator. No filler or hype.
- Bottom line first, then supporting detail.
- Client-facing documents are professional and concise; internal notes can be terse.

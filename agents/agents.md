# Agent List

| Agent | Status | Runtime | Owner | Summary |
|-------|--------|---------|-------|---------|
| [Midline AI](#midline-ai) | Live | Supabase edge function `midline-agent` | TBD | Conversational assistant that answers org data questions and proposes (never executes) writes. |

---

## Midline AI

- **Slug:** `midline-agent`
- **Status:** Live
- **Source:** [`supabase/functions/midline-agent/index.ts`](https://github.com/midlinedentalpartners-ux/insight-hub/blob/main/supabase/functions/midline-agent/index.ts)
- **UI entry point:** [`src/components/ai/AIAssistant.tsx`](https://github.com/midlinedentalpartners-ux/insight-hub/blob/main/src/components/ai/AIAssistant.tsx)
- **Model:** `google/gemini-3-flash-preview`
- **Data tables:** `agent_conversations`, `agent_messages`, `agent_suggested_actions`
- **Rate limit:** 20 requests / 60s per user
- **Tools:**
  - `query_providers`: list providers, filterable by role or location
  - `query_locations`: list org locations
  - `query_forecast`: forecast actuals (production + collection)
  - `query_training_compliance`: training compliance status
  - `query_financial_kpis`: financial KPIs
  - `search_sops`: search SOPs
  - `search_documents`: search documents
  - `suggest_action`: propose a write for the user to confirm
- **Guardrails:** read-only tools, scoped to the current user's organization; every write goes through a user-confirmed suggested action.
- **Owner:** TBD
- **Notes:** —

---

## Template

```md
## <Agent name>

- **Slug:** `<agent-slug>`
- **Status:** Idea | In development | Live | Retired
- **Source:** <path or link>
- **UI entry point:** <path or N/A>
- **Model:** <model id>
- **Data tables:** <tables or N/A>
- **Rate limit:** <limit or N/A>
- **Tools:**
  - `<tool_name>`: <what it does>
- **Guardrails:** <what it can and cannot do>
- **Owner:** <name>
- **Notes:** <anything else>
```

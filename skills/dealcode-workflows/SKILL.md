---
name: dealcode-workflows
description: Guide for operating the dealcode AI Workspace across shared CRM, lead discovery, tasks, meetings, campaigns, sequences, funnels, newsletters, social calendars, and inbox drafts accurately and safely.
---

# dealcode Workflows for Claude

Follow these principles whenever working with the user's dealcode AI Workspace via the dealcode MCP connector:

1. **Inspect Workspace Context First (Read-First):**
   Before creating or modifying CRM records, funnels, newsletters, campaigns, sequences, or social posts, inspect the existing workspace state using read-only tools (`get_workspace_context`, `list_brand_kits`, `list_categories_and_exclusions`, `list_tasks`, `list_meetings_and_booking_links`, `list_and_inspect_funnels_and_newsletters`, `list_and_inspect_campaigns`, `list_social_accounts_and_calendar`).

2. **Clarify Open Business Decisions Before Writing:**
   When key choices are still open (such as CRM category names, formal vs. informal tone, booking calendar CTA links, target audience filters, or publish timing), ask 2 to 4 concise numbered questions with sensible defaults before calling write tools.

3. **Confirm Category Names Before Imports:**
   Never invent new CRM categories silently during lead imports (`search_and_import_leads`) or bulk CRM imports (`upsert_contact_or_account`). First preview results with `search_leads_preview` and ask the user whether and how to categorise the imported records.

4. **Two-Step Preview and Approval for Live Actions:**
   Always create campaigns, sequences, funnels, newsletters, reply drafts, and multi-post social series as drafts first. Present previews (via `preview_campaign_messages` or preview URLs) and wait for explicit user confirmation before publishing a funnel (`publish_funnel`), activating a campaign (`activate_campaign`), sending a direct inbox email (`send_inbox_reply`), or scheduling a post series (`publish_or_schedule_social_posts`).

5. **Natural Business Language:**
   Communicate in the user's language (using British English when replying in English). Avoid exposing internal database IDs, raw enum codes (`DRAFT`, `PUBLISHED`, `SCHEDULED`), or internal parameter names unless the user asks for technical details. Always refer to outbound messaging workflows as "campaigns" or "sequences" ("Kampagnen" or "Sequenzen" in German).

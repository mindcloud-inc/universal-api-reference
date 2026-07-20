# <img src="https://images.mindcloud.co/apps/icons/images-7_1774905344872.png" alt="Myphoner logo" width="28" height="28"> Myphoner: Universal API

Manage Myphoner lists, leads, calls, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/myphoner/latest
- **Category:** Support / Contact Center
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.myphoner.com
- **Vendor API docs:** https://www.myphoner.com/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/myphoner/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Information](actions/get-call-information.md) | GET | Retrieves details for a call from Myphoner. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [List Columns for List](actions/list-columns-for-list.md) | GET | Retrieves column information for a list in Myphoner. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Archive Lead](actions/archive-lead.md) | PUT | Archives an existing lead in Myphoner. |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in a Myphoner list. |
| [Delegate Lead](actions/delegate-lead.md) | PUT | Delegates or claims a lead in Myphoner. |
| [Find Leads](actions/find-leads.md) | GET | Finds leads in Myphoner by field values. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves details for a lead from Myphoner. |
| [List Leads in List](actions/list-leads-in-list.md) | GET | Retrieves leads from a list in Myphoner. |
| [Mark Lead as Loser](actions/mark-lead-as-loser.md) | PUT | Marks a lead as a loser in Myphoner. |
| [Mark Lead as Winner](actions/mark-lead-as-winner.md) | PUT | Marks a lead as a winner in Myphoner. |
| [Mark Lead for Call Back](actions/mark-lead-for-call-back.md) | PUT | Marks a lead for call back in Myphoner. |
| [Migrate Lead](actions/migrate-lead.md) | PUT | Moves a lead to another list in Myphoner. |
| [Search Leads](actions/search-leads.md) | GET | Searches for leads in Myphoner by query. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Myphoner. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in Myphoner. |
| [Get List](actions/get-list.md) | GET | Retrieves details for a list from Myphoner. |
| [List Lists](actions/list-lists.md) | GET | Retrieves all existing lists from Myphoner. |

### List Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get List Statistics](actions/get-list-statistics.md) | GET | Retrieves lead statistics for a list in Myphoner. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook subscription from Myphoner. |


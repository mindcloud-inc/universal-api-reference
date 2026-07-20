# <img src="https://images.mindcloud.co/apps/icons/vector-1_1780950801090.png" alt="BoardCRM logo" width="28" height="28"> BoardCRM: Universal API

Manage deals, leads, and customer contacts in BoardCRM

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/boardCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://boardcrm.io
- **Vendor API docs:** https://dev.boardcrm.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Deal Fields](actions/list-deal-fields.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boardCRM/latest/actions/list-deal-fields?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in BoardCRM. |
| [Create Deals Batch](actions/create-deals-batch.md) | POST | Creates multiple deal records in BoardCRM. |
| [Delete Deal](actions/delete-deal.md) | DELETE | Deletes an existing deal from BoardCRM. |
| [Delete Deals Batch](actions/delete-deals-batch.md) | DELETE | Deletes multiple deal records from BoardCRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a single deal from BoardCRM. |
| [Set Deal Field Values](actions/set-deal-field-values.md) | PUT | Updates field values for a deal in BoardCRM. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in BoardCRM. |

### Deal Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal Comment](actions/create-deal-comment.md) | POST | Creates a new comment for a deal in BoardCRM. |

### Deal Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Deals](actions/export-deals.md) | GET | Exports deal records from the BoardCRM workspace. |

### Deal Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal Field](actions/create-deal-field.md) | POST | Creates a new deal field in BoardCRM. |
| [Delete Deal Field](actions/delete-deal-field.md) | DELETE | Deletes an existing deal field from BoardCRM. |
| [List Deal Fields](actions/list-deal-fields.md) | GET | Retrieves custom deal fields from BoardCRM. |
| [Update Deal Field](actions/update-deal-field.md) | PUT | Updates an existing deal field in BoardCRM. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from BoardCRM. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a single lead from BoardCRM. |
| [List Leads](actions/list-leads.md) | GET | Retrieves lead records from the BoardCRM workspace. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in BoardCRM. |

### Lead Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Leads](actions/export-leads.md) | GET | Exports lead records from the BoardCRM workspace. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Change Deal Column](actions/change-deal-column.md) | PUT | Moves deals between columns in BoardCRM. |


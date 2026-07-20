# <img src="https://images.mindcloud.co/apps/icons/stacker-icon_1777045032630.png" alt="Stacker logo" width="28" height="28"> Stacker: Universal API

Manage Stacker accounts, stacks, objects, fields, and records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/stacker/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://stackerhq.com
- **Vendor API docs:** https://docs.stackerhq.com/stacker/ai-and-automations/open-api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stacker/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Stacker. |

### Action Button

| Action | Method | Description |
| --- | --- | --- |
| [List Action Buttons](actions/list-action-buttons.md) | GET | Retrieves action buttons for a Stacker object. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields for a Stacker object. |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [List Objects](actions/list-objects.md) | GET | Retrieves objects from Stacker. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Create and Update Records](actions/bulk-create-and-update-records.md) | PUT | Creates or updates records in a Stacker object. |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a Stacker object. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from a Stacker object. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a Stacker object. |
| [Search Records](actions/search-records.md) | GET | Finds records in a Stacker object. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a Stacker object. |

### Stack

| Action | Method | Description |
| --- | --- | --- |
| [List Stacks](actions/list-stacks.md) | GET | Retrieves stacks from Stacker. |


# <img src="https://images.mindcloud.co/apps/icons/attio_1773087038316.png" alt="Attio logo" width="28" height="28"> Attio: Universal API

Manage records, lists, notes, tasks, and meetings in Attio

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/attio/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://attio.com
- **Vendor API docs:** https://docs.attio.com/rest-api/endpoint-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Objects](actions/list-objects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-objects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### List

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Attio. |
| [List All Lists](actions/list-all-lists.md) | GET | Retrieves lists from Attio. |

### List Entry

| Action | Method | Description |
| --- | --- | --- |
| [Assert List Entry by Parent](actions/assert-list-entry-by-parent.md) | PUT | Creates or updates a list entry in Attio by parent record. |
| [Create Entry](actions/create-entry.md) | POST | Creates a list entry in Attio. |
| [Delete List Entry](actions/delete-list-entry.md) | DELETE | Deletes a list entry from Attio. |
| [Get List Entry](actions/get-list-entry.md) | GET | Retrieves a list entry from Attio. |
| [List Entries](actions/list-entries.md) | GET | Retrieves list entries from Attio. |
| [Update List Entry](actions/update-list-entry.md) | PUT | Updates a list entry in Attio. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a note in Attio. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Attio. |

### Object

| Action | Method | Description |
| --- | --- | --- |
| [Get Object](actions/get-object.md) | GET | Retrieves an object from Attio. |
| [List Objects](actions/list-objects.md) | GET | Retrieves objects from Attio. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Assert Record](actions/assert-record.md) | PUT | Creates or updates a record in Attio by matching attribute. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from Attio. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from Attio. |
| [List Records](actions/list-records.md) | GET | Retrieves records from Attio. |
| [Search Records](actions/search-records.md) | GET | Finds records in Attio by fuzzy search. |
| [Update Record](actions/update-record.md) | PUT | Updates a record in Attio. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a task in Attio. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Attio. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Attio. |
| [Update Task](actions/update-task.md) | PUT | Updates a task in Attio. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Attio. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Attio. |


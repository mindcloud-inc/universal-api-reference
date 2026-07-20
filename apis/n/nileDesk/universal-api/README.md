# <img src="https://images.mindcloud.co/apps/icons/favicon_1775594435001.png" alt="NileDesk logo" width="28" height="28"> NileDesk: Universal API

No-code BPM platform for process flows, boards, datasets, data forms, and API-driven workflow integrations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nileDesk/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.niledesk.com/
- **Vendor API docs:** https://niledesk.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Templates](actions/list-templates.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nileDesk/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Board Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Board Item](actions/create-board-item.md) | POST | Creates a live board item in NileDesk. |
| [Create Draft Board Item](actions/create-draft-board-item.md) | POST | Creates a draft board item in NileDesk. |
| [Move Board Item To Step](actions/move-board-item-to-step.md) | PUT | Moves a board item to another step in NileDesk. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Template Fields](actions/list-template-fields.md) | GET | Retrieves fields for a NileDesk template. |

### Process Item

| Action | Method | Description |
| --- | --- | --- |
| [Approve Item](actions/approve-item.md) | PUT | Approves a process item in NileDesk. |
| [Create Draft Process Flow Item](actions/create-draft-process-flow-item.md) | POST | Creates a draft process flow item in NileDesk. |
| [Create Process Flow Item](actions/create-process-flow-item.md) | POST | Creates a live process flow item in NileDesk. |
| [Reject Item](actions/reject-item.md) | PUT | Rejects a process item in NileDesk. |
| [Return Item To Last Executed Step](actions/return-item-to-last-executed-step.md) | PUT | Returns an item to the last executed step in NileDesk. |
| [Send Process Item Forward](actions/send-process-item-forward.md) | PUT | Sends a process item forward in NileDesk. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Record](actions/add-record.md) | POST | Creates a new record in NileDesk. |
| [Count Records](actions/count-records.md) | GET | Counts matching records in NileDesk by filters. |
| [Delete Many Records](actions/delete-many-records.md) | DELETE | Deletes multiple matched records from NileDesk. |
| [Delete One Record](actions/delete-one-record.md) | DELETE | Deletes a single record from NileDesk. |
| [Find Many Records](actions/find-many-records.md) | GET | Finds multiple records in NileDesk by filters. |
| [Find One Record](actions/find-one-record.md) | GET | Finds one record in NileDesk by filters. |
| [Update Many Records](actions/update-many-records.md) | PUT | Updates multiple matched records in NileDesk. |
| [Update One Record](actions/update-one-record.md) | PUT | Updates a single record in NileDesk. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves API-enabled templates from the NileDesk workspace. |

### Timeline Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Process Timeline](actions/get-process-timeline.md) | GET | Retrieves a process or board item timeline in NileDesk. |


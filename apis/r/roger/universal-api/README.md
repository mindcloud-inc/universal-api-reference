# <img src="https://images.mindcloud.co/apps/icons/roger_1775660154267.png" alt="Roger logo" width="28" height="28"> Roger: Universal API

Manage contacts, organizations, tasks, tags, lists, and webhooks in RogerRoger

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/roger/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rogerroger.io
- **Vendor API docs:** https://developer.rogerroger.io

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List People](actions/list-people.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roger/latest/actions/list-people?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | POST |  |
| [Delete Organization](actions/delete-organization.md) | DELETE |  |
| [Get Organization](actions/get-organization.md) | GET |  |
| [List Organizations](actions/list-organizations.md) | GET |  |
| [Update Organization](actions/update-organization.md) | PUT |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Delete Person](actions/delete-person.md) | DELETE |  |
| [Get Person](actions/get-person.md) | GET |  |
| [List People](actions/list-people.md) | GET |  |
| [Update Person](actions/update-person.md) | PUT |  |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Create Segment](actions/create-segment.md) | POST |  |
| [Delete Segment](actions/delete-segment.md) | DELETE |  |
| [Get Segment](actions/get-segment.md) | GET |  |
| [List Segments](actions/list-segments.md) | GET |  |
| [Update Segment](actions/update-segment.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |


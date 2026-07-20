# <img src="https://images.mindcloud.co/apps/icons/less-annoying-crm_1773749371728.png" alt="Less Annoying CRM logo" width="28" height="28"> Less Annoying CRM: Universal API

Manage contacts, notes, tasks, events, and pipelines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lessAnnoyingCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lessannoyingcrm.com/
- **Vendor API docs:** https://account.lessannoyingcrm.com/api_docs/v2/Getting_Started/Introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User](actions/get-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessAnnoyingCRM/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars](actions/list-calendars.md) | GET |  |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [Search Contacts](actions/search-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Deals

| Action | Method | Description |
| --- | --- | --- |
| [Create Pipeline Item](actions/create-pipeline-item.md) | POST |  |
| [Get Pipeline Item](actions/get-pipeline-item.md) | GET |  |
| [List Pipeline Items](actions/list-pipeline-items.md) | GET |  |
| [Update Pipeline Item](actions/update-pipeline-item.md) | PUT |  |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | POST |  |
| [Get Event](actions/get-event.md) | GET |  |
| [List Events](actions/list-events.md) | GET |  |
| [Update Event](actions/update-event.md) | PUT |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Pipelines

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Pipeline Statuses](actions/list-pipeline-statuses.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |


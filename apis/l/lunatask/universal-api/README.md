# <img src="https://images.mindcloud.co/apps/icons/lunatask_1773948979700.png" alt="Lunatask logo" width="28" height="28"> Lunatask: Universal API

Manage tasks, notes, habits, journals, and relationships

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lunatask/latest
- **Category:** Productivity / Project Management
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lunatask.app
- **Vendor API docs:** https://lunatask.app/api/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping](actions/ping.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunatask/latest/actions/ping?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Habit Activity

| Action | Method | Description |
| --- | --- | --- |
| [Track Habit Activity](actions/track-habit-activity.md) | POST |  |

### Journal Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Journal Entry](actions/create-journal-entry.md) | POST |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Delete Note](actions/delete-note.md) | DELETE |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Create Person](actions/create-person.md) | POST |  |
| [Delete Person](actions/delete-person.md) | DELETE |  |
| [List People](actions/list-people.md) | GET |  |
| [Retrieve Person](actions/retrieve-person.md) | GET |  |

### Person Timeline Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Person Timeline Note](actions/create-person-timeline-note.md) | POST |  |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping](actions/ping.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Retrieve Task](actions/retrieve-task.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |


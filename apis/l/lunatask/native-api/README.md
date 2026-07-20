# Lunatask: Native API Reference

A consolidated summary of Lunatask's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://lunatask.app/api/overview
- **API base URL:** `https://api.lunatask.app/v1`

## Authentication

### Access Token

Use a Lunatask access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://lunatask.app/api/authentication)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Journal Entry](actions/create-journal-entry.md) | `POST /journal_entries` | [docs](https://lunatask.app/api/journal-api/create) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://lunatask.app/api/notes-api/create) |
| [Create Person](actions/create-person.md) | `POST /people` | [docs](https://lunatask.app/api/people-api/create) |
| [Create Person Timeline Note](actions/create-person-timeline-note.md) | `POST /person_timeline_notes` | [docs](https://lunatask.app/api/person-timeline-notes-api/create) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://lunatask.app/api/tasks-api/create) |
| [Delete Note](actions/delete-note.md) | `DELETE /notes/:id` | [docs](https://lunatask.app/api/notes-api/delete) |
| [Delete Person](actions/delete-person.md) | `DELETE /people/:id` | [docs](https://lunatask.app/api/people-api/delete) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://lunatask.app/api/tasks-api/delete) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://lunatask.app/api/notes-api/list) |
| [List People](actions/list-people.md) | `GET /people` | [docs](https://lunatask.app/api/people-api/list) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://lunatask.app/api/tasks-api/list) |
| [Ping](actions/ping.md) | `GET /ping` | [docs](https://lunatask.app/api/authentication) |
| [Retrieve Person](actions/retrieve-person.md) | `GET /people/:id` | [docs](https://lunatask.app/api/people-api/show) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /tasks/:id` | [docs](https://lunatask.app/api/tasks-api/show) |
| [Track Habit Activity](actions/track-habit-activity.md) | `POST /habits/:id/track` | [docs](https://lunatask.app/api/habits-api/track-activity) |
| [Update Note](actions/update-note.md) | `PUT /notes/:id` | [docs](https://lunatask.app/api/notes-api/update) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://lunatask.app/api/tasks-api/update) |

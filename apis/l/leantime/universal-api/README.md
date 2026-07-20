# <img src="https://images.mindcloud.co/apps/icons/icone-new-150x150_1774981498571.png" alt="Leantime logo" width="28" height="28"> Leantime: Universal API

Manage strategy, plans, projects, tasks, and execution workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/leantime/latest
- **Category:** Productivity / Project Management
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://leantime.io
- **Vendor API docs:** https://docs.leantime.io/api/README

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Project Types](actions/list-project-types.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leantime/latest/actions/list-project-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Delete Client](actions/delete-client.md) | DELETE |  |
| [Get Client](actions/get-client.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |
| [Update Client](actions/update-client.md) | PUT |  |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST |  |
| [List Comments](actions/list-comments.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files By Module](actions/list-files-by-module.md) | GET |  |

### Milestone

| Action | Method | Description |
| --- | --- | --- |
| [Create Milestone](actions/create-milestone.md) | POST |  |
| [Get Milestone Progress](actions/get-milestone-progress.md) | GET |  |
| [List Milestones](actions/list-milestones.md) | GET |  |
| [Update Milestone](actions/update-milestone.md) | PUT |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Check Clock Status](actions/check-clock-status.md) | GET |  |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [List Time Entries](actions/list-time-entries.md) | GET |  |
| [Log Time](actions/log-time.md) | POST |  |
| [Punch In](actions/punch-in.md) | POST |  |
| [Punch Out](actions/punch-out.md) | PUT |  |
| [Upload File](actions/upload-file.md) | POST |  |
| [Upsert Time Entry](actions/upsert-time-entry.md) | POST |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Duplicate Project](actions/duplicate-project.md) | POST |  |
| [Get Project](actions/get-project.md) | GET |  |
| [Get Project Progress](actions/get-project-progress.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |
| [Search Projects](actions/search-projects.md) | GET |  |
| [Update Project](actions/update-project.md) | PUT |  |

### Project Type

| Action | Method | Description |
| --- | --- | --- |
| [List Project Types](actions/list-project-types.md) | GET |  |

### Sprint

| Action | Method | Description |
| --- | --- | --- |
| [Create Sprint](actions/create-sprint.md) | POST |  |
| [List Sprints](actions/list-sprints.md) | GET |  |
| [Update Sprint](actions/update-sprint.md) | PUT |  |

### Status Label

| Action | Method | Description |
| --- | --- | --- |
| [List Status Labels](actions/list-status-labels.md) | GET |  |

### Subtask

| Action | Method | Description |
| --- | --- | --- |
| [List Subtasks](actions/list-subtasks.md) | GET |  |
| [Upsert Subtask](actions/upsert-subtask.md) | PUT |  |

### Ticket

| Action | Method | Description |
| --- | --- | --- |
| [Create Ticket](actions/create-ticket.md) | POST |  |
| [Delete Ticket](actions/delete-ticket.md) | DELETE |  |
| [Get Ticket](actions/get-ticket.md) | GET |  |
| [List Tickets](actions/list-tickets.md) | GET |  |
| [Move Ticket](actions/move-ticket.md) | PUT |  |
| [Search Tickets](actions/search-tickets.md) | GET |  |
| [Update Ticket](actions/update-ticket.md) | PUT |  |

### Ticket Type

| Action | Method | Description |
| --- | --- | --- |
| [List Ticket Types](actions/list-ticket-types.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST |  |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Get User](actions/get-user.md) | GET |  |
| [Get User by Email](actions/get-user-by-email.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |
| [Update User](actions/update-user.md) | PUT |  |


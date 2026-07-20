# Leantime: Native API Reference

A consolidated summary of Leantime's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://docs.leantime.io/api/README
- **API base URL:** `{workspaceUrl}/api/jsonrpc`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required
- **Workspace URL:** `workspaceUrl` · required · Your Leantime workspace URL without a trailing slash, for example https://yourcompany.leantime.io

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://docs.leantime.io/api/usage)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `result`.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Comments/Services/Comments) |
| [Check Clock Status](actions/check-clock-status.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets) |
| [Create Client](actions/create-client.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients) |
| [Create Milestone](actions/create-milestone.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Create Project](actions/create-project.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [Create Sprint](actions/create-sprint.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Sprints/Services/Sprints) |
| [Create Ticket](actions/create-ticket.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Create User](actions/create-user.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users) |
| [Delete Client](actions/delete-client.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients) |
| [Delete File](actions/delete-file.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Files/Services/Files) |
| [Delete Ticket](actions/delete-ticket.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Delete User](actions/delete-user.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users) |
| [Duplicate Project](actions/duplicate-project.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [Get Client](actions/get-client.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients) |
| [Get Milestone Progress](actions/get-milestone-progress.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Get Project](actions/get-project.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [Get Project Progress](actions/get-project-progress.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [Get Ticket](actions/get-ticket.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Get User](actions/get-user.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users) |
| [Get User by Email](actions/get-user-by-email.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users) |
| [List Clients](actions/list-clients.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients) |
| [List Comments](actions/list-comments.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Comments/Services/Comments) |
| [List Files By Module](actions/list-files-by-module.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Files/Services/Files) |
| [List Milestones](actions/list-milestones.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [List Project Types](actions/list-project-types.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [List Projects](actions/list-projects.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [List Sprints](actions/list-sprints.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Sprints/Services/Sprints) |
| [List Status Labels](actions/list-status-labels.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [List Subtasks](actions/list-subtasks.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [List Ticket Types](actions/list-ticket-types.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [List Tickets](actions/list-tickets.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [List Time Entries](actions/list-time-entries.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets) |
| [List Users](actions/list-users.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users) |
| [Log Time](actions/log-time.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets) |
| [Move Ticket](actions/move-ticket.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Punch In](actions/punch-in.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets) |
| [Punch Out](actions/punch-out.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets) |
| [Search Projects](actions/search-projects.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [Search Tickets](actions/search-tickets.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Update Client](actions/update-client.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Clients/Services/Clients) |
| [Update Milestone](actions/update-milestone.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Update Project](actions/update-project.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects) |
| [Update Sprint](actions/update-sprint.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Sprints/Services/Sprints) |
| [Update Ticket](actions/update-ticket.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Update User](actions/update-user.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Users/Services/Users) |
| [Upload File](actions/upload-file.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Files/Services/Files) |
| [Upsert Subtask](actions/upsert-subtask.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Tickets/Services/Tickets) |
| [Upsert Time Entry](actions/upsert-time-entry.md) | `POST /` | [docs](https://docs.leantime.io/api/classes/Leantime/Domain/Timesheets/Services/Timesheets) |

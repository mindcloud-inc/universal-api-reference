# ProProfs Project: Native API Reference

A consolidated summary of ProProfs Project's API configuration and 46 documented operations, with links to official documentation.

- **Official docs:** https://help.proprofsproject.com/docs
- **API base URL:** `https://api.projectbubble.com/v2`

## Authentication

### API Key and Domain

Authenticate with your ProProfs Project API key and tenant domain.

### Credentials

- **API Key:** `apiKey` · required · Your ProProfs Project API key from the My Account page.
- **Domain:** `domain` · required · Your full tenant domain, for example mydomain.projectbubble.com.

Send these headers with each API request:

```http
key: <apiKey>
domain: <domain>
```

[Official authentication documentation](https://help.proprofsproject.com/api-for-developers)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (46 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://help.proprofsproject.com/clients-api) |
| [Create Comment](actions/create-comment.md) | `POST /comments/{{project_id}}` | [docs](https://help.proprofsproject.com/managing-comments) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://help.proprofsproject.com/events) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://help.proprofsproject.com/projects) |
| [Create Subtask](actions/create-subtask.md) | `POST /subtasks/{{task_id}}` | [docs](https://help.proprofsproject.com/subtasks) |
| [Create Task](actions/create-task.md) | `POST /tasks/{{project_id}}` | [docs](https://help.proprofsproject.com/tasks) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /time_entries/{{task_id}}` | [docs](https://help.proprofsproject.com/time-entries) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /hooks` | [docs](https://help.proprofsproject.com/webhooks) |
| [Delete Client](actions/delete-client.md) | `DELETE /clients/{{client_id}}` | [docs](https://help.proprofsproject.com/clients-api) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /comments/{{comment_id}}` | [docs](https://help.proprofsproject.com/managing-comments) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{{contact_id}}` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/{{event_id}}` | [docs](https://help.proprofsproject.com/events) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/{{project_id}}` | [docs](https://help.proprofsproject.com/projects) |
| [Delete Subtask](actions/delete-subtask.md) | `DELETE /subtasks/{{subtask_id}}` | [docs](https://help.proprofsproject.com/subtasks) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/{{task_id}}` | [docs](https://help.proprofsproject.com/tasks) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /time_entries/{{entry_id}}` | [docs](https://help.proprofsproject.com/time-entries) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /hooks/{{subscription_id}}` | [docs](https://help.proprofsproject.com/webhooks) |
| [Get Client](actions/get-client.md) | `GET /clients/{{client_id}}` | [docs](https://help.proprofsproject.com/clients-api) |
| [Get Comment](actions/get-comment.md) | `GET /comments/{{comment_id}}` | [docs](https://help.proprofsproject.com/managing-comments) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://help.proprofsproject.com/company-users) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/{{contact_id}}` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Get Event](actions/get-event.md) | `GET /events/{{event_id}}` | [docs](https://help.proprofsproject.com/events) |
| [Get Project](actions/get-project.md) | `GET /projects/{{project_id}}` | [docs](https://help.proprofsproject.com/projects) |
| [Get Subtask](actions/get-subtask.md) | `GET /subtasks/{{subtask_id}}` | [docs](https://help.proprofsproject.com/subtasks) |
| [Get Task](actions/get-task.md) | `GET /tasks/{{task_id}}` | [docs](https://help.proprofsproject.com/tasks) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /time_entries/{{entry_id}}` | [docs](https://help.proprofsproject.com/time-entries) |
| [Get User](actions/get-user.md) | `GET /users/{{user_id}}` | [docs](https://help.proprofsproject.com/company-users) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://help.proprofsproject.com/clients-api) |
| [List Comments](actions/list-comments.md) | `GET /comments` | [docs](https://help.proprofsproject.com/managing-comments) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [List Events](actions/list-events.md) | `GET /events` | [docs](https://help.proprofsproject.com/events) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://help.proprofsproject.com/files) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://help.proprofsproject.com/projects) |
| [List Subtasks](actions/list-subtasks.md) | `GET /subtasks` | [docs](https://help.proprofsproject.com/subtasks) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://help.proprofsproject.com/tasks) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://help.proprofsproject.com/company-users) |
| [List Time Entries](actions/list-time-entries.md) | `GET /time_entries` | [docs](https://help.proprofsproject.com/time-entries) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://help.proprofsproject.com/company-users) |
| [Update Client](actions/update-client.md) | `PUT /clients/{{client_id}}` | [docs](https://help.proprofsproject.com/clients-api) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/{{contact_id}}` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Update Event](actions/update-event.md) | `PUT /events/{{event_id}}` | [docs](https://help.proprofsproject.com/events) |
| [Update Project](actions/update-project.md) | `PUT /projects/{{project_id}}` | [docs](https://help.proprofsproject.com/projects) |
| [Update Subtask](actions/update-subtask.md) | `PUT /subtasks/{{subtask_id}}` | [docs](https://help.proprofsproject.com/subtasks) |
| [Update Task](actions/update-task.md) | `PUT /tasks/{{task_id}}` | [docs](https://help.proprofsproject.com/tasks) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /time_entries/{{entry_id}}` | [docs](https://help.proprofsproject.com/time-entries) |

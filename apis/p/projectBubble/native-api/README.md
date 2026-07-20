# Project Bubble: Native API Reference

A consolidated summary of Project Bubble's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://help.proprofsproject.com/developers
- **API base URL:** `https://api.projectbubble.com/v2`

## Authentication

### API Key + Domain

Authenticate with your ProProfs Project API key and full Project Bubble domain.

### Credentials

- **API Key:** `apiKey` · required · Your Project Bubble API key from the My Account page.
- **Domain:** `domain` · required · Your full Project Bubble domain, for example mindcloud.projectbubble.com.

Send these headers with each API request:

```http
key: <apiKey>
domain: <domain>
```

[Official authentication documentation](https://help.proprofsproject.com/api-for-developers)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /comments/:project_id` | [docs](https://help.proprofsproject.com/managing-comments) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Create Event](actions/create-event.md) | `POST /events` | [docs](https://help.proprofsproject.com/events) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://help.proprofsproject.com/projects) |
| [Create Task](actions/create-task.md) | `POST /tasks/:project_id` | [docs](https://help.proprofsproject.com/tasks) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /comments/:comment_id` | [docs](https://help.proprofsproject.com/managing-comments) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contact_id` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Delete Event](actions/delete-event.md) | `DELETE /events/:event_id` | [docs](https://help.proprofsproject.com/events) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:project_id` | [docs](https://help.proprofsproject.com/projects) |
| [Get Comment](actions/get-comment.md) | `GET /comments/:comment_id` | [docs](https://help.proprofsproject.com/managing-comments) |
| [Get Company](actions/get-company.md) | `GET /company` | [docs](https://help.proprofsproject.com/company-users) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contact_id` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Get Event](actions/get-event.md) | `GET /events/:event_id` | [docs](https://help.proprofsproject.com/events) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://help.proprofsproject.com/projects) |
| [Get Task](actions/get-task.md) | `GET /tasks/:task_id` | [docs](https://help.proprofsproject.com/tasks) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://help.proprofsproject.com/company-users) |
| [List Files](actions/list-files.md) | `GET /files` | [docs](https://help.proprofsproject.com/files) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://help.proprofsproject.com/company-users) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contact_id` | [docs](https://help.proprofsproject.com/managing-contacts) |
| [Update Event](actions/update-event.md) | `PUT /events/:event_id` | [docs](https://help.proprofsproject.com/events) |
| [Update Project](actions/update-project.md) | `PUT /projects/:project_id` | [docs](https://help.proprofsproject.com/projects) |

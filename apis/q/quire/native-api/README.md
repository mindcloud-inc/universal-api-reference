# Quire: Native API Reference

A consolidated summary of Quire's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://quire.io/dev/api/
- **API base URL:** `https://quire.io/api`

## Authentication

### OAuth 2.0

OAuth 2.0 for Quire REST API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://quire.io/oauth to approve access.
2. Exchange the returned authorization code with a POST request to https://quire.io/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://quire.io/oauth/token.

[Official authentication documentation](https://quire.io/dev/api/)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Status](actions/create-status.md) | `POST status/id/:projectId` | [docs](https://quire.io/dev/api/#operation--status-id--projectId--post) |
| [Create Tag](actions/create-tag.md) | `POST tag/id/:projectId` | [docs](https://quire.io/dev/api/#operation--tag-id--projectId--post) |
| [Create Task](actions/create-task.md) | `POST task/id/:projectId` | [docs](https://quire.io/dev/api/#operation--task-id--projectId--post) |
| [Delete Status](actions/delete-status.md) | `DELETE status/id/:projectId/:value` | [docs](https://quire.io/dev/api/#operation--status-id--projectId---value--delete) |
| [Delete Tag](actions/delete-tag.md) | `DELETE tag/:oid` | [docs](https://quire.io/dev/api/#operation--tag--oid--delete) |
| [Delete Task](actions/delete-task.md) | `DELETE task/:oid` | [docs](https://quire.io/dev/api/#operation--task--oid--delete) |
| [Get Current User](actions/get-current-user.md) | `GET user/id/me` | [docs](https://quire.io/dev/api/#operation--user-id--id--get) |
| [Get Project](actions/get-project.md) | `GET project/id/:id` | [docs](https://quire.io/dev/api/#operation--project-id--id--get) |
| [Get Status](actions/get-status.md) | `GET status/id/:projectId/:value` | [docs](https://quire.io/dev/api/#operation--status-id--projectId---value--get) |
| [Get Tag](actions/get-tag.md) | `GET tag/:oid` | [docs](https://quire.io/dev/api/#operation--tag--oid--get) |
| [Get Task](actions/get-task.md) | `GET task/id/:projectId/:id` | [docs](https://quire.io/dev/api/#operation--task-id--projectId---id--get) |
| [List Projects](actions/list-projects.md) | `GET project/list` | [docs](https://quire.io/dev/api/#operation--project-list-get) |
| [List Root Tasks](actions/list-root-tasks.md) | `GET task/list/id/:projectId` | [docs](https://quire.io/dev/api/#operation--task-list-id--projectId--get) |
| [List Statuses](actions/list-statuses.md) | `GET status/list/id/:projectId` | [docs](https://quire.io/dev/api/#operation--status-list-id--projectId--get) |
| [List Subtasks](actions/list-subtasks.md) | `GET task/list/id/:projectId/:taskId` | [docs](https://quire.io/dev/api/#operation--task-list-id--projectId---taskId--get) |
| [List Tags](actions/list-tags.md) | `GET tag/list/:projectOid` | [docs](https://quire.io/dev/api/#operation--tag-list--projectOid--get) |
| [List Users](actions/list-users.md) | `GET user/list` | [docs](https://quire.io/dev/api/#operation--user-list-get) |
| [Search Tasks](actions/search-tasks.md) | `GET task/search/id/:projectId` | [docs](https://quire.io/dev/api/#operation--task-search-id--projectId--get) |
| [Update Status](actions/update-status.md) | `PUT status/id/:projectId/:value` | [docs](https://quire.io/dev/api/#operation--status-id--projectId---value--put) |
| [Update Tag](actions/update-tag.md) | `PUT tag/:oid` | [docs](https://quire.io/dev/api/#operation--tag--oid--put) |
| [Update Task](actions/update-task.md) | `PUT task/id/:projectId/:id` | [docs](https://quire.io/dev/api/#operation--task-id--projectId---id--put) |

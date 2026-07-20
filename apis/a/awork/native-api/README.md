# Awork: Native API Reference

A consolidated summary of Awork's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.awork.com/
- **OpenAPI specification:** https://api.awork.com/openapi/v1
- **API base URL:** `https://api.awork.com/api/v1`

## Authentication

### OAuth 2.1

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.awork.com/api/v1/accounts/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.awork.com/api/v1/accounts/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `full_access offline_access`.

PKCE is enabled with the `other` challenge method. The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://api.awork.com/api/v1/accounts/token.

[Official authentication documentation](https://developers.awork.com/authentication)

## Pagination

Use `pageSize` in the query string to set the page size (default 10; maximum 1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.awork.com/apiv1/projects/post-project) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developers.awork.com/apiv1/tasks/creates-a-new-task) |
| [Create Task Comment](actions/create-task-comment.md) | `POST /tasks/:taskId/comments` | [docs](https://developers.awork.com/apiv1/task-comments/post-task-comment) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /timeentries` | [docs](https://developers.awork.com/apiv1/time-entries/post-time-entry) |
| [Get Company](actions/get-company.md) | `GET /companies/:companyId` | [docs](https://developers.awork.com/companies) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://developers.awork.com/apiv1/users/returns-the-currently-logged-in-user-and-workspace) |
| [Get Document](actions/get-document.md) | `GET /documents/:documentId` | [docs](https://developers.awork.com/apiv1/documents/get-document-by-id) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://developers.awork.com/apiv1/projects/returns-the-project-with-the-specified-id) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://developers.awork.com/tasks) |
| [Get Task By Key](actions/get-task-by-key.md) | `GET /tasks/key/:taskIdentifier` | [docs](https://developers.awork.com/tasks) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://developers.awork.com/apiv1/users/get-user) |
| [List Assigned Tasks](actions/list-assigned-tasks.md) | `GET /me/assignedtasks` | [docs](https://developers.awork.com/apiv1/assigned-tasks/get-my-me-assigned-tasks) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developers.awork.com/apiv1/companies/get-companies) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://developers.awork.com/apiv1/documents/returns-all-documents) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/:projectId/projecttasks` | [docs](https://developers.awork.com/apiv1/project-tasks/returns-all-project-tasks-of-the-project-with-the-specified-id) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.awork.com/apiv1/projects/returns-all-projects) |
| [List Task Comments](actions/list-task-comments.md) | `GET /tasks/:taskId/comments` | [docs](https://developers.awork.com/apiv1/task-comments/get-task-comments) |
| [List Time Entries](actions/list-time-entries.md) | `GET /timeentries` | [docs](https://developers.awork.com/apiv1/time-entries/get-time-entries) |
| [List User Workloads](actions/list-user-workloads.md) | `GET /users/workload` | [docs](https://developers.awork.com/workload) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.awork.com/apiv1/users/get-users) |
| [Search Workspace](actions/search-workspace.md) | `GET /search` | [docs](https://developers.awork.com/search) |
| [Set Task Assignees](actions/set-task-assignees.md) | `POST /tasks/:taskId/setassignees` | [docs](https://developers.awork.com/apiv1/tasks/post-set-assignees) |
| [Update Project](actions/update-project.md) | `PUT /projects/:projectId` | [docs](https://developers.awork.com/apiv1/projects/put-project) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://developers.awork.com/apiv1/tasks/put-task) |

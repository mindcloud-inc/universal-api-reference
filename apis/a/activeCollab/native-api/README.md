# ActiveCollab: Native API Reference

A consolidated summary of ActiveCollab's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://developers.activecollab.com/api-documentation/index.html
- **API base URL:** `https://app.activecollab.com/:instanceId/api/v1`

## Authentication

### API Key

Connect with an ActiveCollab API token. MindCloud sends the token as a Bearer authorization header at runtime.

### Credentials

- **API Key:** `apiKey` · required
- **Instance ID:** `instanceId` · required · Your ActiveCollab workspace instance ID from the app URL, for example 459658.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://activecollab.com/help/books/my-active-collab/api-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instanceId` | path | `string` | yes | Your ActiveCollab workspace instance ID from the URL, for example 459658. |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/projects.html) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:projectId` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/projects.html) |
| [Get Company](actions/get-company.md) | `GET /companies/:companyId` | [docs](https://developers.activecollab.com/api-documentation/v1/people/companies/all.html) |
| [Get Default Job Type](actions/get-default-job-type.md) | `GET /job-types/default` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/time-records/job-types.html) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/projects.html) |
| [Get User](actions/get-user.md) | `GET /users/:userId` | [docs](https://developers.activecollab.com/api-documentation/v1/people/users/users.html) |
| [Get Workspace Info](actions/get-workspace-info.md) | `GET /info` | [docs](https://developers.activecollab.com/api-documentation/v1/info.html) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://developers.activecollab.com/api-documentation/v1/people/companies/all.html) |
| [List Discussions](actions/list-discussions.md) | `GET /projects/:projectId/discussions` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/discussions.html) |
| [List Job Types](actions/list-job-types.md) | `GET /job-types` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/time-records/job-types.html) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://developers.activecollab.com/api-documentation/v1/utilities/labels.html) |
| [List Notes](actions/list-notes.md) | `GET /projects/:projectId/notes` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/notes/notes.html) |
| [List Project Labels](actions/list-project-labels.md) | `GET /labels/project-labels` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/labels.html) |
| [List Project Time Records](actions/list-project-time-records.md) | `GET /projects/:projectId/time-records` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/time-records/time-records.html) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/projects.html) |
| [List Task Lists](actions/list-task-lists.md) | `GET /projects/:projectId/task-lists` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/task-lists/task-lists.html) |
| [List Tasks](actions/list-tasks.md) | `GET /projects/:projectId/tasks` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/elements/tasks/tasks.html) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.activecollab.com/api-documentation/v1/people/users/users.html) |
| [Update Project](actions/update-project.md) | `PUT /projects/:projectId` | [docs](https://developers.activecollab.com/api-documentation/v1/projects/projects.html) |

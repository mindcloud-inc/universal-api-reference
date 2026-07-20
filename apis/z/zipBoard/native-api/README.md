# zipBoard: Native API Reference

A consolidated summary of zipBoard's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.zipboard.co/
- **API base URL:** `https://app.zipboard.co/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.zipboard.co/article/171-api-authentication-and-uri-structure)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | `POST /issues/comments` | [docs](https://help.zipboard.co/article/182-api-for-issues-feedback) |
| [Create File](actions/create-file.md) | `POST /files` | [docs](https://help.zipboard.co/article/179-api-for-files-url) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://help.zipboard.co/article/178-api-for-project) |
| [Create Response](actions/create-response.md) | `POST /issues/responses` | [docs](https://docs.zipboard.co/#tag/Responses/paths/~1api~1v1~1issues~1responses/post) |
| [Create Review Link](actions/create-review-link.md) | `POST /shareurl` | [docs](https://help.zipboard.co/article/180-api-for-review-links) |
| [Create Task](actions/create-task.md) | `POST /issues/tasks` | [docs](https://help.zipboard.co/article/181-api-for-issues-task) |
| [Delete Feedback](actions/delete-feedback.md) | `DELETE /issues/comments/:id` | [docs](https://help.zipboard.co/article/182-api-for-issues-feedback) |
| [Delete File](actions/delete-file.md) | `DELETE /files/:id` | [docs](https://help.zipboard.co/article/179-api-for-files-url) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://help.zipboard.co/article/178-api-for-project) |
| [Delete Response](actions/delete-response.md) | `DELETE /issues/responses/:id` | [docs](https://docs.zipboard.co/#tag/Responses/paths/~1api~1v1~1issues~1responses~1{id}/delete) |
| [Delete Review Link](actions/delete-review-link.md) | `DELETE /shareurl/:id` | [docs](https://help.zipboard.co/article/180-api-for-review-links) |
| [Delete Task](actions/delete-task.md) | `DELETE /issues/tasks/:id` | [docs](https://help.zipboard.co/article/181-api-for-issues-task) |
| [Get Feedback](actions/get-feedback.md) | `GET /issues/comments` | [docs](https://help.zipboard.co/article/182-api-for-issues-feedback) |
| [Get Files](actions/get-files.md) | `GET /files` | [docs](https://help.zipboard.co/article/179-api-for-files-url) |
| [Get Organization](actions/get-organization.md) | `GET /organization` | [docs](https://docs.zipboard.co/#tag/Organizations/paths/~1api~1v1~1organization/get) |
| [Get Organizations](actions/get-organizations.md) | `GET /orgs` | [docs](https://help.zipboard.co/article/237-api-for-organization) |
| [Get Project Collaborators](actions/get-project-collaborators.md) | `GET /project/:id/collaborators` | [docs](https://docs.zipboard.co/#tag/Collaborators/paths/~1api~1v1~1project~1{id}~1collaborators/get) |
| [Get Projects](actions/get-projects.md) | `GET /projects` | [docs](https://help.zipboard.co/article/178-api-for-project) |
| [Get Responses](actions/get-responses.md) | `GET /issues/responses` | [docs](https://docs.zipboard.co/#tag/Responses/paths/~1api~1v1~1issues~1responses/get) |
| [Get Review Links](actions/get-review-links.md) | `GET /shareurl` | [docs](https://help.zipboard.co/article/180-api-for-review-links) |
| [Get Tasks](actions/get-tasks.md) | `GET /issues/tasks` | [docs](https://help.zipboard.co/article/181-api-for-issues-task) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://docs.zipboard.co/#tag/Users/paths/~1api~1v1~1user/get) |
| [Get User by ID](actions/get-user-by-id.md) | `GET /user/:id` | [docs](https://docs.zipboard.co/#tag/Users/paths/~1api~1v1~1user~1{id}/get) |
| [Remove Project Collaborator](actions/remove-project-collaborator.md) | `DELETE /project/:id/collaborators` | [docs](https://docs.zipboard.co/#tag/Collaborators/paths/~1api~1v1~1project~1{id}~1collaborators/delete) |
| [Update Feedback](actions/update-feedback.md) | `PUT /issues/comments/:id` | [docs](https://help.zipboard.co/article/182-api-for-issues-feedback) |
| [Update File](actions/update-file.md) | `PUT /files/:id` | [docs](https://help.zipboard.co/article/179-api-for-files-url) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://help.zipboard.co/article/178-api-for-project) |
| [Update Response](actions/update-response.md) | `PUT /issues/responses/:id` | [docs](https://docs.zipboard.co/#tag/Responses/paths/~1api~1v1~1issues~1responses~1{id}/put) |
| [Update Task](actions/update-task.md) | `PUT /issues/tasks/:id` | [docs](https://help.zipboard.co/article/181-api-for-issues-task) |
| [Update User](actions/update-user.md) | `PUT /user/:id` | [docs](https://docs.zipboard.co/#tag/Users/paths/~1api~1v1~1user~1{id}/put) |

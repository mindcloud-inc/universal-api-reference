# Hex: Native API Reference

A consolidated summary of Hex's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://learn.hex.tech/docs/api-integrations/api/reference
- **OpenAPI specification:** https://static.hex.site/openapi.json
- **API base URL:** `https://app.hex.tech/api/v1`

## Authentication

### API Key

Connect with a Hex personal access token or workspace token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://learn.hex.tech/docs/api-integrations/api/overview)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `values`. The next-page cursor is read from `pagination.after`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortDirection`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Project Run](actions/cancel-project-run.md) | `DELETE /projects/:projectId/runs/:runId` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CancelRun) |
| [Create Collection](actions/create-collection.md) | `POST /collections` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreateCollection) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreateGroup) |
| [Create Presigned Embed URL](actions/create-presigned-embed-url.md) | `POST /embedding/createPresignedUrl/{projectId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreatePresignedUrl) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/CreateProject) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/{groupId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/DeleteGroup) |
| [Get Collection](actions/get-collection.md) | `GET /collections/{collectionId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetCollection) |
| [Get Group](actions/get-group.md) | `GET /groups/{groupId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetGroup) |
| [Get Project](actions/get-project.md) | `GET /projects/{projectId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetProject) |
| [Get Project Run](actions/get-project-run.md) | `GET /projects/:projectId/runs/:runId` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetRunStatus) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/ListCollections) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/ListGroups) |
| [List Project Runs](actions/list-project-runs.md) | `GET /projects/{projectId}/runs` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/GetProjectRuns) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/ListProjects) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/ListUsers) |
| [Run Project](actions/run-project.md) | `POST /projects/:projectId/runs` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/RunProject) |
| [Update Collection](actions/update-collection.md) | `PATCH /collections/{collectionId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/EditCollection) |
| [Update Group](actions/update-group.md) | `PATCH /groups/{groupId}` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/EditGroup) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:projectId` | [docs](https://learn.hex.tech/docs/api-integrations/api/reference#operation/UpdateProject) |

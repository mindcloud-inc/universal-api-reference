# Gridly: Native API Reference

A consolidated summary of Gridly's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.gridly.com/docs/api/
- **API base URL:** `https://api.gridly.com/v1`

## Authentication

### API Key

Authenticate Gridly requests with a company or personal API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.gridly.com/en/create-and-manage-api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Column](actions/create-column.md) | `POST /views/:viewId/columns` | [docs](https://www.gridly.com/docs/api/#create-a-column) |
| [Create Dependency](actions/create-dependency.md) | `POST /views/:viewId/dependencies` | [docs](https://www.gridly.com/docs/api/#create-a-dependency) |
| [Create Grid](actions/create-grid.md) | `POST /grids` | [docs](https://www.gridly.com/docs/api/#create-grid) |
| [Create View](actions/create-view.md) | `POST /views` | [docs](https://www.gridly.com/docs/api/#create-view) |
| [Delete Column](actions/delete-column.md) | `DELETE /views/:viewId/columns/:id` | [docs](https://www.gridly.com/docs/api/#delete-a-column) |
| [Delete Dependency](actions/delete-dependency.md) | `DELETE /views/:viewId/dependencies/:id` | [docs](https://www.gridly.com/docs/api/#delete-a-dependency) |
| [Delete Grid](actions/delete-grid.md) | `DELETE /grids/:id` | [docs](https://www.gridly.com/docs/api/#delete-a-grid) |
| [Delete View](actions/delete-view.md) | `DELETE /views/:id` | [docs](https://www.gridly.com/docs/api/#delete-view) |
| [Get Branch](actions/get-branch.md) | `GET /branches/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-branch) |
| [Get Column](actions/get-column.md) | `GET /views/:viewId/columns/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-column) |
| [Get Database](actions/get-database.md) | `GET /databases/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-database) |
| [Get Dependency](actions/get-dependency.md) | `GET /views/:viewId/dependencies/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-dependency) |
| [Get Grid](actions/get-grid.md) | `GET /grids/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-grid) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-project) |
| [Get View](actions/get-view.md) | `GET /views/:id` | [docs](https://www.gridly.com/docs/api/#retrieve-a-view) |
| [List Branches](actions/list-branches.md) | `GET /branches` | [docs](https://www.gridly.com/docs/api/#list-branches) |
| [List Databases](actions/list-databases.md) | `GET /databases` | [docs](https://www.gridly.com/docs/api/#list-databases) |
| [List Dependencies](actions/list-dependencies.md) | `GET /views/:viewId/dependencies` | [docs](https://www.gridly.com/docs/api/#list-dependencies) |
| [List Grids](actions/list-grids.md) | `GET /grids` | [docs](https://www.gridly.com/docs/api/#list-grids) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.gridly.com/docs/api/#list-projects) |
| [List Records](actions/list-records.md) | `GET /views/:viewId/records` | [docs](https://www.gridly.com/docs/api/#list-records) |
| [List Views](actions/list-views.md) | `GET /views` | [docs](https://www.gridly.com/docs/api/#list-views) |
| [Update Column](actions/update-column.md) | `PATCH /views/:viewId/columns/:id` | [docs](https://www.gridly.com/docs/api/#update-a-column) |
| [Update Dependency](actions/update-dependency.md) | `PUT /views/:viewId/dependencies/:id` | [docs](https://www.gridly.com/docs/api/#update-a-dependency) |
| [Update Grid](actions/update-grid.md) | `PATCH /grids/:id` | [docs](https://www.gridly.com/docs/api/#update-a-grid) |

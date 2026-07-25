# CoordinateHQ: Native API Reference

A consolidated summary of CoordinateHQ's API configuration and 12 documented operations.

- **API base URL:** `https://app.coordinatehq.com/api/v1`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Bearer: <apiKey>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Organization Stakeholder](actions/add-organization-stakeholder.md) | `POST /organizations/:organizationId/stakeholders` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#organizations) |
| [Add Project to Organization](actions/add-project-to-organization.md) | `POST /organizations/:organizationId/projects` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#organizations) |
| [Attach Task File](actions/attach-task-file.md) | `POST /projects/:project_id/task/:task_id/files/attach` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#project-pages) |
| [Create Organization](actions/create-organization.md) | `POST /organizations` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#organizations) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#projects) |
| [Download Task File](actions/download-task-file.md) | `GET /projects/:project_id/task/:task_id/file/:file_id` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#tasks) |
| [Get Task](actions/get-task.md) | `GET /projects/:project_id/task/:task_id` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#project-pages) |
| [List Entity](actions/list-entity.md) | `GET /entity` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#entity) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#organizations) |
| [List Project Group](actions/list-project-group.md) | `GET /projects/:projectId/group` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#groups) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/:projectId/task` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#tasks) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://app.coordinatehq.com/static/API_Documentation.html#projects) |

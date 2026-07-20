# KiteSuite: Native API Reference

A consolidated summary of KiteSuite's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://api.kitesuite.com/swagger/
- **API base URL:** `https://api.kitesuite.com`

## Authentication

### API Token

Authenticate with a KiteSuite API token and workspace key.

### Credentials

- **API Key:** `apiKey` · required
- **Workspace Key:** `workspace_key` · required

Send these headers with each API request:

```http
api-token: <apiKey>
workspace: <workspace_key>
```

[Official authentication documentation](https://api.kitesuite.com/swagger/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Member](actions/add-project-member.md) | `POST /api/v1/project/member` | [docs](https://api.kitesuite.com/swagger/) |
| [Add Workspace Member](actions/add-workspace-member.md) | `POST /api/v1/workspace/member` | [docs](https://api.kitesuite.com/swagger/) |
| [Create List](actions/create-list.md) | `POST /api/v1/list` | [docs](https://api.kitesuite.com/swagger/) |
| [Create Project](actions/create-project.md) | `POST /api/v1/project` | [docs](https://api.kitesuite.com/swagger/) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Project](actions/get-project.md) | `GET /api/v1/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Project Data](actions/get-project-data.md) | `GET /api/v1/project/all/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get User](actions/get-user.md) | `GET /api/v1/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/v1/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Get Workspace Project Data](actions/get-workspace-project-data.md) | `GET /api/v1/project/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [List Project Lists](actions/list-project-lists.md) | `GET /api/v1/list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [List User Workspaces](actions/list-user-workspaces.md) | `GET /api/v1/workspace/user/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [List Workspace Documents](actions/list-workspace-documents.md) | `GET /api/v1/document` | [docs](https://api.kitesuite.com/swagger/) |
| [List Workspace Roles](actions/list-workspace-roles.md) | `GET /api/v1/workspace-role` | [docs](https://api.kitesuite.com/swagger/) |
| [List Workspace Users](actions/list-workspace-users.md) | `GET /api/v1/user/workspace/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Move Task To List](actions/move-task-to-list.md) | `PATCH /api/v1/list/task/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Search Workspace Data](actions/search-workspace-data.md) | `GET /api/v1/workspace/search/:query` | [docs](https://api.kitesuite.com/swagger/) |
| [Update List](actions/update-list.md) | `PATCH /api/v1/list/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Project](actions/update-project.md) | `PUT /api/v1/project/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Project Member Role](actions/update-project-member-role.md) | `PATCH /api/v1/project/member/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Workspace Member Role](actions/update-workspace-member-role.md) | `PATCH /api/v1/workspace/member/:id` | [docs](https://api.kitesuite.com/swagger/) |
| [Update Workspace Role](actions/update-workspace-role.md) | `PATCH /api/v1/workspace-role/:id` | [docs](https://api.kitesuite.com/swagger/) |

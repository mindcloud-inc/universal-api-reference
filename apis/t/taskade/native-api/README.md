# Taskade: Native API Reference

A consolidated summary of Taskade's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide
- **OpenAPI specification:** https://884954080-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FEOkDZjClZ0y8qSYnc7hO%2Fuploads%2Fgit-blob-67a8dca7dcae187ca92c97983b1be8a0aecfa00b%2Fapi-0.1.0.json?alt=media&token=e1456304-55dd-4486-b72e-cc2f742c8d81
- **API base URL:** `https://www.taskade.com/api/v1`

## Authentication

### OAuth 2.0

Connect Taskade with OAuth 2.0.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.taskade.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://www.taskade.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://www.taskade.com/oauth2/token.

[Official authentication documentation](https://docs.taskade.com/docs/developers/developers/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |
| `Content-Type` | `application/json` |

Response data is read from `items`.

## Pagination

Use `limit` in the query string to set the page size (default 100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project To Agent Knowledge](actions/add-project-to-agent-knowledge.md) | `POST /agents/:agentId/knowledge/project` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/agents/add-project-to-agent-knowledge) |
| [Copy Project](actions/copy-project.md) | `POST /projects/:projectId/copy` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/copy-project) |
| [Create Agent in Folder](actions/create-agent-in-folder.md) | `POST /folders/:folderId/agents` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/create-agent-in-folder) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/create-project) |
| [Create Project in Workspace](actions/create-project-in-workspace.md) | `POST /workspaces/:workspaceId/projects` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/workspaces/get-projects) |
| [Create Task](actions/create-task.md) | `POST /projects/:projectId/tasks/` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/create-task) |
| [Generate Agent in Folder](actions/generate-agent-in-folder.md) | `POST /folders/:folderId/agent-generate` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/generate-agent-in-folder) |
| [Get Agent](actions/get-agent.md) | `GET /agents/:agentId` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/agents/get-agent) |
| [Get Project](actions/get-project.md) | `GET /projects/:projectId` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/get-project) |
| [Get Project Share Link](actions/get-project-share-link.md) | `GET /projects/:projectId/shareLink` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/get-share-link) |
| [Get Task](actions/get-task.md) | `GET /projects/:projectId/tasks/:taskId` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task) |
| [Get Task Date](actions/get-task-date.md) | `GET /projects/:projectId/tasks/:taskId/date` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task-date) |
| [Get Task Note](actions/get-task-note.md) | `GET /projects/:projectId/tasks/:taskId/note` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task-note) |
| [List Folder Agents](actions/list-folder-agents.md) | `GET /folders/:folderId/agents` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-agents) |
| [List Folder Media Files](actions/list-folder-media-files.md) | `GET /folders/:folderId/medias` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-medias) |
| [List Folder Project Templates](actions/list-folder-project-templates.md) | `GET /folders/:folderId/project-templates` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-project-templates) |
| [List Folder Projects](actions/list-folder-projects.md) | `GET /folders/:folderId/projects` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/folders/get-folder-projects) |
| [List My Projects](actions/list-my-projects.md) | `GET /me/projects` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/me/projects) |
| [List Project Fields](actions/list-project-fields.md) | `GET /projects/:projectId/fields` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/get-project-fields) |
| [List Project Members](actions/list-project-members.md) | `GET /projects/:projectId/members` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/get-project-members) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /projects/:projectId/tasks` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/projects/get-project-tasks) |
| [List Task Assignees](actions/list-task-assignees.md) | `GET /projects/:projectId/tasks/:taskId/assignees` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/get-task-assignees) |
| [List Workspace Folders](actions/list-workspace-folders.md) | `GET /workspaces/:workspaceId/folders` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/workspaces/get-folders) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/workspaces/get-workspaces) |
| [Move Task](actions/move-task.md) | `PUT /projects/:projectId/tasks/:taskId/move` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/move-task) |
| [Update Agent](actions/update-agent.md) | `PATCH /agents/:agentId` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/agents/update-agent) |
| [Update Task](actions/update-task.md) | `PUT /projects/:projectId/tasks/:taskId` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task) |
| [Update Task Assignees](actions/update-task-assignees.md) | `PUT /projects/:projectId/tasks/:taskId/assignees` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task-assignees) |
| [Update Task Date](actions/update-task-date.md) | `PUT /projects/:projectId/tasks/:taskId/date` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task-date) |
| [Update Task Note](actions/update-task-note.md) | `PUT /projects/:projectId/tasks/:taskId/note` | [docs](https://docs.taskade.com/docs/apis-and-developer/comprehensive-api-guide/tasks/update-task-note) |

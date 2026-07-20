# Toggl Track: Native API Reference

A consolidated summary of Toggl Track's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://engineering.toggl.com/docs/track/
- **API base URL:** `https://api.track.toggl.com`

## Authentication

### API Token

Use your Toggl Track personal API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://engineering.toggl.com/docs/authentication/index.html)

## API conventions

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Client](actions/archive-client.md) | `POST /api/v9/workspaces/:workspace_id/clients/:client_id/archive` | [docs](https://engineering.toggl.com/docs/track/api/clients/#post-archives-client) |
| [Create Client](actions/create-client.md) | `POST /api/v9/workspaces/:workspace_id/clients` | [docs](https://engineering.toggl.com/docs/track/api/clients/#post-create-client) |
| [Create Project](actions/create-project.md) | `POST /api/v9/workspaces/:workspace_id/projects` | [docs](https://engineering.toggl.com/docs/track/api/projects/#post-workspaceprojects) |
| [Create Tag](actions/create-tag.md) | `POST /api/v9/workspaces/:workspace_id/tags` | [docs](https://engineering.toggl.com/docs/track/api/tags/#post-create-tag) |
| [Create Task](actions/create-task.md) | `POST /api/v9/workspaces/:workspace_id/projects/:project_id/tasks` | [docs](https://engineering.toggl.com/docs/track/api/tasks/#post-workspaceprojecttasks) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /api/v9/workspaces/:workspace_id/time_entries` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#post-timeentries) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v9/workspaces/:workspace_id/projects/:project_id` | [docs](https://engineering.toggl.com/docs/track/api/projects/#delete-workspaceproject) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/v9/workspaces/:workspace_id/tags/:tag_id` | [docs](https://engineering.toggl.com/docs/track/api/tags/#delete-delete-tag) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id` | [docs](https://engineering.toggl.com/docs/track/api/tasks/#delete-workspaceprojecttask) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /api/v9/workspaces/:workspace_id/time_entries/:time_entry_id` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#delete-timeentries) |
| [Get Client](actions/get-client.md) | `GET /api/v9/workspaces/:workspace_id/clients/:client_id` | [docs](https://engineering.toggl.com/docs/track/api/clients/#get-load-client-from-id) |
| [Get Current Time Entry](actions/get-current-time-entry.md) | `GET /api/v9/me/time_entries/current` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#get-get-current-time-entry) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v9/me` | [docs](https://engineering.toggl.com/docs/track/api/me/#get-me) |
| [Get Project](actions/get-project.md) | `GET /api/v9/workspaces/:workspace_id/projects/:project_id` | [docs](https://engineering.toggl.com/docs/track/api/projects/#get-workspaceproject) |
| [Get Task](actions/get-task.md) | `GET /api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id` | [docs](https://engineering.toggl.com/docs/track/api/tasks/#get-workspaceprojecttask) |
| [Get Time Entry By ID](actions/get-time-entry-by-id.md) | `GET /api/v9/me/time_entries/:time_entry_id` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#get-get-a-time-entry-by-id) |
| [Get Workspace](actions/get-workspace.md) | `GET /api/v9/workspaces/:workspace_id` | [docs](https://engineering.toggl.com/docs/track/api/workspaces/#get-get-single-workspace) |
| [Get Workspace Users](actions/get-workspace-users.md) | `GET /api/v9/workspaces/:workspace_id/users` | [docs](https://engineering.toggl.com/docs/track/api/workspaces/#get-get-workspace-users) |
| [List Clients](actions/list-clients.md) | `GET /api/v9/workspaces/:workspace_id/clients` | [docs](https://engineering.toggl.com/docs/track/api/clients/#get-list-clients) |
| [List Project Tasks](actions/list-project-tasks.md) | `GET /api/v9/workspaces/:workspace_id/projects/:project_id/tasks` | [docs](https://engineering.toggl.com/docs/track/api/tasks/#get-workspaceprojecttasks) |
| [List Projects](actions/list-projects.md) | `GET /api/v9/workspaces/:workspace_id/projects` | [docs](https://engineering.toggl.com/docs/track/api/projects/#get-workspaceprojects) |
| [List Tags](actions/list-tags.md) | `GET /api/v9/workspaces/:workspace_id/tags` | [docs](https://engineering.toggl.com/docs/track/api/tags/#get-tags) |
| [List Time Entries](actions/list-time-entries.md) | `GET /api/v9/me/time_entries` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#get-timeentries) |
| [List Workspaces](actions/list-workspaces.md) | `GET /api/v9/workspaces` | [docs](https://engineering.toggl.com/docs/track/api/workspaces/#get-workspaces) |
| [Search Detailed Report](actions/search-detailed-report.md) | `POST /reports/api/v3/workspace/:workspace_id/search/time_entries` | [docs](https://engineering.toggl.com/docs/track/reports/detailed_reports/#post-search-time-entries) |
| [Search Summary Report](actions/search-summary-report.md) | `POST /reports/api/v3/workspace/:workspace_id/summary/time_entries` | [docs](https://engineering.toggl.com/docs/track/reports/summary_reports/#post-search-time-entries) |
| [Stop Time Entry](actions/stop-time-entry.md) | `PATCH /api/v9/workspaces/:workspace_id/time_entries/:time_entry_id/stop` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#patch-stop-timeentry) |
| [Update Client](actions/update-client.md) | `PUT /api/v9/workspaces/:workspace_id/clients/:client_id` | [docs](https://engineering.toggl.com/docs/track/api/clients/#put-change-client) |
| [Update Project](actions/update-project.md) | `PUT /api/v9/workspaces/:workspace_id/projects/:project_id` | [docs](https://engineering.toggl.com/docs/track/api/projects/#put-workspaceproject) |
| [Update Tag](actions/update-tag.md) | `PUT /api/v9/workspaces/:workspace_id/tags/:tag_id` | [docs](https://engineering.toggl.com/docs/track/api/tags/#put-update-tag) |
| [Update Task](actions/update-task.md) | `PUT /api/v9/workspaces/:workspace_id/projects/:project_id/tasks/:task_id` | [docs](https://engineering.toggl.com/docs/track/api/tasks/#put-workspaceprojecttask) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /api/v9/workspaces/:workspace_id/time_entries/:time_entry_id` | [docs](https://engineering.toggl.com/docs/track/api/time_entries/#put-timeentries) |

# Todoist: Native API Reference

A consolidated summary of Todoist's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.todoist.com/api/v1/
- **API base URL:** `https://api.todoist.com`

## Authentication

### API Token

Todoist API token authentication via Authorization Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.todoist.com/api/v1/#tag/Authorization)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `nextCursor`.

## Pagination

Use `limit` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Task](actions/close-task.md) | `POST /api/v1/tasks/:task_id/close` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/close_task_api_v1_tasks__task_id__close_post) |
| [Create Label](actions/create-label.md) | `POST /api/v1/labels` | [docs](https://developer.todoist.com/api/v1/#tag/Labels/operation/create_label_api_v1_labels_post) |
| [Create Project](actions/create-project.md) | `POST /api/v1/projects` | [docs](https://developer.todoist.com/api/v1/#tag/Projects/operation/create_project_api_v1_projects_post) |
| [Create Section](actions/create-section.md) | `POST /api/v1/sections` | [docs](https://developer.todoist.com/api/v1/#tag/Sections/operation/create_section_api_v1_sections_post) |
| [Create Task](actions/create-task.md) | `POST /api/v1/tasks` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/create_task_api_v1_tasks_post) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/v1/projects/:project_id` | [docs](https://developer.todoist.com/api/v1/#tag/Projects/operation/delete_project_api_v1_projects__project_id__delete) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/v1/tasks/:task_id` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/delete_task_api_v1_tasks__task_id__delete) |
| [Get Project](actions/get-project.md) | `GET /api/v1/projects/:project_id` | [docs](https://developer.todoist.com/api/v1/#tag/Projects/operation/get_project_api_v1_projects__project_id__get) |
| [Get Task](actions/get-task.md) | `GET /api/v1/tasks/:task_id` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/get_task_api_v1_tasks__task_id__get) |
| [List Comments](actions/list-comments.md) | `GET /api/v1/comments` | [docs](https://developer.todoist.com/api/v1/#tag/Comments/operation/get_comments_api_v1_comments_get) |
| [List Labels](actions/list-labels.md) | `GET /api/v1/labels` | [docs](https://developer.todoist.com/api/v1/#tag/Labels/operation/get_labels_api_v1_labels_get) |
| [List Projects](actions/list-projects.md) | `GET /api/v1/projects` | [docs](https://developer.todoist.com/api/v1/#tag/Projects/operation/get_projects_api_v1_projects_get) |
| [List Sections](actions/list-sections.md) | `GET /api/v1/sections` | [docs](https://developer.todoist.com/api/v1/#tag/Sections/operation/get_sections_api_v1_sections_get) |
| [List Tasks](actions/list-tasks.md) | `GET /api/v1/tasks` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/get_tasks_api_v1_tasks_get) |
| [Move Task](actions/move-task.md) | `POST /api/v1/tasks/:task_id/move` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/move_task_api_v1_tasks__task_id__move_post) |
| [Quick Add](actions/quick-add.md) | `POST /api/v1/tasks/quick` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/quick_add_api_v1_tasks_quick_post) |
| [Reopen Task](actions/reopen-task.md) | `POST /api/v1/tasks/:task_id/reopen` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/reopen_task_api_v1_tasks__task_id__reopen_post) |
| [Search Tasks By Filter](actions/search-tasks-by-filter.md) | `GET /api/v1/tasks/filter` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/get_tasks_by_filter_api_v1_tasks_filter_get) |
| [Update Project](actions/update-project.md) | `POST /api/v1/projects/:project_id` | [docs](https://developer.todoist.com/api/v1/#tag/Projects/operation/update_project_api_v1_projects__project_id__post) |
| [Update Task](actions/update-task.md) | `POST /api/v1/tasks/:task_id` | [docs](https://developer.todoist.com/api/v1/#tag/Tasks/operation/update_task_api_v1_tasks__task_id__post) |

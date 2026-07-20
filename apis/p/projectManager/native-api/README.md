# ProjectManager: Native API Reference

A consolidated summary of ProjectManager's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.projectmanager.com/getting-started/authentication
- **OpenAPI specification:** https://developer.projectmanager.com/openapi.json
- **API base URL:** `https://api.projectmanager.com`

## Authentication

### API Key

Authenticate ProjectManager requests with a bearer API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.projectmanager.com/getting-started/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add TaskTag to Task](actions/add-task-tag-to-task.md) | `PUT /api/data/tasks/:taskId/tags` | [docs](https://developer.projectmanager.com/api-reference/task-tag/add-task-tag-to-task) |
| [Create Meeting](actions/create-meeting.md) | `POST /api/data/meetings` | [docs](https://developer.projectmanager.com/api-reference/meetings/create-meeting) |
| [Create Or Update TaskAssignee](actions/create-or-update-task-assignee.md) | `PUT /api/data/tasks/:taskId/assignees` | [docs](https://developer.projectmanager.com/api-reference/task-assignee/create-or-update-task-assignee) |
| [Create Project](actions/create-project.md) | `POST /api/data/projects` | [docs](https://developer.projectmanager.com/api-reference/project/create-project) |
| [Create Resource](actions/create-resource.md) | `POST /api/data/resources` | [docs](https://developer.projectmanager.com/api-reference/resource/create-resource) |
| [Create Tag](actions/create-tag.md) | `POST /api/data/tags` | [docs](https://developer.projectmanager.com/api-reference/tag/create-tag) |
| [Create Task](actions/create-task.md) | `POST /api/data/projects/:projectId/tasks` | [docs](https://developer.projectmanager.com/api-reference/task/create-task) |
| [Create Task Comment](actions/create-task-comment.md) | `POST /api/data/tasks/:taskId/comments` | [docs](https://developer.projectmanager.com/api-reference/discussion/create-task-comment) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/data/projects/:projectId` | [docs](https://developer.projectmanager.com/api-reference/project/delete-project) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/data/tasks/:taskId` | [docs](https://developer.projectmanager.com/api-reference/task/delete-task) |
| [Fetch the first level child tasks from the task](actions/fetch-the-first-level-child-tasks-from-the-task.md) | `GET /api/data/tasks/:taskId/subtasks` | [docs](https://developer.projectmanager.com/api-reference/task/fetch-the-first-level-child-tasks-from-the-task) |
| [Get Meeting](actions/get-meeting.md) | `GET /api/data/meetings/:meetingId` | [docs](https://developer.projectmanager.com/api-reference/meetings/get-meeting) |
| [Get Risk](actions/get-risk.md) | `GET /api/data/risks/:riskId` | [docs](https://developer.projectmanager.com/api-reference/risk/get-risk) |
| [Mark Notification Read](actions/mark-notification-read.md) | `POST /api/data/notifications/:id/markread` | [docs](https://developer.projectmanager.com/api-reference/notification/mark-notification-read) |
| [Query Projects](actions/query-projects.md) | `GET /api/data/projects` | [docs](https://developer.projectmanager.com/api-reference/project/query-projects) |
| [Query Resources](actions/query-resources.md) | `GET /api/data/resources` | [docs](https://developer.projectmanager.com/api-reference/resource/query-resources) |
| [Query Risks](actions/query-risks.md) | `GET /api/data/risks` | [docs](https://developer.projectmanager.com/api-reference/risk/query-risks) |
| [Query Tags](actions/query-tags.md) | `GET /api/data/tags` | [docs](https://developer.projectmanager.com/api-reference/tag/query-tags) |
| [Query Tasks](actions/query-tasks.md) | `GET /api/data/tasks` | [docs](https://developer.projectmanager.com/api-reference/task/query-tasks) |
| [Remove TaskTag from Task](actions/remove-task-tag-from-task.md) | `DELETE /api/data/tasks/:taskId/tags` | [docs](https://developer.projectmanager.com/api-reference/task-tag/remove-task-tag-from-task) |
| [Restore Project](actions/restore-project.md) | `PUT /api/data/projects/:projectId/restore` | [docs](https://developer.projectmanager.com/api-reference/project/restore-project) |
| [Retrieve Me](actions/retrieve-me.md) | `GET /api/data/me` | [docs](https://developer.projectmanager.com/api-reference/me/retrieve-me) |
| [Retrieve Notifications](actions/retrieve-notifications.md) | `GET /api/data/notifications` | [docs](https://developer.projectmanager.com/api-reference/notification/retrieve-notifications) |
| [Retrieve Project](actions/retrieve-project.md) | `GET /api/data/projects/:projectId` | [docs](https://developer.projectmanager.com/api-reference/project/retrieve-project) |
| [Retrieve Project Priorities](actions/retrieve-project-priorities.md) | `GET /api/data/projects/priorities` | [docs](https://developer.projectmanager.com/api-reference/project-priority/retrieve-project-priorities) |
| [Retrieve Project Templates](actions/retrieve-project-templates.md) | `GET /api/data/projects/templates` | [docs](https://developer.projectmanager.com/api-reference/project-template/retrieve-project-templates) |
| [Retrieve Resource](actions/retrieve-resource.md) | `GET /api/data/resources/:resourceId` | [docs](https://developer.projectmanager.com/api-reference/resource/retrieve-resource) |
| [Retrieve Task](actions/retrieve-task.md) | `GET /api/data/tasks/:taskId` | [docs](https://developer.projectmanager.com/api-reference/task/retrieve-task) |
| [Retrieve Task Comments](actions/retrieve-task-comments.md) | `GET /api/data/tasks/:taskId/comments` | [docs](https://developer.projectmanager.com/api-reference/discussion/retrieve-task-comments) |
| [Retrieve Task Priorities](actions/retrieve-task-priorities.md) | `GET /api/data/tasks/priorities` | [docs](https://developer.projectmanager.com/api-reference/task/retrieve-task-priorities) |
| [Retrieve TaskTags](actions/retrieve-task-tags.md) | `GET /api/data/tasks/:taskId/tags` | [docs](https://developer.projectmanager.com/api-reference/task-tag/retrieve-task-tags) |
| [Retrieve Workspaces](actions/retrieve-workspaces.md) | `GET /api/data/workspaces` | [docs](https://developer.projectmanager.com/api-reference/work-space/retrieve-workspaces) |
| [Returns task assignees](actions/returns-task-assignees.md) | `GET /api/data/tasks/:taskId/assignees` | [docs](https://developer.projectmanager.com/api-reference/task-assignee/returns-task-assignees) |
| [Unread Notification Count](actions/unread-notification-count.md) | `GET /api/data/notifications/unreadcount` | [docs](https://developer.projectmanager.com/api-reference/notification/unread-notification-count) |
| [Update Meeting](actions/update-meeting.md) | `PUT /api/data/meetings/:meetingId` | [docs](https://developer.projectmanager.com/api-reference/meetings/update-meeting) |
| [Update Project](actions/update-project.md) | `PUT /api/data/projects/:projectId` | [docs](https://developer.projectmanager.com/api-reference/project/update-project) |
| [Update Resource](actions/update-resource.md) | `PUT /api/data/resources/:resourceId` | [docs](https://developer.projectmanager.com/api-reference/resource/update-resource) |
| [Update Risk](actions/update-risk.md) | `PUT /api/data/risks/:riskId` | [docs](https://developer.projectmanager.com/api-reference/risk/update-risk) |
| [Update Tag](actions/update-tag.md) | `PUT /api/data/tags/:tagId` | [docs](https://developer.projectmanager.com/api-reference/tag/update-tag) |
| [Update Task](actions/update-task.md) | `PUT /api/data/tasks/:taskId` | [docs](https://developer.projectmanager.com/api-reference/task/update-task) |

# Rocketlane: Native API Reference

A consolidated summary of Rocketlane's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.rocketlane.com/reference
- **API base URL:** `https://api.rocketlane.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.rocketlane.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `pagination.nextPageToken`.

## Pagination

Use `pageSize` in the query string to set the page size (default 100; accepted range 1–100). Use `pageToken` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Conversation Members](actions/add-conversation-members.md) | `POST /1.0/conversations/:conversationId/add-members` | [docs](https://developer.rocketlane.com/reference/add-members-to-conversation) |
| [Add Project Members](actions/add-project-members.md) | `POST /1.0/projects/:projectId/add-members` | [docs](https://developer.rocketlane.com/reference/add-members) |
| [Add Task Assignees](actions/add-task-assignees.md) | `POST /1.0/tasks/:taskId/add-assignees` | [docs](https://developer.rocketlane.com/reference/add-assignee-to-task) |
| [Add Task Dependencies](actions/add-task-dependencies.md) | `POST /1.0/tasks/:taskId/add-dependencies` | [docs](https://developer.rocketlane.com/reference/add-dependencies-to-task) |
| [Archive Project](actions/archive-project.md) | `POST /1.0/projects/:projectId/archive` | [docs](https://developer.rocketlane.com/reference/archiveProject) |
| [Create Comment](actions/create-comment.md) | `POST /1.0/comments` | [docs](https://developer.rocketlane.com/reference/create-comment) |
| [Create Conversation](actions/create-conversation.md) | `POST /1.0/conversations` | [docs](https://developer.rocketlane.com/reference/create-conversation) |
| [Create Phase](actions/create-phase.md) | `POST /1.0/phases` | [docs](https://developer.rocketlane.com/reference/create-phase) |
| [Create Project](actions/create-project.md) | `POST /1.0/projects` | [docs](https://developer.rocketlane.com/reference/create-project) |
| [Create Task](actions/create-task.md) | `POST /1.0/tasks` | [docs](https://developer.rocketlane.com/reference/create-task) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /1.0/comments/:commentId` | [docs](https://developer.rocketlane.com/reference/delete-comment) |
| [Delete Phase](actions/delete-phase.md) | `DELETE /1.0/phases/:phaseId` | [docs](https://developer.rocketlane.com/reference/delete-phase) |
| [Delete Task](actions/delete-task.md) | `DELETE /1.0/tasks/:taskId` | [docs](https://developer.rocketlane.com/reference/delete-task) |
| [Get Comment](actions/get-comment.md) | `GET /1.0/comments/:commentId` | [docs](https://developer.rocketlane.com/reference/get-comment) |
| [Get Conversation](actions/get-conversation.md) | `GET /1.0/conversations/:conversationId` | [docs](https://developer.rocketlane.com/reference/get-conversation) |
| [Get Phase](actions/get-phase.md) | `GET /1.0/phases/:phaseId` | [docs](https://developer.rocketlane.com/reference/get-phase) |
| [Get Project](actions/get-project.md) | `GET /1.0/projects/:projectId` | [docs](https://developer.rocketlane.com/reference/get-project) |
| [Get Task](actions/get-task.md) | `GET /1.0/tasks/:taskId` | [docs](https://developer.rocketlane.com/reference/get-task) |
| [Get Time Entry](actions/get-time-entry.md) | `GET /1.0/time-entries/:timeEntryId` | [docs](https://developer.rocketlane.com/reference/get-time-entry) |
| [Get User](actions/get-user.md) | `GET /1.0/users/:userId` | [docs](https://developer.rocketlane.com/reference/get-user) |
| [Import Project Template](actions/import-project-template.md) | `POST /1.0/projects/:projectId/import-template` | [docs](https://developer.rocketlane.com/reference/import-template) |
| [List Comments](actions/list-comments.md) | `GET /1.0/comments` | [docs](https://developer.rocketlane.com/reference/get-comments) |
| [List Conversations](actions/list-conversations.md) | `GET /1.0/conversations` | [docs](https://developer.rocketlane.com/reference/get-all-conversations) |
| [List Invoices](actions/list-invoices.md) | `GET /1.0/invoices` | [docs](https://developer.rocketlane.com/reference/search-invoices) |
| [List Phases](actions/list-phases.md) | `GET /1.0/phases` | [docs](https://developer.rocketlane.com/reference/get-all-phases) |
| [List Projects](actions/list-projects.md) | `GET /1.0/projects` | [docs](https://developer.rocketlane.com/reference/get-all-projects) |
| [List Tasks](actions/list-tasks.md) | `GET /1.0/tasks` | [docs](https://developer.rocketlane.com/reference/get-all-tasks) |
| [List Time Entries](actions/list-time-entries.md) | `GET /1.0/time-entries` | [docs](https://developer.rocketlane.com/reference/get-all-time-entries) |
| [List Users](actions/list-users.md) | `GET /1.0/users` | [docs](https://developer.rocketlane.com/reference/get-all-users) |
| [Move Task To Phase](actions/move-task-to-phase.md) | `POST /1.0/tasks/:taskId/move-phase` | [docs](https://developer.rocketlane.com/reference/move-task-to-given-phase) |
| [Remove Conversation Members](actions/remove-conversation-members.md) | `POST /1.0/conversations/:conversationId/remove-members` | [docs](https://developer.rocketlane.com/reference/remove-members-from-conversation) |
| [Remove Project Members](actions/remove-project-members.md) | `POST /1.0/projects/:projectId/remove-members` | [docs](https://developer.rocketlane.com/reference/remove-members) |
| [Remove Task Assignees](actions/remove-task-assignees.md) | `POST /1.0/tasks/:taskId/remove-assignees` | [docs](https://developer.rocketlane.com/reference/remove-assignees-from-task) |
| [Remove Task Dependencies](actions/remove-task-dependencies.md) | `POST /1.0/tasks/:taskId/remove-dependencies` | [docs](https://developer.rocketlane.com/reference/remove-dependencies-from-task) |
| [Search Time Entries](actions/search-time-entries.md) | `GET /1.0/time-entries/search` | [docs](https://developer.rocketlane.com/reference/search-time-entries) |
| [Update Comment](actions/update-comment.md) | `PUT /1.0/comments/:commentId` | [docs](https://developer.rocketlane.com/reference/update-comment) |
| [Update Conversation](actions/update-conversation.md) | `PUT /1.0/conversations/:conversationId` | [docs](https://developer.rocketlane.com/reference/update-conversation) |
| [Update Phase](actions/update-phase.md) | `PUT /1.0/phases/:phaseId` | [docs](https://developer.rocketlane.com/reference/update-phase) |
| [Update Project](actions/update-project.md) | `PUT /1.0/projects/:projectId` | [docs](https://developer.rocketlane.com/reference/update-project) |
| [Update Task](actions/update-task.md) | `PUT /1.0/tasks/:taskId` | [docs](https://developer.rocketlane.com/reference/update-task) |

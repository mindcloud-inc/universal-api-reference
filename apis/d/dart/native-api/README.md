# Dart: Native API Reference

A consolidated summary of Dart's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://app.dartai.com/api/v0/public/docs/
- **OpenAPI specification:** https://app.dartai.com/api/v0/public/schema/
- **API base URL:** `https://app.dartai.com/api/v0/public`

## Authentication

### OAuth2

Connect to Dart using the official OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.dartai.com/api/oauth/authorize/ to approve access.
2. Exchange the returned authorization code with a POST request to https://app.dartai.com/api/oauth/token/.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `read write`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://app.dartai.com/api/oauth/token/.

[Official authentication documentation](https://help.dartai.com/en/articles/12618292-dart-oauth-integration-guide)

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `o` in the query string. Multiple sort fields can be combined.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Task Attachment From Url](actions/add-task-attachment-from-url.md) | `POST /tasks/:id/attachments/from-url` | [docs](https://app.dartai.com/api/v0/public/docs/#/Attachment/addTaskAttachmentFromUrl) |
| [Add Task Time Tracking Entry](actions/add-task-time-tracking-entry.md) | `POST /tasks/:id/time-tracking` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/addTaskTimeTracking) |
| [Create Doc](actions/create-doc.md) | `POST /docs` | [docs](https://app.dartai.com/api/v0/public/docs/#/Doc/createDoc) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/createTask) |
| [Create Task Comment](actions/create-task-comment.md) | `POST /comments` | [docs](https://app.dartai.com/api/v0/public/docs/#/Comment/addTaskComment) |
| [Delete Doc](actions/delete-doc.md) | `DELETE /docs/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Doc/deleteDoc) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/deleteTask) |
| [Get Dartboard](actions/get-dartboard.md) | `GET /dartboards/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Dartboard/getDartboard) |
| [Get Doc](actions/get-doc.md) | `GET /docs/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Doc/getDoc) |
| [Get Folder](actions/get-folder.md) | `GET /folders/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Folder/getFolder) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/getTask) |
| [Get User Space Configuration](actions/get-user-space-configuration.md) | `GET /config` | [docs](https://app.dartai.com/api/v0/public/docs/#/Config/getConfig) |
| [Get View](actions/get-view.md) | `GET /views/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/View/getView) |
| [List Docs](actions/list-docs.md) | `GET /docs/list` | [docs](https://app.dartai.com/api/v0/public/docs/#/Doc/listDocs) |
| [List Help Center Articles](actions/list-help-center-articles.md) | `GET /help-center-articles/list` | [docs](https://app.dartai.com/api/v0/public/docs/#/Help%20center%20article/listHelpCenterArticles) |
| [List Task Comments](actions/list-task-comments.md) | `GET /comments/list` | [docs](https://app.dartai.com/api/v0/public/docs/#/Comment/listComments) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks/list` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/listTasks) |
| [Move Task](actions/move-task.md) | `POST /tasks/:id/move` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/moveTask) |
| [Retrieve Skill by Title](actions/retrieve-skill-by-title.md) | `GET /skills/by-title` | [docs](https://app.dartai.com/api/v0/public/docs/#/Skill/retrieveSkillByTitle) |
| [Update Doc](actions/update-doc.md) | `PUT /docs/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Doc/updateDoc) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://app.dartai.com/api/v0/public/docs/#/Task/updateTask) |

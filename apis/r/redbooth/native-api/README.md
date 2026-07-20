# Redbooth: Native API Reference

A consolidated summary of Redbooth's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://redbooth.com/api/api-docs/
- **API base URL:** `https://redbooth.com/api/3`

## Authentication

### OAuth 2.0

Authenticate to Redbooth using OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://redbooth.com/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://redbooth.com/oauth2/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `all`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://redbooth.com/oauth2/token.

[Official authentication documentation](https://redbooth.com/api/authentication/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /comments` | [docs](https://redbooth.com/api/api-docs/#page:comments,header:comments-comment-list-post) |
| [Create Conversation](actions/create-conversation.md) | `POST /conversations` | [docs](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-list-post) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-list-post) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-list-post) |
| [Create Task List](actions/create-task-list.md) | `POST /task_lists` | [docs](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-list-post) |
| [Delete Conversation](actions/delete-conversation.md) | `DELETE /conversations/:id` | [docs](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-delete) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:id` | [docs](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-delete) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/:id` | [docs](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-delete) |
| [Delete Task List](actions/delete-task-list.md) | `DELETE /task_lists/:id` | [docs](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-delete) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/:id` | [docs](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-get) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-get) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-get) |
| [Get Task List](actions/get-task-list.md) | `GET /task_lists/:id` | [docs](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-get) |
| [Get User Information](actions/get-user-information.md) | `GET /me` | [docs](https://redbooth.com/api/api-docs/#page:user-information,header:user-information-user-information-get) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-list-get) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://redbooth.com/api/api-docs/#page:organizations,header:organizations-organization-list-get) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-list-get) |
| [List Task Lists](actions/list-task-lists.md) | `GET /task_lists` | [docs](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-list-get) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-list-get) |
| [Search](actions/search.md) | `GET /search` | [docs](https://redbooth.com/api/api-docs/#page:search,header:search-search-get) |
| [Update Conversation](actions/update-conversation.md) | `PUT /conversations/:id` | [docs](https://redbooth.com/api/api-docs/#page:conversations,header:conversations-conversation-put) |
| [Update Project](actions/update-project.md) | `PUT /projects/:id` | [docs](https://redbooth.com/api/api-docs/#page:projects,header:projects-project-put) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:id` | [docs](https://redbooth.com/api/api-docs/#page:tasks,header:tasks-task-put) |
| [Update Task List](actions/update-task-list.md) | `PUT /task_lists/:id` | [docs](https://redbooth.com/api/api-docs/#page:tasklists,header:tasklists-tasklist-put) |

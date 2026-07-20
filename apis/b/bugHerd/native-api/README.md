# BugHerd: Native API Reference

A consolidated summary of BugHerd's API configuration and 37 documented operations, with links to official documentation.

- **Official docs:** https://docs.bugherd.com/api
- **API base URL:** `https://www.bugherd.com/api_v2`

## Authentication

### API Key

Authenticate with your BugHerd organization API key using HTTP Basic auth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.bugherd.com/api_v2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (37 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Project Client](actions/add-project-client.md) | `POST projects/:project_id/add_guest.json` | [docs](https://docs.bugherd.com/api) |
| [Add Project Member](actions/add-project-member.md) | `POST projects/:project_id/add_member.json` | [docs](https://docs.bugherd.com/api) |
| [Create Attachment From URL](actions/create-attachment-from-url.md) | `POST projects/:project_id/tasks/:task_id/attachments.json` | [docs](https://docs.bugherd.com/api) |
| [Create Column](actions/create-column.md) | `POST projects/:project_id/columns.json` | [docs](https://docs.bugherd.com/api) |
| [Create Comment](actions/create-comment.md) | `POST projects/:project_id/tasks/:task_id/comments.json` | [docs](https://docs.bugherd.com/api) |
| [Create Project](actions/create-project.md) | `POST projects.json` | [docs](https://docs.bugherd.com/api) |
| [Create Task](actions/create-task.md) | `POST projects/:project_id/tasks.json` | [docs](https://docs.bugherd.com/api) |
| [Create Webhook](actions/create-webhook.md) | `POST webhooks.json` | [docs](https://docs.bugherd.com/api) |
| [Delete Attachment](actions/delete-attachment.md) | `DELETE projects/:project_id/tasks/:task_id/attachments/:id.json` | [docs](https://docs.bugherd.com/api) |
| [Delete Project](actions/delete-project.md) | `DELETE projects/:project_id.json` | [docs](https://docs.bugherd.com/api) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE webhooks/:id.json` | [docs](https://docs.bugherd.com/api) |
| [List Active Projects](actions/list-active-projects.md) | `GET projects/active.json` | [docs](https://docs.bugherd.com/api) |
| [List Archived Tasks](actions/list-archived-tasks.md) | `GET projects/:project_id/tasks/archive.json` | [docs](https://docs.bugherd.com/api) |
| [List Attachments](actions/list-attachments.md) | `GET projects/:project_id/tasks/:task_id/attachments.json` | [docs](https://docs.bugherd.com/api) |
| [List Clients](actions/list-clients.md) | `GET users/guests.json` | [docs](https://docs.bugherd.com/api) |
| [List Columns](actions/list-columns.md) | `GET projects/:project_id/columns.json` | [docs](https://docs.bugherd.com/api) |
| [List Comments](actions/list-comments.md) | `GET projects/:project_id/tasks/:task_id/comments.json` | [docs](https://docs.bugherd.com/api) |
| [List Feedback Tasks](actions/list-feedback-tasks.md) | `GET projects/:project_id/tasks/feedback.json` | [docs](https://docs.bugherd.com/api) |
| [List Members](actions/list-members.md) | `GET users/members.json` | [docs](https://docs.bugherd.com/api) |
| [List Projects](actions/list-projects.md) | `GET projects.json` | [docs](https://docs.bugherd.com/api) |
| [List Taskboard Tasks](actions/list-taskboard-tasks.md) | `GET projects/:project_id/tasks/taskboard.json` | [docs](https://docs.bugherd.com/api) |
| [List Tasks](actions/list-tasks.md) | `GET projects/:project_id/tasks.json` | [docs](https://docs.bugherd.com/api) |
| [List User Projects](actions/list-user-projects.md) | `GET users/:user_id/projects.json` | [docs](https://docs.bugherd.com/api) |
| [List User Tasks](actions/list-user-tasks.md) | `GET users/:user_id/tasks.json` | [docs](https://docs.bugherd.com/api) |
| [List Users](actions/list-users.md) | `GET users.json` | [docs](https://docs.bugherd.com/api) |
| [List Webhooks](actions/list-webhooks.md) | `GET webhooks.json` | [docs](https://docs.bugherd.com/api) |
| [Show Attachment](actions/show-attachment.md) | `GET projects/:project_id/tasks/:task_id/attachments/:id.json` | [docs](https://docs.bugherd.com/api) |
| [Show Column](actions/show-column.md) | `GET projects/:project_id/columns/:column_id.json` | [docs](https://docs.bugherd.com/api) |
| [Show Organization](actions/show-organization.md) | `GET organization.json` | [docs](https://docs.bugherd.com/api) |
| [Show Project](actions/show-project.md) | `GET projects/:project_id.json` | [docs](https://docs.bugherd.com/api) |
| [Show Task By Global ID](actions/show-task-by-global-id.md) | `GET tasks/:task_id.json` | [docs](https://docs.bugherd.com/api) |
| [Show Task By Local Task ID](actions/show-task-by-local-task-id.md) | `GET projects/:project_id/local_tasks/:local_task_id.json` | [docs](https://docs.bugherd.com/api) |
| [Show Task By Project ID](actions/show-task-by-project-id.md) | `GET projects/:project_id/tasks/:task_id.json` | [docs](https://docs.bugherd.com/api) |
| [Update Column](actions/update-column.md) | `PUT projects/:project_id/columns/:column_id.json` | [docs](https://docs.bugherd.com/api) |
| [Update Project](actions/update-project.md) | `PUT projects/:project_id.json` | [docs](https://docs.bugherd.com/api) |
| [Update Task](actions/update-task.md) | `PUT projects/:project_id/tasks/:task_id.json` | [docs](https://docs.bugherd.com/api) |
| [Upload Attachment](actions/upload-attachment.md) | `POST projects/:project_id/tasks/:task_id/attachments/upload` | [docs](https://docs.bugherd.com/api) |

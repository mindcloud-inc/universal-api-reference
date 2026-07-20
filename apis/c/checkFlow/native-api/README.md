# CheckFlow: Native API Reference

A consolidated summary of CheckFlow's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://docs.checkflow.io/docs/api/overview
- **OpenAPI specification:** https://app.checkflow.io/swagger/v2/swagger.json
- **API base URL:** `https://app.checkflow.io`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://docs.checkflow.io/docs/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `X-API-VERSION` | `2.0` |

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 3). Use `pageNumber` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Task Assignees by Name](actions/add-task-assignees-by-name.md) | `POST /api/task/assign-by-name` | [docs](https://docs.checkflow.io/docs/api/tasks#add-task-assignees-by-name) |
| [Assign Tag To Checklist Or Task](actions/assign-tag-to-checklist-or-task.md) | `POST /api/tag/assignment` | [docs](https://docs.checkflow.io/docs/api/tags#assign-tag) |
| [Create Checklist](actions/create-checklist.md) | `POST /api/checklist` | [docs](https://docs.checkflow.io/docs/api/checklists#create-checklist) |
| [Create Checklist With Parameters](actions/create-checklist-with-parameters.md) | `POST /api/checklist/create-with-parameters` | [docs](https://docs.checkflow.io/docs/api/checklists#create-checklist-with-parameters) |
| [Create Many Checklists](actions/create-many-checklists.md) | `POST /api/checklist/create-many` | [docs](https://docs.checkflow.io/docs/api/checklists#create-many-checklists) |
| [Create Tag](actions/create-tag.md) | `POST /api/tag` | [docs](https://docs.checkflow.io/docs/api/tags#create-tag) |
| [Create Task Comment](actions/create-task-comment.md) | `POST /api/task/comment` | [docs](https://docs.checkflow.io/docs/api/tasks#create-task-comment) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /api/web-hook/subscribe` | [docs](https://docs.checkflow.io/docs/api/webhooks#create-webhook-subscription) |
| [Delete Checklist](actions/delete-checklist.md) | `DELETE /api/checklist` | [docs](https://docs.checkflow.io/docs/api/checklists#delete-checklist) |
| [Delete Many Checklists](actions/delete-many-checklists.md) | `DELETE /api/checklist/delete-many` | [docs](https://docs.checkflow.io/docs/api/checklists#delete-many-checklists) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /api/tag` | [docs](https://docs.checkflow.io/docs/api/tags#delete-tag) |
| [Delete Task Assignments](actions/delete-task-assignments.md) | `DELETE /api/task/assignments` | [docs](https://docs.checkflow.io/docs/api/tasks#delete-task-assignments) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /api/web-hook/unsubscribe` | [docs](https://docs.checkflow.io/docs/api/webhooks#delete-webhook-subscription) |
| [Find Checklists](actions/find-checklists.md) | `GET /api/checklist/find` | [docs](https://docs.checkflow.io/docs/api/checklists#find-checklists) |
| [Get Analytics](actions/get-analytics.md) | `GET /api/analytics/all` | [docs](https://docs.checkflow.io/docs/api/analytics#get-analytics) |
| [Get Checklist Details](actions/get-checklist-details.md) | `GET /api/checklist/details` | [docs](https://docs.checkflow.io/docs/api/checklists#get-checklist-details) |
| [Get Task Details](actions/get-task-details.md) | `GET /api/task/details` | [docs](https://docs.checkflow.io/docs/api/tasks#get-task-details) |
| [Get Uploaded Checklist Files](actions/get-uploaded-checklist-files.md) | `GET /api/checklist/uploaded-files` | [docs](https://docs.checkflow.io/docs/api/checklists#get-uploaded-files) |
| [List Tags](actions/list-tags.md) | `GET /api/tag/tags` | [docs](https://docs.checkflow.io/docs/api/tags#list-tags) |
| [List Task Assignments](actions/list-task-assignments.md) | `GET /api/task/assignments` | [docs](https://docs.checkflow.io/docs/api/tasks#get-task-assignments) |
| [List Task Controls](actions/list-task-controls.md) | `GET /api/template/task-content` | [docs](https://docs.checkflow.io/docs/api/templates#list-task-controls) |
| [List Tasks by Task Key](actions/list-tasks-by-task-key.md) | `GET /api/checklist/tasks` | [docs](https://docs.checkflow.io/docs/api/checklists#get-tasks-by-task-key) |
| [List Team Groups](actions/list-team-groups.md) | `GET /api/team/groups` | [docs](https://docs.checkflow.io/docs/api/team#get-groups) |
| [List Team Members](actions/list-team-members.md) | `GET /api/team/members` | [docs](https://docs.checkflow.io/docs/api/team#get-members) |
| [List Team Members And Groups](actions/list-team-members-and-groups.md) | `GET /api/team/members-and-groups` | [docs](https://docs.checkflow.io/docs/api/team#get-members-and-groups) |
| [List Template Tasks](actions/list-template-tasks.md) | `GET /api/template/tasks` | [docs](https://docs.checkflow.io/docs/api/templates#list-template-tasks) |
| [List Templates](actions/list-templates.md) | `GET /api/template/templates` | [docs](https://docs.checkflow.io/docs/api/templates#list-templates) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /api/web-hook/subscriptions` | [docs](https://docs.checkflow.io/docs/api/webhooks#list-webhook-subscriptions) |
| [Remove Tag Assignment](actions/remove-tag-assignment.md) | `DELETE /api/tag/assignment` | [docs](https://docs.checkflow.io/docs/api/tags#remove-tag-assignment) |
| [Share Checklist](actions/share-checklist.md) | `POST /api/checklist/share` | [docs](https://docs.checkflow.io/docs/api/checklists#share-checklist) |
| [Update Task Assignments](actions/update-task-assignments.md) | `PUT /api/task/assignments` | [docs](https://docs.checkflow.io/docs/api/tasks#update-task-assignments) |
| [Update Task Control Value](actions/update-task-control-value.md) | `PUT /api/task/update-task-content` | [docs](https://docs.checkflow.io/docs/api/tasks#update-task-control-value) |
| [Update Task Status](actions/update-task-status.md) | `PUT /api/task/status` | [docs](https://docs.checkflow.io/docs/api/tasks#update-task-status) |
| [Validate API Key](actions/validate-api-key.md) | `GET /api/authentication/validate` | [docs](https://docs.checkflow.io/docs/api/authentication#validate-api-key) |

# ClickUp: Native API Reference

A consolidated summary of ClickUp's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://developer.clickup.com/reference/
- **OpenAPI specification:** https://developer.clickup.com/openapi/clickup-api-v2-reference.json
- **API base URL:** `https://api.clickup.com/api/v2/`

## Authentication

### OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.clickup.com/api to approve access.
2. Exchange the returned authorization code with a POST request to https://api.clickup.com/api/v2/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://clickup.com/api/developer-portal/authentication#oauth-flow)

### API token

### Credentials

- **API Key:** `apiKey` · optional

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://developer.clickup.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `reverse`. Use `false` for ascending order and `true` for descending order. Only one sort field is accepted.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create List](actions/create-list.md) | `POST folder/:folder_id/list` | [docs](https://developer.clickup.com/reference/createlist) |
| [Create List From Template](actions/create-list-from-template.md) | `POST folder/:folder_id/list_template/:template_id` | [docs](https://developer.clickup.com/reference/createfolderlistfromtemplate) |
| [Create List View](actions/create-list-view.md) | `POST list/:list_id/view` | [docs](https://developer.clickup.com/reference/createlist) |
| [Create Task](actions/create-task.md) | `POST list/:list_id/task` | [docs](https://developer.clickup.com/reference/createtask) |
| [Create Task Attachment](actions/create-task-attachment.md) | `POST task/:task_id/attachment` | [docs](https://developer.clickup.com/reference/createtaskattachment) |
| [Create Task From Template](actions/create-task-from-template.md) | `POST list/:list_id/taskTemplate/:template_id` | [docs](https://developer.clickup.com/reference/createtaskfromtemplate) |
| [Create Webhook](actions/create-webhook.md) | `POST team/:team_id/webhook` | [docs](https://developer.clickup.com/reference/createwebhook) |
| [Delete Task](actions/delete-task.md) | `DELETE task/:task_id` | [docs](https://developer.clickup.com/reference/deletetask) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE webhook/:webhook_id` | [docs](https://developer.clickup.com/reference/getwebhooks) |
| [Get List](actions/get-list.md) | `GET list/:list_id` | [docs](https://developer.clickup.com/reference/getlist) |
| [Get Task](actions/get-task.md) | `GET task/:task_id` | [docs](https://developer.clickup.com/reference/gettask) |
| [Get User](actions/get-user.md) | `GET team/:team_id/user/:user_id` | [docs](https://developer.clickup.com/reference/getuser) |
| [Get View Tasks](actions/get-view-tasks.md) | `GET view/:view_id/task` | [docs](https://developer.clickup.com/reference/createlist) |
| [List Authorized Workspaces](actions/list-authorized-workspaces.md) | `GET team` | [docs](https://developer.clickup.com/reference/getauthorizedteams) |
| [List Filtered Team Tasks](actions/list-filtered-team-tasks.md) | `GET team/:team_Id/task` | [docs](https://developer.clickup.com/reference/getfilteredteamtasks) |
| [List Folderless Lists](actions/list-folderless-lists.md) | `GET space/:space_id/list` | [docs](https://developer.clickup.com/reference/getfolderlesslists) |
| [List Folders](actions/list-folders.md) | `GET space/:space_id/folder` | [docs](https://developer.clickup.com/reference/getfolders) |
| [List List Custom Fields](actions/list-list-custom-fields.md) | `GET list/:list_id/field` | [docs](https://developer.clickup.com/reference/getaccessiblecustomfields) |
| [List Lists](actions/list-lists.md) | `GET folder/:folder_id/list` | [docs](https://developer.clickup.com/reference/getlists) |
| [List Spaces](actions/list-spaces.md) | `GET team/:team_id/space` | [docs](https://developer.clickup.com/reference/getspaces) |
| [List Task Templates](actions/list-task-templates.md) | `GET team/:team_id/taskTemplate` | [docs](https://developer.clickup.com/reference/gettasktemplates) |
| [List Tasks](actions/list-tasks.md) | `GET list/:list_id/task` | [docs](https://developer.clickup.com/reference/gettasks) |
| [List Webhook](actions/list-webhook.md) | `GET team/:team_id/webhook` | [docs](https://developer.clickup.com/reference/getwebhooks) |
| [Remove Custom Field Value](actions/remove-custom-field-value.md) | `DELETE task/:task_id/field/:field_id` | [docs](https://developer.clickup.com/reference/removecustomfieldvalue) |
| [Search Workspace Docs](actions/search-workspace-docs.md) | `GET https://api.clickup.com/api/v3/workspaces/:workspace_id/docs` | [docs](https://developer.clickup.com/reference/searchdocspublic) |
| [Set Custom Field Value](actions/set-custom-field-value.md) | `POST task/:task_id/field/:field_id` | [docs](https://developer.clickup.com/reference/setcustomfieldvalue) |
| [Update Task](actions/update-task.md) | `PUT task/:task_id` | [docs](https://developer.clickup.com/reference/updatetask) |
| [Update Webhook](actions/update-webhook.md) | `PUT webhook/:webhook_id` | [docs](https://developer.clickup.com/reference/getwebhooks) |

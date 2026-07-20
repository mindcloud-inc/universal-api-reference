# Checkvist: Native API Reference

A consolidated summary of Checkvist's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://checkvist.com/auth/api
- **API base URL:** `https://checkvist.com`

## Authentication

### Basic Auth

Authenticate with your Checkvist email or username and Remote API key.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://checkvist.com/auth/api)

### API Token

Authenticate with a Checkvist API token obtained from the login endpoint and send it in the X-Client-Token header.

### Credentials

- **API token:** `token` · required · A current Checkvist API token from /auth/login.json?version=2.

Send these headers with each API request:

```http
X-Client-Token: <token>
```

[Official authentication documentation](https://checkvist.com/auth/api)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Change Task Status](actions/change-task-status.md) | `POST /checklists/:checklistId/tasks/:taskId/:action.json` | [docs](https://checkvist.com/auth/api#list_items_status) |
| [Create Checklist](actions/create-checklist.md) | `POST /checklists.json` | [docs](https://checkvist.com/auth/api) |
| [Create Task](actions/create-task.md) | `POST /checklists/:checklistId/tasks.json` | [docs](https://checkvist.com/auth/api#list_items_create) |
| [Create Task Note](actions/create-task-note.md) | `POST /checklists/:checklistId/tasks/:taskId/comments.json` | [docs](https://checkvist.com/auth/api) |
| [Delete Checklist](actions/delete-checklist.md) | `DELETE /checklists/:checklistId.json` | [docs](https://checkvist.com/auth/api) |
| [Delete Task](actions/delete-task.md) | `DELETE /checklists/:checklistId/tasks/:taskId.json` | [docs](https://checkvist.com/auth/api#list_items) |
| [Delete Task Note](actions/delete-task-note.md) | `DELETE /checklists/:checklistId/tasks/:taskId/comments/:noteId.json` | [docs](https://checkvist.com/auth/api) |
| [Get Checklist](actions/get-checklist.md) | `GET /checklists/:checklistId.json` | [docs](https://checkvist.com/auth/api) |
| [Get Current User](actions/get-current-user.md) | `GET /auth/curr_user.json` | [docs](https://checkvist.com/auth/api) |
| [Get Task](actions/get-task.md) | `GET /checklists/:checklistId/tasks/:taskId.json` | [docs](https://checkvist.com/auth/api#list_items) |
| [Import Tasks](actions/import-tasks.md) | `POST /checklists/:checklistId/import.json` | [docs](https://checkvist.com/auth/api#list_items_create) |
| [List Checklists](actions/list-checklists.md) | `GET /checklists.json` | [docs](https://checkvist.com/auth/api) |
| [List Task Notes](actions/list-task-notes.md) | `GET /checklists/:checklistId/tasks/:taskId/comments.json` | [docs](https://checkvist.com/auth/api) |
| [List Tasks](actions/list-tasks.md) | `GET /checklists/:checklistId/tasks.json` | [docs](https://checkvist.com/auth/api#list_items) |
| [Set Repeating Task](actions/set-repeating-task.md) | `POST /checklists/:checklistId/tasks/:taskId/repeat.json` | [docs](https://checkvist.com/auth/api#list_items) |
| [Update Checklist](actions/update-checklist.md) | `PUT /checklists/:checklistId.json` | [docs](https://checkvist.com/auth/api) |
| [Update Task](actions/update-task.md) | `PUT /checklists/:checklistId/tasks/:taskId.json` | [docs](https://checkvist.com/auth/api#list_items_update) |
| [Update Task Note](actions/update-task-note.md) | `PUT /checklists/:checklistId/tasks/:taskId/comments/:noteId.json` | [docs](https://checkvist.com/auth/api) |

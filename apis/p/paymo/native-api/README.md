# Paymo: Native API Reference

A consolidated summary of Paymo's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://github.com/paymo-org/api
- **API base URL:** `https://app.paymoapp.com/api/`

## Authentication

### API Key (Basic Auth)

Authenticate with a Paymo API key over HTTP Basic Auth. In MindCloud, put the Paymo API key in the Username field and use `x` as the Password placeholder, per Paymo's API authentication guide.

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

[Official authentication documentation](https://github.com/paymo-org/api/blob/master/sections/authentication.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST clients` | [docs](https://github.com/paymo-org/api/blob/master/sections/clients.md#creating-a-client) |
| [Create Project](actions/create-project.md) | `POST projects` | [docs](https://github.com/paymo-org/api/blob/master/sections/projects.md#creating-a-project) |
| [Create Task](actions/create-task.md) | `POST tasks` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasks.md#creating-a-task) |
| [Create Task List](actions/create-task-list.md) | `POST tasklists` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#creating-a-task-list) |
| [Create Time Entry](actions/create-time-entry.md) | `POST entries` | [docs](https://github.com/paymo-org/api/blob/master/sections/entries.md#creating-a-time-entry) |
| [Get Client](actions/get-client.md) | `GET clients/:clientId` | [docs](https://github.com/paymo-org/api/blob/master/sections/clients.md#getting-a-client) |
| [Get Project](actions/get-project.md) | `GET projects/:projectId` | [docs](https://github.com/paymo-org/api/blob/master/sections/projects.md#getting-a-project) |
| [Get Task](actions/get-task.md) | `GET tasks/:taskId` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasks.md#getting-a-task) |
| [Get Task List](actions/get-task-list.md) | `GET tasklists/:tasklistId` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#getting-a-task-list) |
| [Get Time Entry](actions/get-time-entry.md) | `GET entries/:entryId` | [docs](https://github.com/paymo-org/api/blob/master/sections/entries.md#getting-a-time-entry) |
| [List Clients](actions/list-clients.md) | `GET clients` | [docs](https://github.com/paymo-org/api/blob/master/sections/clients.md#getting-clients) |
| [List Projects](actions/list-projects.md) | `GET projects` | [docs](https://github.com/paymo-org/api/blob/master/sections/projects.md#getting-projects) |
| [List Task Lists](actions/list-task-lists.md) | `GET tasklists` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#getting-task-lists) |
| [List Tasks](actions/list-tasks.md) | `GET tasks` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasks.md#getting-tasks) |
| [List Time Entries](actions/list-time-entries.md) | `GET entries` | [docs](https://github.com/paymo-org/api/blob/master/sections/entries.md#getting-time-entries) |
| [Update Client](actions/update-client.md) | `PUT clients/:clientId` | [docs](https://github.com/paymo-org/api/blob/master/sections/clients.md#updating-a-client) |
| [Update Project](actions/update-project.md) | `PUT projects/:projectId` | [docs](https://github.com/paymo-org/api/blob/master/sections/projects.md#updating-a-project) |
| [Update Task](actions/update-task.md) | `PUT tasks/:taskId` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasks.md#updating-a-task) |
| [Update Task List](actions/update-task-list.md) | `PUT tasklists/:tasklistId` | [docs](https://github.com/paymo-org/api/blob/master/sections/tasklists.md#updating-a-task-list) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT entries/:entryId` | [docs](https://github.com/paymo-org/api/blob/master/sections/entries.md#updating-a-time-entry) |

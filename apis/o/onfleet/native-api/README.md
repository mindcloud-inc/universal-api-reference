# Onfleet: Native API Reference

A consolidated summary of Onfleet's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.onfleet.com/reference
- **API base URL:** `https://onfleet.com/api/v2`

## Authentication

### Basic Auth

Connect with your Onfleet API key as the username and leave the password blank

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

[Official authentication documentation](https://docs.onfleet.com/reference/authentication)

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Auto-Assign Tasks](actions/auto-assign-tasks.md) | `POST /tasks/autoAssign` | [docs](https://docs.onfleet.com/reference/automatically-assign-list-of-tasks) |
| [Create Destination](actions/create-destination.md) | `POST /destinations` | [docs](https://docs.onfleet.com/reference/create-destination) |
| [Create Recipient](actions/create-recipient.md) | `POST /recipients` | [docs](https://docs.onfleet.com/reference/create-recipient) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://docs.onfleet.com/reference/create-task) |
| [Create Team](actions/create-team.md) | `POST /teams` | [docs](https://docs.onfleet.com/reference/create-team) |
| [Create Worker](actions/create-worker.md) | `POST /workers` | [docs](https://docs.onfleet.com/reference/create-worker) |
| [Find Recipient](actions/find-recipient.md) | `GET /recipients/:lookupType/:lookupValue` | [docs](https://docs.onfleet.com/reference/find-recipient) |
| [Get Destination](actions/get-destination.md) | `GET /destinations/:destinationId` | [docs](https://docs.onfleet.com/reference/get-single-destination) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /organization` | [docs](https://docs.onfleet.com/reference/get-details) |
| [Get Recipient](actions/get-recipient.md) | `GET /recipients/:recipientId` | [docs](https://docs.onfleet.com/reference/get-single-recipient) |
| [Get Task](actions/get-task.md) | `GET /tasks/:taskId` | [docs](https://docs.onfleet.com/reference/get-single-task) |
| [Get Team](actions/get-team.md) | `GET /teams/:teamId` | [docs](https://docs.onfleet.com/reference/get-single-team) |
| [Get Worker](actions/get-worker.md) | `GET /workers/:workerId` | [docs](https://docs.onfleet.com/reference/get-single-worker) |
| [Get Workers By Location](actions/get-workers-by-location.md) | `GET /workers/location` | [docs](https://docs.onfleet.com/reference/get-workers-by-location) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://docs.onfleet.com/reference/list-tasks) |
| [List Team Tasks](actions/list-team-tasks.md) | `GET /teams/:teamId/tasks` | [docs](https://docs.onfleet.com/reference/list-tasks-in-team) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://docs.onfleet.com/reference/list-teams) |
| [List Worker Tasks](actions/list-worker-tasks.md) | `GET /workers/:workerId/tasks` | [docs](https://docs.onfleet.com/reference/list-workers-assigned-tasks) |
| [List Workers](actions/list-workers.md) | `GET /workers` | [docs](https://docs.onfleet.com/reference/list-workers) |
| [Test API Key](actions/test-api-key.md) | `GET /auth/test` | [docs](https://docs.onfleet.com/reference/testing-your-api-key) |
| [Update Recipient](actions/update-recipient.md) | `PUT /recipients/:recipientId` | [docs](https://docs.onfleet.com/reference/update-recipient) |
| [Update Task](actions/update-task.md) | `PUT /tasks/:taskId` | [docs](https://docs.onfleet.com/reference/update-task) |
| [Update Team](actions/update-team.md) | `PUT /teams/:teamId` | [docs](https://docs.onfleet.com/reference/update-team) |
| [Update Worker](actions/update-worker.md) | `PUT /workers/:workerId` | [docs](https://docs.onfleet.com/reference/update-worker) |

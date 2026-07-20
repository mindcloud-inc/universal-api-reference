# TeamBook: Native API Reference

A consolidated summary of TeamBook's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://kb.teambookapp.com/en/article/teambook-api
- **OpenAPI specification:** https://docs.teambook.apiary.io/
- **API base URL:** `https://web.teambookapp.com/api/public`

## Authentication

### API Key

Admin-generated TeamBook API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://kb.teambookapp.com/en/article/teambook-api)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Actual Logs](actions/create-actual-logs.md) | `POST /actual_logs` | [docs](https://kb.teambookapp.com/en/article/export-records) |
| [Create Booking](actions/create-booking.md) | `POST /bookings` | [docs](https://kb.teambookapp.com/en/article/create-bookings) |
| [Create Client](actions/create-client.md) | `POST /clients` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-clients) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-projects) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://kb.teambookapp.com/en/article/define-tasks) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://kb.teambookapp.com/en/article/create-users) |
| [Delete Booking](actions/delete-booking.md) | `DELETE /bookings/{bookingId}` | [docs](https://kb.teambookapp.com/en/article/delete-bookings) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/{projectId}` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-projects) |
| [Delete Task](actions/delete-task.md) | `DELETE /tasks/{taskId}` | [docs](https://kb.teambookapp.com/en/article/define-tasks) |
| [Delete User](actions/delete-user.md) | `DELETE /users/{userId}` | [docs](https://kb.teambookapp.com/en/article/create-users) |
| [Get Booking](actions/get-booking.md) | `GET /bookings/{bookingId}` | [docs](https://kb.teambookapp.com/en/article/teambook-api) |
| [Get Client](actions/get-client.md) | `GET /clients/{clientId}` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-clients) |
| [Get Project](actions/get-project.md) | `GET /projects/{projectId}` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-projects) |
| [Get Task](actions/get-task.md) | `GET /tasks/{taskId}` | [docs](https://kb.teambookapp.com/en/article/define-tasks) |
| [Get Team](actions/get-team.md) | `GET /teams/{teamId}` | [docs](https://kb.teambookapp.com/en/article/teams-why-and-how-to-use) |
| [Get User](actions/get-user.md) | `GET /users/{userId}` | [docs](https://kb.teambookapp.com/en/article/create-users) |
| [List Actual Logs](actions/list-actual-logs.md) | `GET /actual_logs` | [docs](https://kb.teambookapp.com/en/article/export-records) |
| [List Bookings](actions/list-bookings.md) | `GET /bookings` | [docs](https://kb.teambookapp.com/en/article/teambook-api) |
| [List Clients](actions/list-clients.md) | `GET /clients` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-clients) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://kb.teambookapp.com/en/article/create-and-edit-projects) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://kb.teambookapp.com/en/article/define-tasks) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://kb.teambookapp.com/en/article/teams-why-and-how-to-use) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://kb.teambookapp.com/en/article/create-users) |

# Testomato: Native API Reference

A consolidated summary of Testomato's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://help.testomato.com/api/testomato-api
- **API base URL:** `https://testomato.com/api`

## Authentication

### Bearer JWT

Bearer JWT API token auth for the Testomato REST API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.testomato.com/api/get-api-token)

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add user to project](actions/add-user-to-project.md) | `POST /project/:id/users` | [docs](https://help.testomato.com/api/add-user-to-project) |
| [Get API token](actions/get-api-token.md) | `POST /authenticate` | [docs](https://help.testomato.com/api/get-api-token) |
| [Get project](actions/get-project.md) | `GET /project/:id` | [docs](https://help.testomato.com/api/get-project) |
| [Get test](actions/get-test.md) | `GET /tests/:id` | [docs](https://help.testomato.com/api/get-test) |
| [New project](actions/new-project.md) | `POST /project/create` | [docs](https://help.testomato.com/api/new-project) |
| [Project delete](actions/project-delete.md) | `DELETE /project/:id` | [docs](https://help.testomato.com/api/project-delete) |
| [Project groups](actions/project-groups.md) | `GET /project/:id/areas` | [docs](https://help.testomato.com/api/project-groups) |
| [Project notifications](actions/project-notifications.md) | `GET /project/:id/notifications` | [docs](https://help.testomato.com/api/project-notifications) |
| [Project permissions](actions/project-permissions.md) | `GET /project/:id/permissions` | [docs](https://help.testomato.com/api/project-permissions) |
| [Project results](actions/project-results.md) | `GET /project/:ProjectId/job/:JobId/results` | [docs](https://help.testomato.com/api/project-results) |
| [Project roles](actions/project-roles.md) | `GET /project/:id/roles` | [docs](https://help.testomato.com/api/project-roles) |
| [Project status](actions/project-status.md) | `GET /project/:id/status` | [docs](https://help.testomato.com/api/project-status) |
| [Project update](actions/project-update.md) | `PUT /project/:id` | [docs](https://help.testomato.com/api/project-update) |
| [Project users](actions/project-users.md) | `GET /project/:id/users` | [docs](https://help.testomato.com/api/project-users) |
| [Response times](actions/response-times.md) | `GET /project/:id/responseTimes` | [docs](https://help.testomato.com/api/response-times) |
| [Simplified project status](actions/simplified-project-status.md) | `GET /project/:id/simple-status` | [docs](https://help.testomato.com/api/simplified-project-status) |
| [Start project group](actions/start-project-group.md) | `GET /project/:ProjectId/start/area/:AreaId` | [docs](https://help.testomato.com/api/start-project-group) |
| [Starting project](actions/starting-project.md) | `GET /project/:id/start` | [docs](https://help.testomato.com/api/starting-project) |
| [Update notifications](actions/update-notifications.md) | `POST /project/:id/notifications` | [docs](https://help.testomato.com/api/update-notifications) |
| [Uptime](actions/uptime.md) | `GET /project/:id/uptime` | [docs](https://help.testomato.com/api/uptime) |
| [Verify API token](actions/verify-api-token.md) | `GET /authenticate` | [docs](https://help.testomato.com/api/verify-api-token) |

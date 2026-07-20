# Time Doctor: Native API Reference

A consolidated summary of Time Doctor's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api2.timedoctor.com/
- **OpenAPI specification:** https://api2.timedoctor.com/spec/
- **API base URL:** `https://api2.timedoctor.com`

## Authentication

### JWT Token

Use a valid Time Doctor JWT token plus the target company or workspace ID.

### Credentials

- **JWT Token:** `token` · required · Valid Time Doctor JWT token used as Authorization: JWT {token}.
- **Company ID:** `companyId` · required · Time Doctor company or workspace ID used by most endpoints.

[Official authentication documentation](https://api2.timedoctor.com/#operation/login)

## API conventions

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–200). Use `page` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | `POST /api/1.0/projects` | [docs](https://api2.timedoctor.com/#operation/createProject) |
| [Create Task](actions/create-task.md) | `POST /api/1.0/tasks` | [docs](https://api2.timedoctor.com/#operation/createTask) |
| [Delete Project](actions/delete-project.md) | `DELETE /api/1.0/projects/:projectId` | [docs](https://api2.timedoctor.com/#operation/deleteProject) |
| [Delete Task](actions/delete-task.md) | `DELETE /api/1.0/tasks/:taskId` | [docs](https://api2.timedoctor.com/#operation/deleteTask) |
| [Get Authorization](actions/get-authorization.md) | `GET /api/1.0/authorization` | [docs](https://api2.timedoctor.com/#operation/authorization) |
| [Get Company](actions/get-company.md) | `GET /api/1.0/companies/:companyId` | [docs](https://api2.timedoctor.com/#operation/getCompany) |
| [Get Company Timezones](actions/get-company-timezones.md) | `GET /api/1.0/companies/:companyId/timezones` | [docs](https://api2.timedoctor.com/#operation/getCompanyTimezones) |
| [Get Invitation Status](actions/get-invitation-status.md) | `GET /api/1.0/invitations/exists` | [docs](https://api2.timedoctor.com/#operation/getInvitations) |
| [Get Leave Stats](actions/get-leave-stats.md) | `GET /api/1.0/work-schedules/stats` | [docs](https://api2.timedoctor.com/#operation/getLeaveStats) |
| [Get Project](actions/get-project.md) | `GET /api/1.0/projects/:projectId` | [docs](https://api2.timedoctor.com/#operation/project) |
| [Get Tag](actions/get-tag.md) | `GET /api/1.0/tags/:tagId` | [docs](https://api2.timedoctor.com/#operation/getTag) |
| [Get Task](actions/get-task.md) | `GET /api/1.0/tasks/:taskId` | [docs](https://api2.timedoctor.com/#operation/task) |
| [Get Unrated Categories Count](actions/get-unrated-categories-count.md) | `GET /api/1.0/categories/unrated-count` | [docs](https://api2.timedoctor.com/#operation/getCategoriesUnratedCount) |
| [Get User](actions/get-user.md) | `GET /api/1.0/users/:userId` | [docs](https://api2.timedoctor.com/#operation/getUser) |
| [List User Categories](actions/get-user-categories.md) | `GET /api/1.0/categories/user/:userId` | [docs](https://api2.timedoctor.com/#operation/getUserCategories) |
| [Get User Totals](actions/get-user-totals.md) | `GET /api/1.0/users/totals` | [docs](https://api2.timedoctor.com/#operation/getUsersTotals) |
| [Invite User](actions/invite-user.md) | `POST /api/1.1/invitations` | [docs](https://api2.timedoctor.com/#operation/postInvitation) |
| [List Categories](actions/list-categories.md) | `GET /api/1.0/categories` | [docs](https://api2.timedoctor.com/#operation/getCategories) |
| [List Companies](actions/list-companies.md) | `GET /api/1.0/companies` | [docs](https://api2.timedoctor.com/#operation/getCompanies) |
| [List Managed Users](actions/list-managed-users.md) | `GET /api/1.0/users/:userId/managed` | [docs](https://api2.timedoctor.com/#operation/getManagedUsers) |
| [List Projects](actions/list-projects.md) | `GET /api/1.0/projects` | [docs](https://api2.timedoctor.com/#operation/getProjects) |
| [List Tags](actions/list-tags.md) | `GET /api/1.0/tags` | [docs](https://api2.timedoctor.com/#operation/getTags) |
| [List Tasks](actions/list-tasks.md) | `GET /api/1.0/tasks` | [docs](https://api2.timedoctor.com/#operation/getTasks) |
| [List User Tokens](actions/list-user-tokens.md) | `GET /api/1.0/users/tokens` | [docs](https://api2.timedoctor.com/#operation/getUsersTokens) |
| [List Users](actions/list-users.md) | `GET /api/1.0/users` | [docs](https://api2.timedoctor.com/#operation/getUsers) |
| [List Work Schedule Issues](actions/list-work-schedule-issues.md) | `GET /api/1.0/work-schedules/issues` | [docs](https://api2.timedoctor.com/#operation/getWorkSchedulesIssues) |
| [List Work Schedules](actions/list-work-schedules.md) | `GET /api/1.0/work-schedules` | [docs](https://api2.timedoctor.com/#operation/getWorkSchedules) |
| [Update Project](actions/update-project.md) | `PUT /api/1.0/projects/:projectId` | [docs](https://api2.timedoctor.com/#operation/putProject) |
| [Update Task](actions/update-task.md) | `PUT /api/1.0/tasks/:taskId` | [docs](https://api2.timedoctor.com/#operation/putTask) |
| [Update User](actions/update-user.md) | `PUT /api/1.0/users/:userId` | [docs](https://api2.timedoctor.com/#operation/putUser) |

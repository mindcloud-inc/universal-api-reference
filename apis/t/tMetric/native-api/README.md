# TMetric: Native API Reference

A consolidated summary of TMetric's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://app.tmetric.com/api-docs
- **API base URL:** `https://app.tmetric.com/api/v3`

## Authentication

### API Token

Use a TMetric API token from Profile Settings -> Get new API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tmetric.com/help/data-management/importing-your-data)

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Time Entry Break](actions/add-time-entry-break.md) | `POST /accounts/:accountId/timeentries/break` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/post-accounts-accountId-timeentries-break) |
| [Create Project](actions/create-project.md) | `POST /accounts/:accountId/projects` | [docs](https://app.tmetric.com/api-docs/#/Projects/post-accounts-accountId-projects) |
| [Create Task](actions/create-task.md) | `POST /accounts/:accountId/tasks` | [docs](https://app.tmetric.com/api-docs/#/Tasks/post-accounts-accountId-tasks) |
| [Create Time Entry](actions/create-time-entry.md) | `POST /accounts/:accountId/timeentries` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/post-accounts-accountId-timeentries) |
| [Delete Task](actions/delete-task.md) | `DELETE /accounts/:accountId/tasks/:taskId` | [docs](https://app.tmetric.com/api-docs/#/Tasks/delete-accounts-accountId-tasks-taskId) |
| [Delete Time Entry](actions/delete-time-entry.md) | `DELETE /accounts/:accountId/timeentries/:timeEntryId` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/delete-accounts-accountId-timeentries-timeEntryId) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /accounts/:accountId/balance` | [docs](https://app.tmetric.com/api-docs/#/Time%20Balance/get-accounts-accountId-balance) |
| [Get Current User](actions/get-current-user.md) | `GET /user` | [docs](https://app.tmetric.com/api-docs/#/User/get-user) |
| [Get Latest Time Entry](actions/get-latest-time-entry.md) | `GET /accounts/:accountId/timeentries/latest` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-latest) |
| [Get Profitability Report](actions/get-profitability-report.md) | `GET /accounts/:accountId/reports/profitability` | [docs](https://app.tmetric.com/api-docs/#/Reports/get-accounts-accountId-reports-profitability) |
| [Get Project Report](actions/get-project-report.md) | `GET /accounts/:accountId/reports/projects` | [docs](https://app.tmetric.com/api-docs/#/Reports/get-accounts-accountId-reports-projects) |
| [Get Project Report Filters](actions/get-project-report-filters.md) | `GET /accounts/:accountId/reports/projects/filter` | [docs](https://app.tmetric.com/api-docs/#/Reports/get-accounts-accountId-reports-teamFilter) |
| [Get Schedule](actions/get-schedule.md) | `GET /accounts/:accountId/schedule` | [docs](https://app.tmetric.com/api-docs/#/Schedule/get-accounts-accountId-schedule) |
| [Get Task](actions/get-task.md) | `GET /accounts/:accountId/tasks/:taskId` | [docs](https://app.tmetric.com/api-docs/#/Tasks/get-accounts-accountId-tasks-taskId) |
| [List Clients](actions/list-clients.md) | `GET /accounts/:accountId/clients` | [docs](https://app.tmetric.com/api-docs/#/Clients/get-accounts-accountId-clients) |
| [List Managed Teams](actions/list-managed-teams.md) | `GET /accounts/:accountId/teams/managed` | [docs](https://app.tmetric.com/api-docs/#/Teams/get-accounts-accountId-teams) |
| [List Project Managers](actions/list-project-managers.md) | `GET /accounts/:accountId/projects/managers` | [docs](https://app.tmetric.com/api-docs/#/Projects/get-accounts-accountId-projects-managers) |
| [List Project Tags](actions/list-project-tags.md) | `GET /accounts/:accountId/timeentries/tags` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-tags) |
| [List Recent Tasks](actions/list-recent-tasks.md) | `GET /accounts/:accountId/tasks/recent` | [docs](https://app.tmetric.com/api-docs/#/Tasks/get-accounts-accountId-tasks-recent) |
| [List Recent Time Entries](actions/list-recent-time-entries.md) | `GET /accounts/:accountId/timeentries/recent` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-recent) |
| [List Task Changes](actions/list-task-changes.md) | `GET /accounts/:accountId/tasks/:taskId/changes` | [docs](https://app.tmetric.com/api-docs/#/Tasks/get-api-v3-accounts-accountId-tasks-taskId-changes) |
| [List Tasks](actions/list-tasks.md) | `GET /accounts/:accountId/tasks` | [docs](https://app.tmetric.com/api-docs/#/Tasks/get-accounts-accountId-tasks) |
| [List Time Entries](actions/list-time-entries.md) | `GET /accounts/:accountId/timeentries` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries) |
| [List Time Tracking Statuses](actions/list-time-tracking-statuses.md) | `GET /accounts/:accountId/timeentries/statuses` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-statuses) |
| [List Trackable Projects](actions/list-trackable-projects.md) | `GET /accounts/:accountId/timeentries/projects` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/get-accounts-accountId-timeentries-projects) |
| [Patch Task](actions/patch-task.md) | `PATCH /accounts/:accountId/tasks/:taskId` | [docs](https://app.tmetric.com/api-docs/#/Tasks/patch-accounts-accountId-tasks-taskId) |
| [Pin Recent Time Entry](actions/pin-recent-time-entry.md) | `PUT /accounts/:accountId/timeentries/recent` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/put-accounts-accountId-timeentries-recent) |
| [Update Current User](actions/update-current-user.md) | `PATCH /user` | [docs](https://app.tmetric.com/api-docs/#/User/patch-user) |
| [Update Time Entry](actions/update-time-entry.md) | `PUT /accounts/:accountId/timeentries/:timeEntryId` | [docs](https://app.tmetric.com/api-docs/#/Time%20Entries/put-accounts-accountId-timeentries-timeEntryId) |

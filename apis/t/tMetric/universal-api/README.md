# <img src="https://images.mindcloud.co/apps/icons/t-metric_1774983035338.png" alt="TMetric logo" width="28" height="28"> TMetric: Universal API

Track time, manage tasks, manage clients, and report on project profitability.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tMetric/latest
- **Category:** Productivity / Project Management
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tmetric.com/
- **Vendor API docs:** https://app.tmetric.com/api-docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tMetric/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET |  |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Trackable Projects](actions/list-trackable-projects.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Profitability Report](actions/get-profitability-report.md) | GET |  |
| [Get Project Report](actions/get-project-report.md) | GET |  |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Schedule](actions/get-schedule.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Time Tracking Statuses](actions/list-time-tracking-statuses.md) | GET |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Project Tags](actions/list-project-tags.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Recent Tasks](actions/list-recent-tasks.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Patch Task](actions/patch-task.md) | PUT |  |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [List Managed Teams](actions/list-managed-teams.md) | GET |  |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Add Time Entry Break](actions/add-time-entry-break.md) | POST |  |
| [Create Time Entry](actions/create-time-entry.md) | POST |  |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE |  |
| [Get Latest Time Entry](actions/get-latest-time-entry.md) | GET |  |
| [List Recent Time Entries](actions/list-recent-time-entries.md) | GET |  |
| [List Time Entries](actions/list-time-entries.md) | GET |  |
| [Pin Recent Time Entry](actions/pin-recent-time-entry.md) | PUT |  |
| [Update Time Entry](actions/update-time-entry.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Balance](actions/get-account-balance.md) | GET |  |
| [Get Project Report Filters](actions/get-project-report-filters.md) | GET |  |
| [List Task Changes](actions/list-task-changes.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |
| [Update Current User](actions/update-current-user.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Project Managers](actions/list-project-managers.md) | GET |  |


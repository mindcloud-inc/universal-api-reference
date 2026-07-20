# <img src="https://images.mindcloud.co/apps/icons/time-live_1775224717176.png" alt="TimeLive logo" width="28" height="28"> TimeLive: Universal API

TimeLive is a time tracking and project management platform for employees, projects, tasks, timesheets, expenses, and billing workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/timeLive/latest
- **Category:** Productivity / Project Management
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.livetecs.com/
- **Vendor API docs:** https://livetecs.com/timelive/integrations/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Employees](actions/list-employees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeLive/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [List Clients](actions/list-clients.md) | GET | Retrieves all client records from TimeLive. |

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Employees](actions/list-employees.md) | GET | Retrieves active employee records from TimeLive. |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves all expense records from TimeLive. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves all project records from TimeLive. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves all task records from TimeLive. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [List Time Entries By Employee Id And Date Range](actions/list-time-entries-by-employee-id-and-date-range.md) | GET | Retrieves time entries from TimeLive by employee and date range. |


# <img src="https://images.mindcloud.co/apps/icons/worktivity-community_1778104264220.png" alt="Worktivity logo" width="28" height="28"> Worktivity: Universal API

Worktivity provides time tracking, employee monitoring, project/task management, productivity analytics, screenshots, payroll, and team operations APIs for organizations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/worktivity/latest
- **Category:** Human Resources / HRIS
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://useworktivity.com
- **Vendor API docs:** https://useworktivity.com/for-developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Application Usage Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Usage Summary](actions/get-application-usage-summary.md) | GET | Retrieves application usage summaries from Worktivity. |

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Customer](actions/create-or-update-customer.md) | PUT | Creates or updates a customer in Worktivity. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Worktivity with optional filters. |

### Employee

| Action | Method | Description |
| --- | --- | --- |
| [Block or Unblock Employee](actions/block-or-unblock-employee.md) | PUT | Blocks or unblocks an employee in Worktivity. |
| [Create Employee](actions/create-employee.md) | POST | Creates a new employee in Worktivity. |
| [List Employees](actions/list-employees.md) | GET | Retrieves employees from Worktivity with optional filters. |
| [Update Employee](actions/update-employee.md) | PUT | Updates an existing employee in Worktivity. |

### Enumeration

| Action | Method | Description |
| --- | --- | --- |
| [List System Enumerations](actions/list-system-enumerations.md) | GET | Retrieves system enumeration values from Worktivity. |

### Productivity Insight

| Action | Method | Description |
| --- | --- | --- |
| [Get Productivity Insights](actions/get-productivity-insights.md) | GET | Retrieves productivity insights from Worktivity for selected filters. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Project](actions/create-or-update-project.md) | PUT | Creates or updates a project in Worktivity. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Worktivity by project ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Worktivity with optional filters. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [List Screenshots](actions/list-screenshots.md) | GET | Retrieves screenshots from Worktivity with optional filters. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Project Task](actions/create-or-update-project-task.md) | PUT | Creates or updates a project task in Worktivity. |
| [Get Project Task](actions/get-project-task.md) | GET | Retrieves a project task from Worktivity by task ID. |
| [List Project Tasks](actions/list-project-tasks.md) | GET | Retrieves project tasks from Worktivity with optional filters. |
| [Update Project Task Assignees](actions/update-project-task-assignees.md) | PUT | Updates assignees for a project task in Worktivity. |
| [Update Project Task Status](actions/update-project-task-status.md) | PUT | Updates a project task status in Worktivity. |

### Task Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Project Task Comments](actions/list-project-task-comments.md) | GET | Retrieves project task comments from Worktivity. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Team](actions/create-or-update-team.md) | PUT | Creates or updates a team in Worktivity. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from Worktivity with optional filters. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Manual Time Entries](actions/list-manual-time-entries.md) | GET | Retrieves manual time entries from Worktivity. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from Worktivity with date filters. |

### Work Times Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Times Analytics](actions/get-work-times-analytics.md) | GET | Retrieves work time analytics from Worktivity. |


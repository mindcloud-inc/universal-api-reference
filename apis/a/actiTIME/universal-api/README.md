# <img src="https://images.mindcloud.co/apps/icons/acti-time_1774883844481.png" alt="actiTIME logo" width="28" height="28"> actiTIME: Universal API

Track time, manage projects, and oversee teams and leave

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/actiTIME/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.actitime.com/
- **Vendor API docs:** https://www.actitime.com/api-documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Activities

| Action | Method | Description |
| --- | --- | --- |
| [Get Default Type of Work](actions/get-default-type-of-work.md) | GET | Retrieves the default type of work from actiTIME. |
| [Get Type of Work](actions/get-type-of-work.md) | GET | Retrieves a type of work from actiTIME. |
| [List Types of Work](actions/list-types-of-work.md) | GET | Retrieves a list of types of work from actiTIME. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Leave Type](actions/get-leave-type.md) | GET | Retrieves a leave type from actiTIME. |
| [List Leave Types](actions/list-leave-types.md) | GET | Retrieves a list of leave types from actiTIME. |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Comments](actions/list-customer-comments.md) | GET | Retrieves comments for a customer in actiTIME. |
| [List Project Comments](actions/list-project-comments.md) | GET | Retrieves comments for a project in actiTIME. |
| [List Task Comments](actions/list-task-comments.md) | GET | Retrieves comments for a task in actiTIME. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a specific customer from actiTIME. |
| [List Customers](actions/list-customers.md) | GET | Retrieves a list of customers from actiTIME. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Get Department](actions/get-department.md) | GET | Retrieves a specific department from actiTIME. |
| [List Departments](actions/list-departments.md) | GET | Retrieves a list of departments from actiTIME. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a specific project from actiTIME. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from actiTIME. |

### Resource Allocations

| Action | Method | Description |
| --- | --- | --- |
| [Get User Work Assignments](actions/get-user-work-assignments.md) | GET | Retrieves a user's work assignments from actiTIME. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get User Schedule](actions/get-user-schedule.md) | GET | Retrieves a user's schedule from actiTIME. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Status](actions/get-workflow-status.md) | GET | Retrieves a workflow status from actiTIME. |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | GET | Retrieves a list of workflow statuses from actiTIME. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves a specific task from actiTIME. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from actiTIME. |

### Time Off Requests

| Action | Method | Description |
| --- | --- | --- |
| [Get Leave Time](actions/get-leave-time.md) | GET | Retrieves leave time records from actiTIME by date range. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Track](actions/get-time-track.md) | GET | Retrieves time track records from actiTIME by date range. |

### Timezone Settings

| Action | Method | Description |
| --- | --- | --- |
| [List Time Zone Groups](actions/list-time-zone-groups.md) | GET | Retrieves time zone groups from actiTIME. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from actiTIME. |
| [Get User](actions/get-user.md) | GET | Retrieves a specific user from actiTIME. |
| [List Customer Assigned Users](actions/list-customer-assigned-users.md) | GET | Retrieves users assigned to a customer in actiTIME. |
| [List Project Assigned Users](actions/list-project-assigned-users.md) | GET | Retrieves users assigned to a project in actiTIME. |
| [List Task Assigned Users](actions/list-task-assigned-users.md) | GET | Retrieves users assigned to a task in actiTIME. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from actiTIME. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get Settings and Info](actions/get-settings-and-info.md) | GET | Retrieves workspace settings and info from actiTIME. |


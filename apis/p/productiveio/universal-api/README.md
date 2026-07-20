# <img src="https://images.mindcloud.co/apps/icons/productiveio_1773769127887.png" alt="Productive.io logo" width="28" height="28"> Productive.io: Universal API

Manage projects, people, time tracking, deals, budgets, and financial operations in Productive.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productiveio/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://productive.io/
- **Vendor API docs:** https://developer.productive.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productiveio/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Booking

| Action | Method | Description |
| --- | --- | --- |
| [Get Booking](actions/get-booking.md) | GET | Retrieves a booking from your Productive.io account. |
| [List Bookings](actions/list-bookings.md) | GET | Retrieves bookings from your Productive.io account. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET | Retrieves a company from your Productive.io account. |
| [List Companies](actions/list-companies.md) | GET | Retrieves companies from your Productive.io account. |

### Contact Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Contact Entry](actions/get-contact-entry.md) | GET | Retrieves a contact entry from your Productive.io account. |
| [List Contact Entries](actions/list-contact-entries.md) | GET | Retrieves contact entries from your Productive.io account. |

### Contract

| Action | Method | Description |
| --- | --- | --- |
| [Get Contract](actions/get-contract.md) | GET | Retrieves a contract from your Productive.io account. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from your Productive.io account. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal from your Productive.io account. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deals from your Productive.io account. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Get Expense](actions/get-expense.md) | GET | Retrieves an expense from your Productive.io account. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from your Productive.io account. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from your Productive.io account. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Productive.io account. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from your Productive.io account. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from your Productive.io account. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves a person from your Productive.io account. |
| [List People](actions/list-people.md) | GET | Retrieves people from your Productive.io account. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from your Productive.io account. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from your Productive.io account. |

### Project Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Assignment](actions/get-project-assignment.md) | GET | Retrieves a project assignment from your Productive.io account. |
| [List Project Assignments](actions/list-project-assignments.md) | GET | Retrieves project assignments from your Productive.io account. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from your Productive.io account. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from your Productive.io account. |

### Task List

| Action | Method | Description |
| --- | --- | --- |
| [Get Task List](actions/get-task-list.md) | GET | Retrieves a task list from your Productive.io account. |
| [List Task Lists](actions/list-task-lists.md) | GET | Retrieves task lists from your Productive.io account. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from your Productive.io account. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from your Productive.io account. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from your Productive.io account. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from your Productive.io account. |

### Timer

| Action | Method | Description |
| --- | --- | --- |
| [Get Timer](actions/get-timer.md) | GET | Retrieves a timer from your Productive.io account. |
| [List Timers](actions/list-timers.md) | GET | Retrieves timers from your Productive.io account. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Get Timesheet](actions/get-timesheet.md) | GET | Retrieves a timesheet from your Productive.io account. |
| [List Timesheets](actions/list-timesheets.md) | GET | Retrieves timesheets from your Productive.io account. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from your Productive.io account. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Productive.io account. |

### Workflow

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow](actions/get-workflow.md) | GET | Retrieves a workflow from your Productive.io account. |
| [List Workflows](actions/list-workflows.md) | GET | Retrieves workflows from your Productive.io account. |

### Workflow Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Workflow Status](actions/get-workflow-status.md) | GET | Retrieves a workflow status from your Productive.io account. |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | GET | Retrieves workflow statuses from your Productive.io account. |


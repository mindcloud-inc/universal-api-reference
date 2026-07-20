# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-14-at-12_1773500839522.png" alt="Harvest logo" width="28" height="28"> Harvest: Universal API

Track time, manage projects, and handle invoices in Harvest

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harvest/latest
- **Category:** Productivity / Project Management
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.getharvest.com/
- **Vendor API docs:** https://help.getharvest.com/api-v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Current User](actions/retrieve-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/retrieve-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Categories](actions/list-expense-categories.md) | GET | Retrieves expense categories from Harvest. |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in Harvest. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Harvest. |
| [Retrieve Client](actions/retrieve-client.md) | GET | Retrieves a client from Harvest. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Harvest. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Company](actions/retrieve-company.md) | GET | Retrieves company details from Harvest. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Harvest. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Harvest. |
| [Retrieve Contact](actions/retrieve-contact.md) | GET | Retrieves a contact from Harvest. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Harvest. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Delete client](actions/delete-client.md) | DELETE | Deletes an existing client from Harvest. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from Harvest. |

### Expenses

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in Harvest. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in Harvest. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Harvest. |
| [Retrieve Invoice](actions/retrieve-invoice.md) | GET | Retrieves an invoice from Harvest. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in Harvest. |
| [Delete invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Harvest. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Harvest. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Harvest. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Harvest. |
| [Retrieve Project](actions/retrieve-project.md) | GET | Retrieves a project from Harvest. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Harvest. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Delete project](actions/delete-project.md) | DELETE | Deletes an existing project from Harvest. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Harvest. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Harvest. |
| [Retrieve Task](actions/retrieve-task.md) | GET | Retrieves a task from Harvest. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Harvest. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Task Assignment](actions/create-project-task-assignment.md) | POST | Creates a task assignment for a project in Harvest. |
| [Delete task](actions/delete-task.md) | DELETE | Deletes an existing task from Harvest. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Harvest. |
| [Retrieve Time Entry](actions/retrieve-time-entry.md) | GET | Retrieves a time entry from Harvest. |

### Timesheet Entries

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Harvest. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Harvest. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Harvest. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Current User](actions/retrieve-current-user.md) | GET | Retrieves the current user from Harvest. |


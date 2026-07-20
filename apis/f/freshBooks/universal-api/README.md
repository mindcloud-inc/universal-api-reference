# <img src="https://images.mindcloud.co/apps/icons/freshbooks-logo-png-seeklogo-431917_1773266675567.png" alt="FreshBooks logo" width="28" height="28"> FreshBooks: Universal API

Manage clients, invoices, expenses, projects, and time entries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freshBooks/latest
- **Category:** Commerce / Accounting
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.freshbooks.com
- **Vendor API docs:** https://www.freshbooks.com/api/start

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Profile](actions/get-current-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshBooks/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST | Creates a new client in FreshBooks for an account. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from FreshBooks for an account. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from FreshBooks for an account. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in FreshBooks for an account. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in FreshBooks for an account. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves an estimate from FreshBooks for an account. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from FreshBooks for an account. |
| [Update Estimate](actions/update-estimate.md) | PUT | Updates an existing estimate in FreshBooks for an account. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in FreshBooks for an account. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves an expense from FreshBooks for an account. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from FreshBooks for an account. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in FreshBooks for an account. |

### Expense Category

| Action | Method | Description |
| --- | --- | --- |
| [List Expense Categories](actions/list-expense-categories.md) | GET | Retrieves expense categories from FreshBooks for an account. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in FreshBooks for an account. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from FreshBooks for an account. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from FreshBooks for an account. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in FreshBooks for an account. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in FreshBooks for a business. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from FreshBooks for a business. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from FreshBooks for a business. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in FreshBooks for a business. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in FreshBooks for a business. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from FreshBooks for a business. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from FreshBooks for a business. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Profile](actions/get-current-user-profile.md) | GET | Retrieves the current user profile from FreshBooks. |


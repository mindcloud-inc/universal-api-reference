# <img src="https://images.mindcloud.co/apps/icons/harpoon_1775685408655.png" alt="Harpoon logo" width="28" height="28"> Harpoon: Universal API

Plan finances, track time, send invoices, and manage projects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/harpoon/latest
- **Category:** Commerce / Accounting
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://harpoonapp.com/
- **Vendor API docs:** https://app.harpoonapp.com/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Harpoon. |
| [List Clients](actions/list-clients.md) | GET | Retrieves clients from Harpoon. |
| [Update Client](actions/update-client.md) | PUT | Updates an existing client in Harpoon. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in Harpoon. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves estimates from Harpoon. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in Harpoon. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves an expense from Harpoon. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves expenses from Harpoon. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in Harpoon. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Harpoon. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from Harpoon. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Harpoon. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Harpoon. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Harpoon. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Harpoon. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Harpoon. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Clone Time Entry](actions/clone-time-entry.md) | POST | Clones a time entry in Harpoon with zero hours. |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in Harpoon. |
| [Delete Time Entry](actions/delete-time-entry.md) | DELETE | Deletes an existing time entry from Harpoon. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from Harpoon. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from Harpoon. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in Harpoon. |


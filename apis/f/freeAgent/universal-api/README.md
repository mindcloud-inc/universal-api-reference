# <img src="https://images.mindcloud.co/apps/icons/free-agent_1773695176587.png" alt="FreeAgent logo" width="28" height="28"> FreeAgent: Universal API

Manage contacts, invoices, projects, and bills in FreeAgent

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freeAgent/latest
- **Category:** Commerce / Accounting
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.freeagent.com
- **Vendor API docs:** https://dev.freeagent.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Bill](actions/get-bill.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-bill?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Bill

| Action | Method | Description |
| --- | --- | --- |
| [Create Bill](actions/create-bill.md) | POST | Creates a new bill in FreeAgent. |
| [Get Bill](actions/get-bill.md) | GET | Retrieves detailed bill information from FreeAgent. |
| [List Bills](actions/list-bills.md) | GET | Retrieves a list of bills from FreeAgent. |
| [Update Bill](actions/update-bill.md) | PUT | Updates an existing bill in FreeAgent. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in FreeAgent. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves detailed contact information from FreeAgent. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves a list of contacts from FreeAgent. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in FreeAgent. |

### Estimate

| Action | Method | Description |
| --- | --- | --- |
| [Create Estimate](actions/create-estimate.md) | POST | Creates a new estimate in FreeAgent. |
| [Get Estimate](actions/get-estimate.md) | GET | Retrieves detailed estimate information from FreeAgent. |
| [List Estimates](actions/list-estimates.md) | GET | Retrieves a list of estimates from FreeAgent. |
| [Update Estimate](actions/update-estimate.md) | PUT | Updates an existing estimate in FreeAgent. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense](actions/create-expense.md) | POST | Creates a new expense in FreeAgent. |
| [Get Expense](actions/get-expense.md) | GET | Retrieves detailed expense information from FreeAgent. |
| [List Expenses](actions/list-expenses.md) | GET | Retrieves a list of expenses from FreeAgent. |
| [Update Expense](actions/update-expense.md) | PUT | Updates an existing expense in FreeAgent. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in FreeAgent. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves detailed invoice information from FreeAgent. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves a list of invoices from FreeAgent. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in FreeAgent. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in FreeAgent. |
| [Get Project](actions/get-project.md) | GET | Retrieves detailed project information from FreeAgent. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a list of projects from FreeAgent. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in FreeAgent. |


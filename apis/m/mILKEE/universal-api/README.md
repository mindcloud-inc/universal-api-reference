# <img src="https://images.mindcloud.co/apps/icons/m-ilkee_1774988650133.png" alt="MILKEE logo" width="28" height="28"> MILKEE: Universal API

REST API integration for MILKEE, a Swiss accounting platform for invoices, time tracking, projects, customers, proposals, and bookkeeping workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mILKEE/latest
- **Category:** Commerce / Accounting
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://milkee.ch
- **Vendor API docs:** https://apidocs.milkee.ch/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Customers](actions/list-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mILKEE/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0&companyId=4640" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | POST | Creates a new customer in MILKEE. |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from MILKEE. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from MILKEE. |
| [Update Customer](actions/update-customer.md) | PUT | Updates an existing customer in MILKEE. |

### Customer Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Statistics](actions/get-customer-statistics.md) | GET | Retrieves customer statistics from MILKEE. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Invoice](actions/create-invoice.md) | POST | Creates a new invoice in MILKEE. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from MILKEE. |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from MILKEE. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in MILKEE. |

### Invoice Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Next Invoice Number](actions/get-next-invoice-number.md) | GET | Retrieves the next invoice number from MILKEE. |

### Invoice Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Invoice Status](actions/update-invoice-status.md) | PUT | Updates an invoice status in MILKEE. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in MILKEE. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from MILKEE. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from MILKEE. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in MILKEE. |

### Proposal

| Action | Method | Description |
| --- | --- | --- |
| [Create Proposal](actions/create-proposal.md) | POST | Creates a new proposal in MILKEE. |
| [Get Proposal](actions/get-proposal.md) | GET | Retrieves a proposal from MILKEE. |
| [List Proposals](actions/list-proposals.md) | GET | Retrieves proposals from MILKEE. |
| [Update Proposal](actions/update-proposal.md) | PUT | Updates an existing proposal in MILKEE. |

### Proposal Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Proposal Status](actions/update-proposal-status.md) | PUT | Updates a proposal status in MILKEE. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in MILKEE. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from MILKEE. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from MILKEE. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in MILKEE. |

### Time Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create Time Entry](actions/create-time-entry.md) | POST | Creates a new time entry in MILKEE. |
| [Get Time Entry](actions/get-time-entry.md) | GET | Retrieves a time entry from MILKEE. |
| [List Time Entries](actions/list-time-entries.md) | GET | Retrieves time entries from MILKEE. |
| [Update Time Entry](actions/update-time-entry.md) | PUT | Updates an existing time entry in MILKEE. |

### Timer

| Action | Method | Description |
| --- | --- | --- |
| [Get Timer Status](actions/get-timer-status.md) | GET | Retrieves the timer status from MILKEE. |
| [Start Or Stop Timer](actions/start-or-stop-timer.md) | PUT | Starts or stops a timer in MILKEE. |


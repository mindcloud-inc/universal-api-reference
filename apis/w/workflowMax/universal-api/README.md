# <img src="https://images.mindcloud.co/apps/icons/workflow-max_1774900595145.png" alt="WorkflowMax logo" width="28" height="28"> WorkflowMax: Universal API

Manage jobs, clients, timesheets, quotes, and invoices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workflowMax/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://workflowmax.com/
- **Vendor API docs:** https://api-docs.workflowmax.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workflowMax/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Bills

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order Bill](actions/create-purchase-order-bill.md) | POST |  |
| [List Purchase Order Bills](actions/list-purchase-order-bills.md) | GET |  |

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | POST |  |
| [Get Client](actions/get-client.md) | GET |  |
| [List Clients](actions/list-clients.md) | GET |  |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [Get Invoice](actions/get-invoice.md) | GET |  |
| [List Invoices](actions/list-invoices.md) | GET |  |

### Job Cost

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Cost](actions/create-job-cost.md) | POST |  |
| [List Job Costs](actions/list-job-costs.md) | GET |  |
| [Update Job Cost](actions/update-job-cost.md) | PUT |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Job](actions/create-job.md) | POST |  |
| [Delete Job](actions/delete-job.md) | DELETE |  |
| [Get Job](actions/get-job.md) | GET |  |
| [List Jobs](actions/list-jobs.md) | GET |  |
| [Update Job](actions/update-job.md) | PUT |  |

### Payments

| Action | Method | Description |
| --- | --- | --- |
| [List Payments](actions/list-payments.md) | GET |  |

### Purchase Orders

| Action | Method | Description |
| --- | --- | --- |
| [Create Purchase Order](actions/create-purchase-order.md) | POST |  |
| [Get Purchase Order](actions/get-purchase-order.md) | GET |  |
| [List Purchase Orders](actions/list-purchase-orders.md) | GET |  |

### Quotes

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Quote](actions/create-job-quote.md) | POST |  |
| [Get Quote](actions/get-quote.md) | GET |  |
| [List Quotes](actions/list-quotes.md) | GET |  |

### Supplier

| Action | Method | Description |
| --- | --- | --- |
| [Create Supplier](actions/create-supplier.md) | POST |  |
| [Get Supplier](actions/get-supplier.md) | GET |  |
| [List Suppliers](actions/list-suppliers.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Task](actions/create-job-task.md) | POST |  |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Job Task](actions/delete-job-task.md) | DELETE |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Job Tasks](actions/list-job-tasks.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Job Task](actions/update-job-task.md) | PUT |  |
| [Update Task](actions/update-task.md) | PUT |  |

### Timesheets

| Action | Method | Description |
| --- | --- | --- |
| [Create Timesheet](actions/create-timesheet.md) | POST |  |
| [Delete Timesheet](actions/delete-timesheet.md) | DELETE |  |
| [Get Timesheet](actions/get-timesheet.md) | GET |  |
| [List Timesheets](actions/list-timesheets.md) | GET |  |
| [Update Timesheet](actions/update-timesheet.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |


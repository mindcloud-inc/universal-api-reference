# WorkflowMax: Native API Reference

A consolidated summary of WorkflowMax's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.workflowmax.com/
- **API base URL:** `https://api.workflowmax.com`

## Authentication

### OAuth 2.0

### Credentials

- **Organisation ID:** `accountId` · required · Required WorkflowMax organisation ID used for the `account_id` request header. Copy it from your WorkflowMax URL when prompted during connection.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://oauth.workflowmax.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth.workflowmax.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `openid profile email workflowmax offline_access`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://oauth.workflowmax.com/oauth/token.

[Official authentication documentation](https://support.workflowmax.com/hc/en-us/articles/28754786654233-API-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `pageSize` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Client](actions/create-client.md) | `POST v2/clients` | [docs](https://api-docs.workflowmax.com/client/post-v2-clients) |
| [Create Job](actions/create-job.md) | `POST v2/jobs` | [docs](https://api-docs.workflowmax.com/job-1/post-v2-jobs) |
| [Create Job Cost](actions/create-job-cost.md) | `POST v2/jobs/{identifier}/costs` | [docs](https://api-docs.workflowmax.com/job-cost/post-v2-jobs-uuid-costs-copy) |
| [Create Job Quote](actions/create-job-quote.md) | `POST v2/jobs/{UUID}/quotes` | [docs](https://api-docs.workflowmax.com/quote/post-v2-jobs-uuid-quotes) |
| [Create Job Task](actions/create-job-task.md) | `POST v2/jobs/{identifier}/tasks` | [docs](https://api-docs.workflowmax.com/job-task/post-v2-jobs-uuidtasks) |
| [Create Purchase Order](actions/create-purchase-order.md) | `POST v2/purchase-orders` | [docs](https://api-docs.workflowmax.com/po-2/post-v2-purchase-orders) |
| [Create Purchase Order Bill](actions/create-purchase-order-bill.md) | `POST v2/purchase-orders/{identifier}/bills` | [docs](https://api-docs.workflowmax.com/po-bill-2/post-v2-purchase-orders-uuid-bills) |
| [Create Supplier](actions/create-supplier.md) | `POST v2/suppliers` | [docs](https://api-docs.workflowmax.com/supplier/post-v2-suppliers) |
| [Create Task](actions/create-task.md) | `POST v2/tasks` | [docs](https://api-docs.workflowmax.com/task/post-v2-tasks) |
| [Create Timesheet](actions/create-timesheet.md) | `POST v2/timesheets` | [docs](https://api-docs.workflowmax.com/timesheet/post-timesheet) |
| [Delete Job](actions/delete-job.md) | `DELETE v2/jobs/{identifier}` | [docs](https://api-docs.workflowmax.com/job-1/delete-v2-jobs-uuid) |
| [Delete Job Task](actions/delete-job-task.md) | `DELETE v2/jobs/tasks/{jobTaskUUID}` | [docs](https://api-docs.workflowmax.com/job-task/delete-v2-jobs-tasks-jobtaskuuid) |
| [Delete Task](actions/delete-task.md) | `DELETE v2/tasks/{UUID}` | [docs](https://api-docs.workflowmax.com/task/delete-v2-tasks-uuid) |
| [Delete Timesheet](actions/delete-timesheet.md) | `DELETE v2/timesheets/{UUID}` | [docs](https://api-docs.workflowmax.com/timesheet/delete-v2-timesheets-uuid) |
| [Get Client](actions/get-client.md) | `GET v2/clients/{UUID}` | [docs](https://api-docs.workflowmax.com/client/get-v2-clients-uuid) |
| [Get Current User](actions/get-current-user.md) | `GET v2/me` | [docs](https://api-docs.workflowmax.com/me/get-v2-me) |
| [Get Invoice](actions/get-invoice.md) | `GET v2/invoices/{UUID}` | [docs](https://api-docs.workflowmax.com/invoice/get-invoice-uuid) |
| [Get Job](actions/get-job.md) | `GET v2/jobs/{identifier}` | [docs](https://api-docs.workflowmax.com/job-1/get-v2-jobs-uuid) |
| [Get Purchase Order](actions/get-purchase-order.md) | `GET v2/purchase-orders/{identifier}` | [docs](https://api-docs.workflowmax.com/po-2/get-v2-purchase-orders-uuid-1) |
| [Get Quote](actions/get-quote.md) | `GET v2/quotes/{UUID}` | [docs](https://api-docs.workflowmax.com/quote/get-v2-quotes-uuid) |
| [Get Supplier](actions/get-supplier.md) | `GET v2/suppliers/{UUID}` | [docs](https://api-docs.workflowmax.com/supplier/get-supplier-uuid) |
| [Get Task](actions/get-task.md) | `GET v2/tasks/{UUID}` | [docs](https://api-docs.workflowmax.com/task/get-v2-tasks-uuid) |
| [Get Timesheet](actions/get-timesheet.md) | `GET v2/timesheets/{UUID}` | [docs](https://api-docs.workflowmax.com/timesheet/get-v2-timesheets-uuid) |
| [List Clients](actions/list-clients.md) | `GET v2/clients` | [docs](https://api-docs.workflowmax.com/client/clients) |
| [List Invoices](actions/list-invoices.md) | `GET v2/invoices` | [docs](https://api-docs.workflowmax.com/invoice/get-invoices) |
| [List Job Costs](actions/list-job-costs.md) | `GET v2/jobs/{UUID}/costs` | [docs](https://api-docs.workflowmax.com/job-cost/get-v2-jobs-uuid-costs) |
| [List Job Tasks](actions/list-job-tasks.md) | `GET v2/jobs/tasks` | [docs](https://api-docs.workflowmax.com/job-task/get-v2-jobs-tasks) |
| [List Jobs](actions/list-jobs.md) | `GET v2/jobs` | [docs](https://api-docs.workflowmax.com/job-1/get-v2-jobs) |
| [List Payments](actions/list-payments.md) | `GET v2/payments` | [docs](https://api-docs.workflowmax.com/invoice/get-v2-payments) |
| [List Purchase Order Bills](actions/list-purchase-order-bills.md) | `GET v2/purchase-orders/bills` | [docs](https://api-docs.workflowmax.com/po-bill-2/get-v2-purchase-orders-bills-1) |
| [List Purchase Orders](actions/list-purchase-orders.md) | `GET v2/purchase-orders` | [docs](https://api-docs.workflowmax.com/po-2/get-v2-purchase-orders-1) |
| [List Quotes](actions/list-quotes.md) | `GET v2/quotes` | [docs](https://api-docs.workflowmax.com/quote/get-v2-quotes) |
| [List Suppliers](actions/list-suppliers.md) | `GET v2/suppliers` | [docs](https://api-docs.workflowmax.com/supplier/get-suppliers) |
| [List Tasks](actions/list-tasks.md) | `GET v2/tasks` | [docs](https://api-docs.workflowmax.com/task/get-v2-tasks) |
| [List Timesheets](actions/list-timesheets.md) | `GET v2/timesheets` | [docs](https://api-docs.workflowmax.com/timesheet/get-v2-timesheets) |
| [Update Job](actions/update-job.md) | `PUT v2/jobs/{identifier}` | [docs](https://api-docs.workflowmax.com/job-1/post-job-copy) |
| [Update Job Cost](actions/update-job-cost.md) | `PUT v2/jobs/costs/{jobCostUUID}` | [docs](https://api-docs.workflowmax.com/job-cost/post-job-identifier-cost-copy) |
| [Update Job Task](actions/update-job-task.md) | `PUT v2/jobs/tasks/{jobTaskUUID}` | [docs](https://api-docs.workflowmax.com/job-task/put-v2-jobs-tasks-jobtaskuuid) |
| [Update Task](actions/update-task.md) | `PUT v2/tasks/{UUID}` | [docs](https://api-docs.workflowmax.com/task/post-tasks-copy) |
| [Update Timesheet](actions/update-timesheet.md) | `PUT v2/timesheets/{UUID}` | [docs](https://api-docs.workflowmax.com/timesheet/put-v2-timesheets-uuid) |

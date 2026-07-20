# Queue: Native API Reference

A consolidated summary of Queue's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.usequeue.com/api-reference/introduction
- **OpenAPI specification:** https://docs.usequeue.com/api-reference/openapi.json
- **API base URL:** `https://app.usequeue.com/api/v1`

## Authentication

### API Key

Use a Queue API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.usequeue.com/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Service Checkout](actions/cancel-service-checkout.md) | `POST service_checkouts/:service_checkout_id/cancel` | [docs](https://docs.usequeue.com/api-reference/service_checkouts/cancel) |
| [Create Column](actions/create-column.md) | `POST projects/:project_id/columns` | [docs](https://docs.usequeue.com/api-reference/columns/create) |
| [Create Column Task](actions/create-column-task.md) | `POST columns/:column_id/tasks` | [docs](https://docs.usequeue.com/api-reference/tasks/create) |
| [Create Project](actions/create-project.md) | `POST projects` | [docs](https://docs.usequeue.com/api-reference/projects/create) |
| [Create Project Client](actions/create-project-client.md) | `POST projects/:project_id/clients` | [docs](https://docs.usequeue.com/api-reference/clients/create) |
| [Create Project Invoice](actions/create-project-invoice.md) | `POST projects/:project_id/invoices` | [docs](https://docs.usequeue.com/api-reference/invoices/create) |
| [Create Project Timesheet](actions/create-project-timesheet.md) | `POST projects/:project_id/timesheets` | [docs](https://docs.usequeue.com/api-reference/timesheets/create) |
| [Delete Client](actions/delete-client.md) | `DELETE clients/:client_id` | [docs](https://docs.usequeue.com/api-reference/clients/delete) |
| [Delete Column](actions/delete-column.md) | `DELETE columns/:column_id` | [docs](https://docs.usequeue.com/api-reference/columns/delete) |
| [Delete File](actions/delete-file.md) | `DELETE files/:file_id` | [docs](https://docs.usequeue.com/api-reference/files/delete) |
| [Delete Invoice](actions/delete-invoice.md) | `DELETE invoices/:invoice_id` | [docs](https://docs.usequeue.com/api-reference/invoices/delete) |
| [Delete Project](actions/delete-project.md) | `DELETE projects/:project_id` | [docs](https://docs.usequeue.com/api-reference/projects/delete) |
| [Delete Service Checkout](actions/delete-service-checkout.md) | `DELETE service_checkouts/:service_checkout_id` | [docs](https://docs.usequeue.com/api-reference/service_checkouts/delete) |
| [Delete Task](actions/delete-task.md) | `DELETE tasks/:task_id` | [docs](https://docs.usequeue.com/api-reference/tasks/delete) |
| [Delete Timesheet](actions/delete-timesheet.md) | `DELETE timesheets/:timesheet_id` | [docs](https://docs.usequeue.com/api-reference/timesheets/delete) |
| [Get Client](actions/get-client.md) | `GET clients/:client_id` | [docs](https://docs.usequeue.com/api-reference/clients/show) |
| [Get Column](actions/get-column.md) | `GET columns/:column_id` | [docs](https://docs.usequeue.com/api-reference/columns/show) |
| [Get Column Tasks](actions/get-column-tasks.md) | `GET columns/:column_id/tasks` | [docs](https://docs.usequeue.com/api-reference/tasks/get) |
| [Get File](actions/get-file.md) | `GET files/:file_id` | [docs](https://docs.usequeue.com/api-reference/files/show) |
| [Get Invoice](actions/get-invoice.md) | `GET invoices/:invoice_id` | [docs](https://docs.usequeue.com/api-reference/invoices/show) |
| [Get Project](actions/get-project.md) | `GET projects/:project_id` | [docs](https://docs.usequeue.com/api-reference/projects/show) |
| [Get Project Clients](actions/get-project-clients.md) | `GET projects/:project_id/clients` | [docs](https://docs.usequeue.com/api-reference/clients/get) |
| [Get Project Columns](actions/get-project-columns.md) | `GET projects/:project_id/columns` | [docs](https://docs.usequeue.com/api-reference/columns/get) |
| [Get Project Files](actions/get-project-files.md) | `GET projects/:project_id/files` | [docs](https://docs.usequeue.com/api-reference/files/get) |
| [Get Project Invoices](actions/get-project-invoices.md) | `GET projects/:project_id/invoices` | [docs](https://docs.usequeue.com/api-reference/invoices/get) |
| [Get Project Service Checkouts](actions/get-project-service-checkouts.md) | `GET projects/:project_id/service_checkouts` | [docs](https://docs.usequeue.com/api-reference/service_checkouts/get) |
| [Get Project Timesheets](actions/get-project-timesheets.md) | `GET projects/:project_id/timesheets` | [docs](https://docs.usequeue.com/api-reference/timesheets/get) |
| [Get Projects](actions/get-projects.md) | `GET projects` | [docs](https://docs.usequeue.com/api-reference/projects/get) |
| [Get Service](actions/get-service.md) | `GET services/:service_id` | [docs](https://docs.usequeue.com/api-reference/services/show) |
| [Get Service Checkout](actions/get-service-checkout.md) | `GET service_checkouts/:service_checkout_id` | [docs](https://docs.usequeue.com/api-reference/service_checkouts/show) |
| [Get Services](actions/get-services.md) | `GET services` | [docs](https://docs.usequeue.com/api-reference/services/get) |
| [Get Task](actions/get-task.md) | `GET tasks/:task_id` | [docs](https://docs.usequeue.com/api-reference/tasks/show) |
| [Get Timesheet](actions/get-timesheet.md) | `GET timesheets/:timesheet_id` | [docs](https://docs.usequeue.com/api-reference/timesheets/show) |
| [Pause Service Checkout](actions/pause-service-checkout.md) | `POST service_checkouts/:service_checkout_id/pause` | [docs](https://docs.usequeue.com/api-reference/service_checkouts/pause) |
| [Unpause Service Checkout](actions/unpause-service-checkout.md) | `POST service_checkouts/:service_checkout_id/unpause` | [docs](https://docs.usequeue.com/api-reference/service_checkouts/unpause) |
| [Update Column](actions/update-column.md) | `PATCH columns/:column_id` | [docs](https://docs.usequeue.com/api-reference/columns/put) |
| [Update Invoice](actions/update-invoice.md) | `PATCH invoices/:invoice_id` | [docs](https://docs.usequeue.com/api-reference/invoices/put) |
| [Update Project](actions/update-project.md) | `PATCH projects/:project_id` | [docs](https://docs.usequeue.com/api-reference/projects/put) |
| [Update Task](actions/update-task.md) | `PATCH tasks/:task_id` | [docs](https://docs.usequeue.com/api-reference/tasks/put) |
| [Update Timesheet](actions/update-timesheet.md) | `PATCH timesheets/:timesheet_id` | [docs](https://docs.usequeue.com/api-reference/timesheets/put) |

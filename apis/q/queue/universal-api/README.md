# <img src="https://images.mindcloud.co/apps/icons/queue_1775852913464.png" alt="Queue logo" width="28" height="28"> Queue: Universal API

Manage projects, tasks, clients, invoices, and timesheets

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/queue/latest
- **Category:** Productivity / Project Management
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.usequeue.com
- **Vendor API docs:** https://docs.usequeue.com/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Projects](actions/get-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Client

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Client](actions/create-project-client.md) | POST | Creates a new client for a Queue project. |
| [Delete Client](actions/delete-client.md) | DELETE | Deletes an existing client from Queue. |
| [Get Client](actions/get-client.md) | GET | Retrieves a client from Queue. |
| [Get Project Clients](actions/get-project-clients.md) | GET | Retrieves clients for a Queue project. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [Create Column](actions/create-column.md) | POST | Creates a new column for a Queue project. |
| [Delete Column](actions/delete-column.md) | DELETE | Deletes an existing column from Queue. |
| [Get Column](actions/get-column.md) | GET | Retrieves a column from Queue. |
| [Get Project Columns](actions/get-project-columns.md) | GET | Retrieves columns for a Queue project. |
| [Update Column](actions/update-column.md) | PUT | Updates an existing column in Queue. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Queue. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from Queue. |
| [Get Project Files](actions/get-project-files.md) | GET | Retrieves files for a Queue project. |

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Invoice](actions/create-project-invoice.md) | POST | Creates a new invoice for a Queue project. |
| [Delete Invoice](actions/delete-invoice.md) | DELETE | Deletes an existing invoice from Queue. |
| [Get Invoice](actions/get-invoice.md) | GET | Retrieves an invoice from Queue. |
| [Get Project Invoices](actions/get-project-invoices.md) | GET | Retrieves invoices for a Queue project. |
| [Update Invoice](actions/update-invoice.md) | PUT | Updates an existing invoice in Queue. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST | Creates a new project in Queue. |
| [Delete Project](actions/delete-project.md) | DELETE | Deletes an existing project from Queue. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Queue. |
| [Get Projects](actions/get-projects.md) | GET | Retrieves projects from Queue. |
| [Update Project](actions/update-project.md) | PUT | Updates an existing project in Queue. |

### Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Service](actions/get-service.md) | GET | Retrieves a service from Queue. |
| [Get Services](actions/get-services.md) | GET | Retrieves services from Queue. |

### Service Checkout

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Service Checkout](actions/cancel-service-checkout.md) | PUT | Cancels a service checkout subscription in Queue. |
| [Delete Service Checkout](actions/delete-service-checkout.md) | DELETE | Deletes an existing service checkout from Queue. |
| [Get Project Service Checkouts](actions/get-project-service-checkouts.md) | GET | Retrieves service checkouts for a Queue project. |
| [Get Service Checkout](actions/get-service-checkout.md) | GET | Retrieves a service checkout from Queue. |
| [Pause Service Checkout](actions/pause-service-checkout.md) | PUT | Pauses a service checkout subscription in Queue. |
| [Unpause Service Checkout](actions/unpause-service-checkout.md) | PUT | Unpauses a service checkout subscription in Queue. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Column Task](actions/create-column-task.md) | POST | Creates a new task for a Queue column. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Queue. |
| [Get Column Tasks](actions/get-column-tasks.md) | GET | Retrieves tasks for a Queue column. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Queue. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Queue. |

### Timesheet

| Action | Method | Description |
| --- | --- | --- |
| [Create Project Timesheet](actions/create-project-timesheet.md) | POST | Creates a new timesheet for a Queue project. |
| [Delete Timesheet](actions/delete-timesheet.md) | DELETE | Deletes an existing timesheet from Queue. |
| [Get Project Timesheets](actions/get-project-timesheets.md) | GET | Retrieves timesheets for a Queue project. |
| [Get Timesheet](actions/get-timesheet.md) | GET | Retrieves a timesheet from Queue. |
| [Update Timesheet](actions/update-timesheet.md) | PUT | Updates an existing timesheet in Queue. |


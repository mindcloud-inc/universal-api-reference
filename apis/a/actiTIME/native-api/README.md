# actiTIME: Native API Reference

A consolidated summary of actiTIME's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://www.actitime.com/api-documentation
- **OpenAPI specification:** https://online.actitime.com/mindcloud/api/v1/swagger.json
- **API base URL:** `{instanceUrl}/api/v1`

## Authentication

### Basic Auth

Use your actiTIME username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Instance URL:** `instanceUrl` · required · Your actiTIME workspace URL without /api/v1, for example https://online.actitime.com/mindcloud

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.actitime.com/api-documentation/api-usage)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 1000; accepted range 0–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Use `+` for ascending order and `-` for descending order. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /users/me` | [docs](https://www.actitime.com/api-documentation/users-resource) |
| [Get Customer](actions/get-customer.md) | `GET /customers/:id` | [docs](https://www.actitime.com/api-documentation/customers-resource) |
| [Get Default Type of Work](actions/get-default-type-of-work.md) | `GET /typesOfWork/default` | [docs](https://www.actitime.com/api-documentation/types-of-work-resource) |
| [Get Department](actions/get-department.md) | `GET /departments/:id` | [docs](https://www.actitime.com/api-documentation/departments-resource) |
| [Get Leave Time](actions/get-leave-time.md) | `GET /leavetime` | [docs](https://www.actitime.com/api-documentation/leave-time-resource) |
| [Get Leave Type](actions/get-leave-type.md) | `GET /leaveTypes/:id` | [docs](https://www.actitime.com/api-documentation/leave-types-resource) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://www.actitime.com/api-documentation/projects-resource) |
| [Get Settings and Info](actions/get-settings-and-info.md) | `GET /info` | [docs](https://www.actitime.com/api-documentation/info-resource) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://www.actitime.com/api-documentation/tasks-resource) |
| [Get Time Track](actions/get-time-track.md) | `GET /timetrack` | [docs](https://www.actitime.com/api-documentation/time-track-resource) |
| [Get Type of Work](actions/get-type-of-work.md) | `GET /typesOfWork/:id` | [docs](https://www.actitime.com/api-documentation/types-of-work-resource) |
| [Get User](actions/get-user.md) | `GET /users/:uid` | [docs](https://www.actitime.com/api-documentation/users-resource) |
| [Get User Schedule](actions/get-user-schedule.md) | `GET /users/:uid/schedule` | [docs](https://www.actitime.com/api-documentation/users-resource) |
| [Get User Work Assignments](actions/get-user-work-assignments.md) | `GET /users/:uid/workAssignments` | [docs](https://www.actitime.com/api-documentation/users-resource) |
| [Get Workflow Status](actions/get-workflow-status.md) | `GET /workflowStatuses/:id` | [docs](https://www.actitime.com/api-documentation/workflow-statuses-resource) |
| [List Customer Assigned Users](actions/list-customer-assigned-users.md) | `GET /customers/:id/assignedUsers` | [docs](https://www.actitime.com/api-documentation/customers-resource) |
| [List Customer Comments](actions/list-customer-comments.md) | `GET /customers/:id/comments` | [docs](https://www.actitime.com/api-documentation/customers-resource) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.actitime.com/api-documentation/customers-resource) |
| [List Departments](actions/list-departments.md) | `GET /departments` | [docs](https://www.actitime.com/api-documentation/departments-resource) |
| [List Leave Types](actions/list-leave-types.md) | `GET /leaveTypes` | [docs](https://www.actitime.com/api-documentation/leave-types-resource) |
| [List Project Assigned Users](actions/list-project-assigned-users.md) | `GET /projects/:id/assignedUsers` | [docs](https://www.actitime.com/api-documentation/projects-resource) |
| [List Project Comments](actions/list-project-comments.md) | `GET /projects/:id/comments` | [docs](https://www.actitime.com/api-documentation/projects-resource) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.actitime.com/api-documentation/projects-resource) |
| [List Task Assigned Users](actions/list-task-assigned-users.md) | `GET /tasks/:id/assignedUsers` | [docs](https://www.actitime.com/api-documentation/tasks-resource) |
| [List Task Comments](actions/list-task-comments.md) | `GET /tasks/:id/comments` | [docs](https://www.actitime.com/api-documentation/tasks-resource) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://www.actitime.com/api-documentation/tasks-resource) |
| [List Time Zone Groups](actions/list-time-zone-groups.md) | `GET /timeZoneGroups` | [docs](https://www.actitime.com/api-documentation/time-zone-groups-resource) |
| [List Types of Work](actions/list-types-of-work.md) | `GET /typesOfWork` | [docs](https://www.actitime.com/api-documentation/types-of-work-resource) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://www.actitime.com/api-documentation/users-resource) |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | `GET /workflowStatuses` | [docs](https://www.actitime.com/api-documentation/workflow-statuses-resource) |

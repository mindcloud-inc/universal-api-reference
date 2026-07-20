# Planfix: Native API Reference

A consolidated summary of Planfix's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://help.planfix.com/restapidocs/
- **OpenAPI specification:** https://help.planfix.com/restapidocs/swagger.json
- **API base URL:** `{accountBaseUrl}/rest`

## Authentication

### API Key

Connect to Planfix with a REST API token and your account base URL.

### Credentials

- **API Key:** `apiKey` · required
- **Account Base URL:** `accountBaseUrl` · required · Your Planfix workspace URL without /rest, for example https://your-account.planfix.com

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://planfix.com/help/Account_Management)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `tasks`.

## Filtering

Send filters in the request body. Supported operators: `eq`, `gt`, `lt`, `ne`.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Task Comment](actions/add-task-comment.md) | `POST /task/:id/comments/` | [docs](https://help.planfix.com/restapidocs/#/Task/post-task-add-comment) |
| [Create Contact](actions/create-contact.md) | `POST /contact/` | [docs](https://help.planfix.com/restapidocs/#/Contact/post-contact) |
| [Create Project](actions/create-project.md) | `POST /project/` | [docs](https://help.planfix.com/restapidocs/#/Project/post-project) |
| [Create Task](actions/create-task.md) | `POST /task/` | [docs](https://help.planfix.com/restapidocs/#/Task/post-task) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /comment/:id` | [docs](https://help.planfix.com/restapidocs/#/Comments/delete-comment-id) |
| [Get Comment](actions/get-comment.md) | `GET /comment/:id` | [docs](https://help.planfix.com/restapidocs/#/Comments/get-comment-id) |
| [Get Contact](actions/get-contact.md) | `GET /contact/:id` | [docs](https://help.planfix.com/restapidocs/#/Contact/get-contact-by-id) |
| [Get Employee](actions/get-employee.md) | `GET /user/:id` | [docs](https://help.planfix.com/restapidocs/#/Employee/get-user-id) |
| [Get Project](actions/get-project.md) | `GET /project/:id` | [docs](https://help.planfix.com/restapidocs/#/Project/get-project-by-id) |
| [Get Task](actions/get-task.md) | `GET /task/:id` | [docs](https://help.planfix.com/restapidocs/#/Task/get-task-by-id) |
| [List Contact Filters](actions/list-contact-filters.md) | `POST /contact/filters` | [docs](https://help.planfix.com/restapidocs/#/Contact/post-contact-filters) |
| [List Contact Templates](actions/list-contact-templates.md) | `GET /contact/templates` | [docs](https://help.planfix.com/restapidocs/#/Contact/get-contact-list-templates) |
| [List Contacts](actions/list-contacts.md) | `POST /contact/list` | [docs](https://help.planfix.com/restapidocs/#/Contact/get-contact-list) |
| [List Employees](actions/list-employees.md) | `POST /user/list` | [docs](https://help.planfix.com/restapidocs/#/Employee/get-user-list) |
| [List Projects](actions/list-projects.md) | `POST /project/list` | [docs](https://help.planfix.com/restapidocs/#/Project/get-project-list) |
| [List Task Comments](actions/list-task-comments.md) | `POST /task/:id/comments/list` | [docs](https://help.planfix.com/restapidocs/#/Task/get-task-comments) |
| [List Task Filters](actions/list-task-filters.md) | `POST /task/filters` | [docs](https://help.planfix.com/restapidocs/#/Task/post-task-filters) |
| [List Tasks](actions/list-tasks.md) | `POST /task/list` | [docs](https://help.planfix.com/restapidocs/#/Task/get-task-list) |
| [Update Contact](actions/update-contact.md) | `POST /contact/:id` | [docs](https://help.planfix.com/restapidocs/#/Contact/post-contact-by-id) |
| [Update Project](actions/update-project.md) | `POST /project/:id` | [docs](https://help.planfix.com/restapidocs/#/Project/post-project-by-id) |
| [Update Task](actions/update-task.md) | `POST /task/:id` | [docs](https://help.planfix.com/restapidocs/#/Task/post-task-by-id) |

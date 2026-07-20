# Formitize: Native API Reference

A consolidated summary of Formitize's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://mitechnologies.github.io/Formitize-NET-API/
- **API base URL:** `https://service.formitize.com/api/rest/v2`

## Authentication

### API Token

Connect with a Formitize API token and send it as a Bearer Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.formitize.com/support/solutions/articles/4000206804-getting-creating-an-api-token-in-order-to-access-data)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON. The current page number is read from `page`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Client](actions/add-client.md) | `POST /crm/client/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Add Contact](actions/add-contact.md) | `POST /crm/client/:clientID/contact/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Add Job](actions/add-job.md) | `POST /job/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Create Task](actions/create-task.md) | `POST /crm/task/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Delete Client](actions/delete-client.md) | `DELETE /crm/client/:clientID` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /crm/client/:id/contact/:contactID` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Delete Job](actions/delete-job.md) | `DELETE /job/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Delete Task](actions/delete-task.md) | `DELETE /crm/task/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Edit Client](actions/edit-client.md) | `POST /crm/client/:clientID` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Edit Contact](actions/edit-contact.md) | `POST /crm/client/:id/contact/:contactID` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Edit Job](actions/edit-job.md) | `POST /job/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Client](actions/get-client.md) | `GET /crm/client/:clientID` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Contact](actions/get-contact.md) | `GET /crm/client/:clientID/contact/:contactID` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Form Template](actions/get-form-template.md) | `GET /form/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Job](actions/get-job.md) | `GET /job/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Job History](actions/get-job-history.md) | `GET /job/:id/history` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Submitted Form](actions/get-submitted-form.md) | `GET /form/submit/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Get Task](actions/get-task.md) | `GET /crm/task/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [List Clients](actions/list-clients.md) | `GET /crm/client/list/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [List Contacts](actions/list-contacts.md) | `GET /crm/client/:clientID/contact/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [List Jobs](actions/list-jobs.md) | `GET /job/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [List Submitted Forms](actions/list-submitted-forms.md) | `GET /form/submit/list` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [List Tasks](actions/list-tasks.md) | `GET /crm/task/` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [List Templates](actions/list-templates.md) | `GET /form/list` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |
| [Update Task](actions/update-task.md) | `POST /crm/task/:id` | [docs](https://mitechnologies.github.io/Formitize-NET-API/) |

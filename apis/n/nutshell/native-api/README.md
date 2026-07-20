# Nutshell: Native API Reference

A consolidated summary of Nutshell's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developers.nutshell.com/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/g4umb1chmkya32ai
- **API base URL:** `https://app.nutshell.com/rest`

## Authentication

### Basic Auth

Authenticate with a Nutshell user email as the username and a Nutshell API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.nutshell.com/guides/authentication)

## Pagination

Use `page[limit]` in the query string to set the page size. Use `page[page]` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Company](actions/create-company.md) | `POST /accounts` | [docs](https://developers.nutshell.com/reference) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://developers.nutshell.com/reference) |
| [Create Lead](actions/create-lead.md) | `POST /leads` | [docs](https://developers.nutshell.com/reference) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://developers.nutshell.com/reference) |
| [Create Task](actions/create-task.md) | `POST /tasks` | [docs](https://developers.nutshell.com/reference) |
| [Get Company](actions/get-company.md) | `GET /accounts/:id` | [docs](https://developers.nutshell.com/reference) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://developers.nutshell.com/reference) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:id` | [docs](https://developers.nutshell.com/reference) |
| [Get Task](actions/get-task.md) | `GET /tasks/:id` | [docs](https://developers.nutshell.com/reference) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://developers.nutshell.com/reference) |
| [List Companies](actions/list-companies.md) | `GET /accounts` | [docs](https://developers.nutshell.com/reference) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://developers.nutshell.com/reference) |
| [List Lead Stages](actions/list-lead-stages.md) | `GET /leads/:id/stages` | [docs](https://developers.nutshell.com/reference) |
| [List Leads](actions/list-leads.md) | `GET /leads` | [docs](https://developers.nutshell.com/reference) |
| [List Notes](actions/list-notes.md) | `GET /notes` | [docs](https://developers.nutshell.com/reference) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://developers.nutshell.com/reference) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://developers.nutshell.com/reference) |
| [Reopen Lead](actions/reopen-lead.md) | `POST /leads/:id/reopen` | [docs](https://developers.nutshell.com/reference) |
| [Set Lead Pipeline](actions/set-lead-pipeline.md) | `POST /leads/:id/stageset` | [docs](https://developers.nutshell.com/reference) |
| [Update Company](actions/update-company.md) | `PATCH /accounts/:id` | [docs](https://developers.nutshell.com/reference) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://developers.nutshell.com/reference) |
| [Update Lead](actions/update-lead.md) | `PATCH /leads/:id` | [docs](https://developers.nutshell.com/reference) |
| [Update Lead Status](actions/update-lead-status.md) | `POST /leads/:id/status` | [docs](https://developers.nutshell.com/reference) |
| [Update Task](actions/update-task.md) | `PATCH /tasks/:id` | [docs](https://developers.nutshell.com/reference) |

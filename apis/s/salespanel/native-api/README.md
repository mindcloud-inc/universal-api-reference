# Salespanel: Native API Reference

A consolidated summary of Salespanel's API configuration and 8 documented operations, with links to official documentation.

- **Official docs:** https://salespanel.io/docs/
- **API base URL:** `https://salespanel.io/api/v1`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://salespanel.io/docs/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (8 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Identify Contact](actions/identify-contact.md) | `POST /contacts/:contact_id/identify/` | [docs](https://salespanel.io/docs/#identify-contact) |
| [List Contact Activities](actions/list-contact-activities.md) | `GET /contacts/:contact_id/activities/` | [docs](https://salespanel.io/docs/#retrieve-activities-of-a-contact) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts/` | [docs](https://salespanel.io/docs/#get-all-contacts) |
| [List Leads](actions/list-leads.md) | `GET /leads/` | [docs](https://salespanel.io/docs/#get-all-leads) |
| [List Visiting Companies](actions/list-visiting-companies.md) | `GET /visiting-companies/` | [docs](https://salespanel.io/docs/#get-all-visiting-companies) |
| [Log Custom Activity](actions/log-custom-activity.md) | `POST /custom-activity/create/` | [docs](https://salespanel.io/docs/#log-a-custom-activity) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/:contact_id/` | [docs](https://salespanel.io/docs/#retrieve-contact) |
| [Set Visitor Attributes](actions/set-visitor-attributes.md) | `POST /visitor-attributes/` | [docs](https://salespanel.io/docs/#set-visitor-attributes) |

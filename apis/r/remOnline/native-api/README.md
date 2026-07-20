# RemOnline: Native API Reference

A consolidated summary of RemOnline's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://roapp.readme.io/reference
- **API base URL:** `https://api.roapp.io`

## Authentication

### API key

Authenticate with an RO App API key from Settings > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.roapp.io/en/articles/3393227-api-general-information)

## API conventions

Responses from this API use JSON.

## Pagination

Use `pageSize` in the query string to set the page size (default 50; accepted range 10–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Organization](actions/create-organization.md) | `POST /v2/contacts/organizations` | [docs](https://roappua.readme.io/reference/create-organization) |
| [Create Person](actions/create-person.md) | `POST /v2/contacts/people` | [docs](https://roappua.readme.io/reference/create-person) |
| [Get Company Information](actions/get-company-information.md) | `GET /v2/company` | [docs](https://roappua.readme.io/reference/get-company-information) |
| [Get Company Settings](actions/get-company-settings.md) | `GET /settings/company` | [docs](https://roappua.readme.io/reference/get-company-settings) |
| [Get Organization By ID](actions/get-organization-by-id.md) | `GET /v2/contacts/organizations/:organization_id` | [docs](https://roappua.readme.io/reference/get-organization-by-id) |
| [Get Person By ID](actions/get-person-by-id.md) | `GET /v2/contacts/people/:person_id` | [docs](https://roappua.readme.io/reference/get-person-by-id) |
| [List Bookings](actions/list-bookings.md) | `GET /v2/bookings` | [docs](https://roappua.readme.io/reference/get-bookings) |
| [List Estimate Statuses](actions/list-estimate-statuses.md) | `GET /estimates/statuses` | [docs](https://roappua.readme.io/reference/get-estimate-statuses) |
| [List Estimates](actions/list-estimates.md) | `GET /estimates` | [docs](https://roappua.readme.io/reference/get-estimates) |
| [List Invoices](actions/list-invoices.md) | `GET /v2/invoices` | [docs](https://roappua.readme.io/reference/get-invoices) |
| [List Order Statuses](actions/list-order-statuses.md) | `GET /orders/statuses` | [docs](https://roappua.readme.io/reference/get-order-statuses) |
| [List Orders](actions/list-orders.md) | `GET /orders` | [docs](https://roappua.readme.io/reference/get-orders) |
| [List Organizations](actions/list-organizations.md) | `GET /v2/contacts/organizations` | [docs](https://roappua.readme.io/reference/get-organizations) |
| [List People](actions/list-people.md) | `GET /v2/contacts/people` | [docs](https://roappua.readme.io/reference/get-people) |
| [Update Organization](actions/update-organization.md) | `PATCH /v2/contacts/organizations/:organization_id` | [docs](https://roappua.readme.io/reference/update-organization) |
| [Update Person](actions/update-person.md) | `PATCH /v2/contacts/people/:person_id` | [docs](https://roappua.readme.io/reference/update-person) |

# GorillaDesk: Native API Reference

A consolidated summary of GorillaDesk's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://api.gorilladesk.com
- **OpenAPI specification:** https://api.gorilladesk.com/v1/specs
- **API base URL:** `https://api.gorilladesk.com/v1`

## Authentication

### API Key

Connect GorillaDesk with an API key generated from the Addons page.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.gorilladesk.com)

## API conventions

Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Multiple sort fields can be combined.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Customer](actions/create-customer.md) | `POST /customers` | [docs](https://api.gorilladesk.com) |
| [Create Customer Note](actions/create-customer-note.md) | `POST /customers/:customerId/notes` | [docs](https://api.gorilladesk.com) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://api.gorilladesk.com) |
| [List Phone Types](actions/list-phone-types.md) | `GET /phone-types` | [docs](https://api.gorilladesk.com) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://api.gorilladesk.com) |
| [Retrieve Company](actions/retrieve-company.md) | `GET /company` | [docs](https://api.gorilladesk.com) |
| [Retrieve Customer](actions/retrieve-customer.md) | `GET /customers/:customerId` | [docs](https://api.gorilladesk.com) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/:userId` | [docs](https://api.gorilladesk.com) |
| [Update Customer](actions/update-customer.md) | `PUT /customers/:customerId` | [docs](https://api.gorilladesk.com) |

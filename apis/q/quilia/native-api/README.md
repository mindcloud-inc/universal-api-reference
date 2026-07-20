# Quilia: Native API Reference

A consolidated summary of Quilia's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://api.quilia.dev/v2
- **OpenAPI specification:** https://api.quilia.dev/v2/openapi
- **API base URL:** `https://api.quilia.dev/v2`

## Authentication

### API Key

Authenticate Quilia API requests with a bearer API key created in the Quilia portal.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.quilia.dev/v2)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 10; minimum 0). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Appointment](actions/create-appointment.md) | `POST appointments` | [docs](https://api.quilia.dev/v2#tag/appointments/POST/appointments) |
| [Create Case](actions/create-case.md) | `POST cases` | [docs](https://api.quilia.dev/v2#tag/cases/POST/cases) |
| [Create Client](actions/create-client.md) | `POST clients` | [docs](https://api.quilia.dev/v2#tag/clients/POST/clients) |
| [Create Contact](actions/create-contact.md) | `POST contacts` | [docs](https://api.quilia.dev/v2#tag/contacts/POST/contacts) |
| [Delete Appointment](actions/delete-appointment.md) | `DELETE appointments/:id` | [docs](https://api.quilia.dev/v2#tag/appointments/DELETE/appointments/%7Bid%7D) |
| [Delete Case](actions/delete-case.md) | `DELETE cases/:id` | [docs](https://api.quilia.dev/v2#tag/cases/DELETE/cases/%7Bid%7D) |
| [Delete Client](actions/delete-client.md) | `DELETE clients/:id` | [docs](https://api.quilia.dev/v2#tag/clients/DELETE/clients/%7Bid%7D) |
| [Delete Contact](actions/delete-contact.md) | `DELETE contacts/:id` | [docs](https://api.quilia.dev/v2#tag/contacts/DELETE/contacts/%7Bid%7D) |
| [Get Appointment](actions/get-appointment.md) | `GET appointments/:id` | [docs](https://api.quilia.dev/v2#tag/appointments/GET/appointments/%7Bid%7D) |
| [Get Case](actions/get-case.md) | `GET cases/:id` | [docs](https://api.quilia.dev/v2#tag/cases/GET/cases/%7Bid%7D) |
| [Get Contact](actions/get-contact.md) | `GET contacts/:id` | [docs](https://api.quilia.dev/v2#tag/contacts/GET/contacts/%7Bid%7D) |
| [Get Current API Key Information](actions/get-current-api-key-information.md) | `GET auth/whoami` | [docs](https://api.quilia.dev/v2#tag/auth/GET/auth/whoami) |
| [List Case Types](actions/list-case-types.md) | `GET cases/casetypes` | [docs](https://api.quilia.dev/v2#tag/cases/GET/cases/casetypes) |
| [List Cases](actions/list-cases.md) | `GET cases` | [docs](https://api.quilia.dev/v2#tag/cases/GET/cases) |
| [List Clients](actions/list-clients.md) | `GET clients` | [docs](https://api.quilia.dev/v2#tag/clients/GET/clients) |
| [Lookup Client By Email Or Phone](actions/lookup-client-by-email-or-phone.md) | `GET clients/lookup` | [docs](https://api.quilia.dev/v2#tag/clients/GET/clients/lookup) |
| [Update Appointment](actions/update-appointment.md) | `PATCH appointments/:id` | [docs](https://api.quilia.dev/v2#tag/appointments/PATCH/appointments/%7Bid%7D) |
| [Update Case Details](actions/update-case-details.md) | `PATCH cases/:id` | [docs](https://api.quilia.dev/v2#tag/cases/PATCH/cases/%7Bid%7D) |
| [Update Case Phase](actions/update-case-phase.md) | `PATCH cases/:id/phase` | [docs](https://api.quilia.dev/v2#tag/cases/PATCH/cases/%7Bid%7D/phase) |
| [Update Client Information](actions/update-client-information.md) | `PATCH clients/:id` | [docs](https://api.quilia.dev/v2#tag/clients/PATCH/clients/%7Bid%7D) |
| [Update Contact](actions/update-contact.md) | `PATCH contacts/:id` | [docs](https://api.quilia.dev/v2#tag/contacts/PATCH/contacts/%7Bid%7D) |

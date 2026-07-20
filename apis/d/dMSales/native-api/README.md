# DMSales: Native API Reference

A consolidated summary of DMSales's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://app.dmsales.com/api-doc/default
- **OpenAPI specification:** https://app.dmsales.com/api-doc/default
- **API base URL:** `https://app.dmsales.com`

## Authentication

### API key

Authenticate DMSales requests with a Bearer API token.

### Credentials

- **API Key:** `apiKey` · required
- **Project ID:** `projectId` · required · DMSales project UUID used as the default project scope for project-based endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dmsales.com/pomoc/jak-wygenerowac-klucz-api/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact Note](actions/add-contact-note.md) | `POST /api/contact-card/add-note` | [docs](https://app.dmsales.com/api-doc/default) |
| [Add Custom Event](actions/add-custom-event.md) | `POST /api/events/add-custom-event` | [docs](https://app.dmsales.com/api-doc/default) |
| [Autocomplete Contact Tags](actions/autocomplete-contact-tags.md) | `GET /api/contact-card/autocomplete-tags` | [docs](https://app.dmsales.com/api-doc/default) |
| [Create Project](actions/create-project.md) | `POST /api/project/create` | [docs](https://app.dmsales.com/api-doc/default) |
| [Create Segment](actions/create-segment.md) | `POST /api/segment/create` | [docs](https://app.dmsales.com/api-doc/default) |
| [Delete Contact Note](actions/delete-contact-note.md) | `DELETE /api/contact-card/delete-note` | [docs](https://app.dmsales.com/api-doc/default) |
| [Edit Contact Note](actions/edit-contact-note.md) | `POST /api/contact-card/edit-note` | [docs](https://app.dmsales.com/api-doc/default) |
| [Get Contact](actions/get-contact.md) | `GET /api/contact-card/` | [docs](https://app.dmsales.com/api-doc/default) |
| [Get Contact Involvement](actions/get-contact-involvement.md) | `GET /api/contact-card/involvement` | [docs](https://app.dmsales.com/api-doc/default) |
| [Get Current User](actions/get-current-user.md) | `GET /api/user/me` | [docs](https://app.dmsales.com/api-doc/default) |
| [Get Refer Score Report ID](actions/get-refer-score-report-id.md) | `GET /api/person/get-refer-score-report-id` | [docs](https://app.dmsales.com/api-doc/default) |
| [Get Wallet Points](actions/get-wallet-points.md) | `GET /api/user/wallet/points` | [docs](https://app.dmsales.com/api-doc/default) |
| [List Contact Events](actions/list-contact-events.md) | `GET /api/contact-card/events` | [docs](https://app.dmsales.com/api-doc/default) |
| [List Contact Statuses](actions/list-contact-statuses.md) | `GET /api/contact-card/available-contact-statuses` | [docs](https://app.dmsales.com/api-doc/default) |
| [List Contacts](actions/list-contacts.md) | `GET /api/persons/list` | [docs](https://app.dmsales.com/api-doc/default) |
| [List Projects](actions/list-projects.md) | `GET /api/project/list` | [docs](https://app.dmsales.com/api-doc/default) |
| [List Searches](actions/list-searches.md) | `GET /api/search/list` | [docs](https://app.dmsales.com/api-doc/default) |
| [List Segments](actions/list-segments.md) | `GET /api/segment/list` | [docs](https://app.dmsales.com/api-doc/default) |

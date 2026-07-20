# redirect.pizza: Native API Reference

A consolidated summary of redirect.pizza's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://redirect.pizza/docs
- **OpenAPI specification:** https://redirect.pizza/api-docs/openapi.yaml
- **API base URL:** `https://redirect.pizza`

## Authentication

### API Key

Use a redirect.pizza API token from the account API tab.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://redirect.pizza/support/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `meta.next_cursor`. The total page count is read from `meta.last_page`. The current page number is read from `meta.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 20; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Apply Automatic DNS](actions/apply-automatic-dns.md) | `POST /api/v1/domains/{id}/automatic-dns` | [docs](https://redirect.pizza/docs) |
| [Check Domain DNS](actions/check-domain-dns.md) | `POST /api/v1/domains/{id}/check-dns` | [docs](https://redirect.pizza/docs) |
| [Create Email Forward](actions/create-email-forward.md) | `POST /api/v1/email-forwards` | [docs](https://redirect.pizza/docs) |
| [Create Redirect](actions/create-redirect.md) | `POST /api/v1/redirects` | [docs](https://redirect.pizza/docs) |
| [Delete Email Forward](actions/delete-email-forward.md) | `DELETE /api/v1/email-forwards/{id}` | [docs](https://redirect.pizza/docs) |
| [Delete Redirect](actions/delete-redirect.md) | `DELETE /api/v1/redirects/{id}` | [docs](https://redirect.pizza/docs) |
| [Generate QR Code](actions/generate-qr-code.md) | `GET /api/v1/qr` | [docs](https://redirect.pizza/docs) |
| [Get Analytics Dimension](actions/get-analytics-dimension.md) | `GET /api/v1/analytics/dimensions/{dimension}` | [docs](https://redirect.pizza/docs) |
| [Get Analytics Hits](actions/get-analytics-hits.md) | `GET /api/v1/analytics/hits` | [docs](https://redirect.pizza/docs) |
| [Get Analytics Raw Hits](actions/get-analytics-raw-hits.md) | `GET /api/v1/analytics/raw` | [docs](https://redirect.pizza/docs) |
| [Get Analytics Time Series](actions/get-analytics-time-series.md) | `GET /api/v1/analytics/time-series` | [docs](https://redirect.pizza/docs) |
| [Get Domain](actions/get-domain.md) | `GET /api/v1/domains/{id}` | [docs](https://redirect.pizza/docs) |
| [Get Email Forward](actions/get-email-forward.md) | `GET /api/v1/email-forwards/{id}` | [docs](https://redirect.pizza/docs) |
| [Get Redirect](actions/get-redirect.md) | `GET /api/v1/redirects/{id}` | [docs](https://redirect.pizza/docs) |
| [Get Team Details](actions/get-team-details.md) | `GET /api/v1/team` | [docs](https://redirect.pizza/docs) |
| [List Domains](actions/list-domains.md) | `GET /api/v1/domains` | [docs](https://redirect.pizza/docs) |
| [List Email Forwards](actions/list-email-forwards.md) | `GET /api/v1/email-forwards` | [docs](https://redirect.pizza/docs) |
| [List Redirects](actions/list-redirects.md) | `GET /api/v1/redirects` | [docs](https://redirect.pizza/docs) |
| [Test Redirects](actions/test-redirects.md) | `GET /api/v1/tester` | [docs](https://redirect.pizza/docs) |
| [Update Email Forward](actions/update-email-forward.md) | `PUT /api/v1/email-forwards/{id}` | [docs](https://redirect.pizza/docs) |
| [Update Redirect](actions/update-redirect.md) | `PUT /api/v1/redirects/{id}` | [docs](https://redirect.pizza/docs) |

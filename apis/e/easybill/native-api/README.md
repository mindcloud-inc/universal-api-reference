# easybill: Native API Reference

A consolidated summary of easybill's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://www.easybill.de/api/
- **OpenAPI specification:** https://api.easybill.de/rest/v1/swagger.json
- **API base URL:** `https://api.easybill.de/rest/v1`

## Authentication

### API Key

Authenticate easybill REST API requests with the tenant API key using the Authorization bearer-token header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.easybill.de/hc/de/articles/115003808529-API-Key-REST-Schnittstelle)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `string` | no | Maximum number of results to return. easybill defaults to 100 and allows up to 1000. |
| `page` | query | `string` | no | Page number to request. easybill list endpoints start at page 1. |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Attachment](actions/get-attachment.md) | `GET /attachments/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Customer](actions/get-customer.md) | `GET /customers/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Document](actions/get-document.md) | `GET /documents/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Login](actions/get-login.md) | `GET /logins/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Position](actions/get-position.md) | `GET /positions/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Position Discount](actions/get-position-discount.md) | `GET /discounts/position/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Position Group](actions/get-position-group.md) | `GET /position-groups/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Position Group Discount](actions/get-position-group-discount.md) | `GET /discounts/position-group/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Post Box](actions/get-post-box.md) | `GET /post-boxes/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Project](actions/get-project.md) | `GET /projects/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Serial Number](actions/get-serial-number.md) | `GET /serial-numbers/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Stock](actions/get-stock.md) | `GET /stocks/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Task](actions/get-task.md) | `GET /tasks/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Text Template](actions/get-text-template.md) | `GET /text-templates/{id}` | [docs](https://www.easybill.de/api/) |
| [Get Time Tracking](actions/get-time-tracking.md) | `GET /time-trackings/{id}` | [docs](https://www.easybill.de/api/) |
| [Get WebHook](actions/get-web-hook.md) | `GET /webhooks/{id}` | [docs](https://www.easybill.de/api/) |
| [List Attachments](actions/list-attachments.md) | `GET /attachments` | [docs](https://www.easybill.de/api/) |
| [List Customers](actions/list-customers.md) | `GET /customers` | [docs](https://www.easybill.de/api/) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://www.easybill.de/api/) |
| [List Logins](actions/list-logins.md) | `GET /logins` | [docs](https://www.easybill.de/api/) |
| [List PDF Templates](actions/list-pdf-templates.md) | `GET /pdf-templates` | [docs](https://www.easybill.de/api/) |
| [List Position Discounts](actions/list-position-discounts.md) | `GET /discounts/position` | [docs](https://www.easybill.de/api/) |
| [List Position Group Discounts](actions/list-position-group-discounts.md) | `GET /discounts/position-group` | [docs](https://www.easybill.de/api/) |
| [List Position Groups](actions/list-position-groups.md) | `GET /position-groups` | [docs](https://www.easybill.de/api/) |
| [List Positions](actions/list-positions.md) | `GET /positions` | [docs](https://www.easybill.de/api/) |
| [List Post Boxes](actions/list-post-boxes.md) | `GET /post-boxes` | [docs](https://www.easybill.de/api/) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://www.easybill.de/api/) |
| [List Serial Numbers](actions/list-serial-numbers.md) | `GET /serial-numbers` | [docs](https://www.easybill.de/api/) |
| [List Stocks](actions/list-stocks.md) | `GET /stocks` | [docs](https://www.easybill.de/api/) |
| [List Tasks](actions/list-tasks.md) | `GET /tasks` | [docs](https://www.easybill.de/api/) |
| [List Text Templates](actions/list-text-templates.md) | `GET /text-templates` | [docs](https://www.easybill.de/api/) |
| [List Time Trackings](actions/list-time-trackings.md) | `GET /time-trackings` | [docs](https://www.easybill.de/api/) |
| [List WebHooks](actions/list-web-hooks.md) | `GET /webhooks` | [docs](https://www.easybill.de/api/) |

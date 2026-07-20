# Ship24: Native API Reference

A consolidated summary of Ship24's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://docs.ship24.com/
- **OpenAPI specification:** https://docs.ship24.com/assets/openapi/ship24-tracking-api.yaml
- **API base URL:** `https://api.ship24.com`

## Authentication

### API Key

Authenticate Ship24 requests with a dashboard-generated API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ship24.com/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–500). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 1 after each failed attempt.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Create Trackers](actions/bulk-create-trackers.md) | `POST /public/v1/trackers/bulk` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/bulk-create-trackers) |
| [Create Tracker](actions/create-tracker.md) | `POST /public/v1/trackers` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/create-tracker) |
| [Create Tracker And Get Results](actions/create-tracker-and-get-results.md) | `POST /public/v1/trackers/track` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/create-tracker-and-get-tracking-results) |
| [Get Tracker By Client Tracker ID](actions/get-tracker-by-client-tracker-id.md) | `GET /public/v1/trackers/:trackerId` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracker-by-trackerId) |
| [Get Tracker By Tracker ID](actions/get-tracker-by-tracker-id.md) | `GET /public/v1/trackers/:trackerId` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracker-by-trackerId) |
| [Get Tracker Results By Client Tracker ID](actions/get-tracker-results-by-client-tracker-id.md) | `GET /public/v1/trackers/:trackerId/results` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking-results-of-tracker-by-trackerId) |
| [Get Tracker Results By Tracker ID](actions/get-tracker-results-by-tracker-id.md) | `GET /public/v1/trackers/:trackerId/results` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking-results-of-tracker-by-trackerId) |
| [Get Tracker Results By Tracking Number](actions/get-tracker-results-by-tracking-number.md) | `GET /public/v1/trackers/search/{trackingNumber}/results` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking-results-of-trackers-by-tracking-number) |
| [Get Tracking Results by Tracking Number](actions/get-tracking-results-by-tracking-number.md) | `POST /public/v1/tracking/search` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking) |
| [List Couriers](actions/list-couriers.md) | `GET /public/v1/couriers` | [docs](https://docs.ship24.com/couriers) |
| [List Trackers](actions/list-trackers.md) | `GET /public/v1/trackers` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/list-trackers) |
| [Resend Tracker Webhook Events](actions/resend-tracker-webhook-events.md) | `POST /public/v1/trackers/:trackerId/webhook-events/resend` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/resend-webhooks) |
| [Update Tracker](actions/update-tracker.md) | `PATCH /public/v1/trackers/:trackerId` | [docs](https://docs.ship24.com/tracking-api-reference/#/operations/update-tracker-by-trackerId) |

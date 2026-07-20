# Hookdeck: Native API Reference

A consolidated summary of Hookdeck's API configuration and 27 documented operations, with links to official documentation.

- **Official docs:** https://hookdeck.com/docs/api.md
- **OpenAPI specification:** https://api.hookdeck.com/2025-07-01/openapi
- **API base URL:** `https://api.hookdeck.com/2025-07-01`

## Authentication

### API Key

Use a Hookdeck project API key from project settings. Hookdeck supports Bearer token authentication and deprecates Basic authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://hookdeck.com/docs/api.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `models`. The next-page cursor is read from `pagination.next`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–250). Use `next` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`, `gt`, `gte`, `lt`, `lte`.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `dir`. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (27 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Event](actions/cancel-event.md) | `PUT /events/:id/cancel` | [docs](https://hookdeck.com/docs/api/inspect.md#events) |
| [Create Connection](actions/create-connection.md) | `POST /connections` | [docs](https://hookdeck.com/docs/api/connections.md#create-a-connection) |
| [Create Destination](actions/create-destination.md) | `POST /destinations` | [docs](https://hookdeck.com/docs/api/destinations.md#create-a-destination) |
| [Create Source](actions/create-source.md) | `POST /sources` | [docs](https://hookdeck.com/docs/api/sources.md#create-a-source) |
| [Delete Connection](actions/delete-connection.md) | `DELETE /connections/:id` | [docs](https://hookdeck.com/docs/api/connections.md#delete-a-connection) |
| [Delete Destination](actions/delete-destination.md) | `DELETE /destinations/:id` | [docs](https://hookdeck.com/docs/api/destinations.md#delete-a-destination) |
| [Delete Source](actions/delete-source.md) | `DELETE /sources/:id` | [docs](https://hookdeck.com/docs/api/sources.md#delete-a-source) |
| [Get Connection](actions/get-connection.md) | `GET /connections/:id` | [docs](https://hookdeck.com/docs/api/connections.md#retrieve-a-connection) |
| [Get Connections](actions/get-connections.md) | `GET /connections` | [docs](https://hookdeck.com/docs/api/connections.md#retrieve-all-connections) |
| [Get Destination](actions/get-destination.md) | `GET /destinations/:id` | [docs](https://hookdeck.com/docs/api/destinations.md#retrieve-a-destination) |
| [Get Destinations](actions/get-destinations.md) | `GET /destinations` | [docs](https://hookdeck.com/docs/api/destinations.md#retrieve-all-destinations) |
| [Get Event](actions/get-event.md) | `GET /events/:id` | [docs](https://hookdeck.com/docs/api/inspect.md#events) |
| [Get Events](actions/get-events.md) | `GET /events` | [docs](https://hookdeck.com/docs/api/inspect.md#events) |
| [Get Issue](actions/get-issue.md) | `GET /issues/:id` | [docs](https://hookdeck.com/docs/api/inspect.md#issues) |
| [Get Issues](actions/get-issues.md) | `GET /issues` | [docs](https://hookdeck.com/docs/api/inspect.md#issues) |
| [Get Request](actions/get-request.md) | `GET /requests/:id` | [docs](https://hookdeck.com/docs/api/inspect.md#requests) |
| [Get Request Events](actions/get-request-events.md) | `GET /requests/:id/events` | [docs](https://hookdeck.com/docs/api/inspect.md#requests) |
| [Get Requests](actions/get-requests.md) | `GET /requests` | [docs](https://hookdeck.com/docs/api/inspect.md#requests) |
| [Get Source](actions/get-source.md) | `GET /sources/:id` | [docs](https://hookdeck.com/docs/api/sources.md#retrieve-a-source) |
| [Get Sources](actions/get-sources.md) | `GET /sources` | [docs](https://hookdeck.com/docs/api/sources.md#retrieve-all-sources) |
| [Pause Connection](actions/pause-connection.md) | `PUT /connections/:id/pause` | [docs](https://hookdeck.com/docs/api/connections.md#pause-a-connection) |
| [Retry Event](actions/retry-event.md) | `POST /events/:id/retry` | [docs](https://hookdeck.com/docs/api/inspect.md#events) |
| [Retry Request](actions/retry-request.md) | `POST /requests/:id/retry` | [docs](https://hookdeck.com/docs/api/inspect.md#requests) |
| [Unpause Connection](actions/unpause-connection.md) | `PUT /connections/:id/unpause` | [docs](https://hookdeck.com/docs/api/connections.md#unpause-a-connection) |
| [Update Connection](actions/update-connection.md) | `PUT /connections/:id` | [docs](https://hookdeck.com/docs/api/connections.md#update-a-connection) |
| [Update Destination](actions/update-destination.md) | `PUT /destinations/:id` | [docs](https://hookdeck.com/docs/api/destinations.md#update-a-destination) |
| [Update Source](actions/update-source.md) | `PUT /sources/:id` | [docs](https://hookdeck.com/docs/api/sources.md#update-a-source) |

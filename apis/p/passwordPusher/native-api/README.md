# Password Pusher: Native API Reference

A consolidated summary of Password Pusher's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://eu.pwpush.com/help/api
- **API base URL:** `https://eu.pwpush.com/api/v2`

## Authentication

### API Key

Use a Password Pusher API token as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://eu.pwpush.com/help/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Close Request](actions/close-request.md) | `DELETE /requests/{{urlToken}}` | [docs](https://eu.pwpush.com/help/api/requests) |
| [Create Push](actions/create-push.md) | `POST /pushes` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [Create Request](actions/create-request.md) | `POST /requests` | [docs](https://eu.pwpush.com/help/api/requests) |
| [Expire Push](actions/expire-push.md) | `DELETE /pushes/{{urlToken}}` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [Get API Version](actions/get-api-version.md) | `GET /version` | [docs](https://eu.pwpush.com/help/api) |
| [Get Push Audit Log](actions/get-push-audit-log.md) | `GET /pushes/{{urlToken}}/audit` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [Get Request Audit Log](actions/get-request-audit-log.md) | `GET /requests/{{urlToken}}/audit` | [docs](https://eu.pwpush.com/help/api/requests) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://eu.pwpush.com/help/api/accounts) |
| [List Active Pushes](actions/list-active-pushes.md) | `GET /pushes/active` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [List Active Requests](actions/list-active-requests.md) | `GET /requests/active` | [docs](https://eu.pwpush.com/help/api/requests) |
| [List Closed Requests](actions/list-closed-requests.md) | `GET /requests/closed` | [docs](https://eu.pwpush.com/help/api/requests) |
| [List Expired Pushes](actions/list-expired-pushes.md) | `GET /pushes/expired` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [List Open Requests](actions/list-open-requests.md) | `GET /requests/open` | [docs](https://eu.pwpush.com/help/api/requests) |
| [List Ready Requests](actions/list-ready-requests.md) | `GET /requests/ready` | [docs](https://eu.pwpush.com/help/api/requests) |
| [Preview Push](actions/preview-push.md) | `GET /pushes/{{urlToken}}/preview` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [Preview Request](actions/preview-request.md) | `GET /requests/{{urlToken}}/preview` | [docs](https://eu.pwpush.com/help/api/requests) |
| [Respond To Request](actions/respond-to-request.md) | `PATCH /requests/{{urlToken}}/respond` | [docs](https://eu.pwpush.com/help/api/requests) |
| [Retrieve Push](actions/retrieve-push.md) | `GET /pushes/{{urlToken}}` | [docs](https://eu.pwpush.com/help/api/pushes) |
| [Retrieve Request](actions/retrieve-request.md) | `GET /requests/{{urlToken}}` | [docs](https://eu.pwpush.com/help/api/requests) |

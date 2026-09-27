# List Sales Navigator threads with ConnectSafely

List messaging threads from Sales Navigator. Requires active Sales Navigator subscription. Supports INBOX/UNREAD/ARCHIVED filtering. Note: GET /conversations automatically merges Sales Nav threads — use this endpoint only if you need Sales Nav-specific filtering (UNREAD/ARCHIVED).

## Endpoint

- **Method:** `GET`
- **Path:** `/sales-nav/threads`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [List Sales Navigator threads](https://connectsafely.ai/docs/api/linkedin-messaging/get-sales-nav-threads-sales-nav-list-threads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID |
| `count` | query | `number` | no | Number of threads Default: `20`. |
| `filter` | query | `list` | no | Thread filter Accepted values: `INBOX`, `UNREAD`, `ARCHIVED`. Default: `INBOX`. |
| `pageStartsAt` | query | `number` | no | Pagination offset |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `threads` | `array` |  |
| `paging` | `object` |  |
| `nextPageStartsAt` | `number` |  |
| `accountId` | `string` |  |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

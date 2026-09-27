# Mark Sales Navigator thread as read with ConnectSafely

Mark a Sales Navigator messaging thread as read.

## Endpoint

- **Method:** `POST`
- **Path:** `/sales-nav/mark-read`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Mark Sales Navigator thread as read](https://connectsafely.ai/docs/api/linkedin-messaging/post-sales-nav-mark-read-sales-nav-mark-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID |
| `threadId` | body | `string` | yes | Thread ID to mark as read |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `threadId` | `string` |  |
| `accountId` | `string` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

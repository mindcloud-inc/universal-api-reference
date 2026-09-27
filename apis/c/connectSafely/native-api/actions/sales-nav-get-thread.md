# Get Sales Navigator thread with messages with ConnectSafely

Get a single Sales Navigator thread with message history. Note: GET /conversations/{conversationUrn}/messages auto-detects Sales Nav URNs and serves the same data.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales-nav/threads/:threadId`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get Sales Navigator thread with messages](https://connectsafely.ai/docs/api/linkedin-messaging/get-sales-nav-threads-threadid-sales-nav-get-thread)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `threadId` | param | `string` | yes | Sales Navigator thread ID |
| `accountId` | query | `string` | no | LinkedIn account ID |
| `messageCount` | query | `number` | no | Number of messages Default: `20`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `thread` | `object` |  |
| `accountId` | `string` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

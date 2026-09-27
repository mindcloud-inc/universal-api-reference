# Send Sales Navigator message with ConnectSafely

Send a message via Sales Navigator API. Can reply to existing thread or start new conversation with recipients. Optionally copy to CRM. Note: POST /conversations/send auto-detects Sales Nav accounts and routes accordingly.

## Endpoint

- **Method:** `POST`
- **Path:** `/sales-nav/send`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Send Sales Navigator message](https://connectsafely.ai/docs/api/linkedin-messaging/post-sales-nav-send-sales-nav-send-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID |
| `threadId` | body | `string` | no | Existing thread ID to reply to |
| `recipients` | body | `array` | no | Profile URNs for new conversation (required if no threadId) |
| `body` | body | `string` | yes | Message text |
| `copyToCrm` | body | `boolean` | no | Copy message to CRM Default: `False`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `message` | `string` |  |
| `threadId` | `string` |  |
| `messageId` | `string` |  |
| `accountId` | `string` |  |

## Error status codes

`400`, `401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

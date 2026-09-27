# Mark all messages as read with ConnectSafely

**DEPRECATED: Will be moved to /conversations API.** --- Mark all LinkedIn messages as read for the authenticated account. Clears all unread indicators in the inbox. Useful for bulk inbox management.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging/mark-all-read`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Mark all messages as read](https://connectsafely.ai/docs/api/linkedin-messaging/post-messaging-mark-all-read-mark-all-messages-read)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `message` | `string` |  |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "message": "All messages marked as read successfully"
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

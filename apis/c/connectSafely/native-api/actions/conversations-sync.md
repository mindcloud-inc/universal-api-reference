# Trigger conversation sync with ConnectSafely

Trigger a full sync of conversations from LinkedIn API to local database.

## Endpoint

- **Method:** `POST`
- **Path:** `/conversations/sync`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Trigger conversation sync](https://connectsafely.ai/docs/api/linkedin-messaging/post-conversations-sync-conversations-sync)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID |
| `force` | body | `boolean` | no | Force sync even if recently synced Default: `False`. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` |  |
| `conversationsProcessed` | `number` |  |
| `messagesProcessed` | `number` |  |
| `durationMs` | `number` |  |
| `durationSeconds` | `string` |  |
| `error` | `string` |  |

## Error status codes

`401`, `404`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

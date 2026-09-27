# Get sync status with ConnectSafely

Get sync status for one or all LinkedIn accounts.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversations/sync/status`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get sync status](https://connectsafely.ai/docs/api/linkedin-messaging/get-conversations-sync-status-conversations-sync-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | Account ID (optional, returns all if omitted) |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accounts` | `array` |  |
| `accounts[].accountId` | `string` |  |
| `accounts[].accountName` | `string` |  |
| `accounts[].accountPicture` | `string` |  |
| `accounts[].syncState` | `object` |  |
| `accounts[].syncState.lastSyncAt` | `date` |  |
| `accounts[].syncState.syncInProgress` | `boolean` |  |
| `accounts[].syncState.totalConversations` | `number` |  |
| `accounts[].syncState.totalMessages` | `number` |  |
| `accounts[].syncState.consecutiveFailures` | `number` |  |
| `accounts[].syncState.lastError` | `string` |  |
| `accounts[].syncState.initialSyncCompleted` | `boolean` |  |

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.

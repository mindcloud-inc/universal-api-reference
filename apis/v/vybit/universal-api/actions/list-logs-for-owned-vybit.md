# Vybit: List Logs for Owned Vybit



```
GET https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-logs-for-owned-vybit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vybit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-logs-for-owned-vybit?connectionId=$CONNECTION_ID&limit=25&offset=0&vybKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "vybKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vybit/latest/actions/list-logs-for-owned-vybit?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | number | no | Maximum number of log records to return. |
| `offset` | number | no | Number of log records to skip. |
| `search` | string | no | Search logs by vybit name or diagnostic fields. |
| `vybKey` | string | yes | The unique key of the owned vybit whose logs to list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "imageUrl": "https://example.com",
      "key": "string",
      "linkUrl": "https://example.com",
      "log": "string",
      "notification": "string",
      "ownerName": "Ava Chen",
      "senderName": "Ava Chen",
      "soundKey": "string",
      "vybDescription": "string",
      "vybfollowKey": "string",
      "vybKey": "string",
      "vybName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the log entry was created. |
| `imageUrl` | string | Image URL included with the notification, when present. |
| `key` | string | Unique log entry identifier. |
| `linkUrl` | string | Link URL included with the notification, when present. |
| `log` | string | Custom log text attached to the notification. |
| `notification` | string | Notification text shown to the recipient. |
| `ownerName` | string | Name of the user who owns or received the notification. |
| `senderName` | string | Name of the user who sent the notification. |
| `soundKey` | string | Key of the sound that was played. |
| `vybDescription` | string | Description of the vybit. |
| `vybfollowKey` | string | Following key when the log was generated from a subscription. |
| `vybKey` | string | Key of the vybit that produced the log, when available. |
| `vybName` | string | Name of the vybit. |

## Native endpoint

Through the native Vybit API, this operation is `GET /logs/vybit/{{vybKey}}` (base URL `https://api.vybit.net/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-logs-for-owned-vybit.md) for the provider-specific parameters and requirements.


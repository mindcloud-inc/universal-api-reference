# WhautoChat: Get Broadcast Logs

Retrieves broadcast logs from WhautoChat.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&broadcastId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "broadcastId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-broadcast-logs?${params}`, {
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
| `broadcastId` | string | yes | Broadcast unique ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "broadcast": {
        "id": "string",
        "name": "Ava Chen"
      },
      "countryCode": "string",
      "createdAt": "string",
      "error": "string",
      "phone": "string",
      "recepientName": "Ava Chen",
      "reply": "string",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `broadcast.id` | string |  |
| `broadcast.name` | string |  |
| `countryCode` | string |  |
| `createdAt` | string |  |
| `error` | string |  |
| `phone` | string |  |
| `recepientName` | string |  |
| `reply` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/broadcasts/{broadcastId}/logs` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-broadcast-logs.md) for the provider-specific parameters and requirements.


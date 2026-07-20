# Heyy: Start Broadcast

Starts a broadcast in a Heyy channel.

```
PUT https://connect.mindcloud.co/v1/universal/heyy/latest/actions/start-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heyy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/heyy/latest/actions/start-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "broadcastId": "string",
  "channelId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/heyy/latest/actions/start-broadcast', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "broadcastId": "string",
    "channelId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `broadcastId` | string | yes | The Heyy broadcast ID. |
| `channelId` | string | yes | The Heyy channel ID. |
| `mediaId` | string | no | Optional media file ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channelId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channelId` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Heyy API, this operation is `POST /[:channelId]/broadcasts/:broadcastId/start` (base URL `https://api.heyy.io/api/v2.0/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-broadcast.md) for the provider-specific parameters and requirements.


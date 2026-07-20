# Chatforma: Create Dispatch To Segment

Creates a segment dispatch in Chatforma.

```
POST https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/create-dispatch-to-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/create-dispatch-to-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "segmentId": 1,
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/create-dispatch-to-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "segmentId": 1,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes |  |
| `segmentId` | number | yes | Use `0` to dispatch to all users for the bot. |
| `content` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "data": [
        {
          "content": "string",
          "type": "string"
        }
      ],
      "delivered": 1,
      "destination": {
        "listId": 1,
        "userId": 1
      },
      "error": "string",
      "id": 1,
      "name": "Ava Chen",
      "runAt": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "type": "string",
      "undelivered": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botId` | number |  |
| `createdAt` | date |  |
| `data[].content` | string |  |
| `data[].type` | string |  |
| `delivered` | number |  |
| `destination.listId` | number |  |
| `destination.userId` | number |  |
| `error` | string |  |
| `id` | number |  |
| `name` | string |  |
| `runAt` | date |  |
| `status` | string |  |
| `type` | string |  |
| `undelivered` | number |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Chatforma API, this operation is `POST /bots/:botId/segments/:segmentId/dispatch` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-dispatch-to-segment.md) for the provider-specific parameters and requirements.


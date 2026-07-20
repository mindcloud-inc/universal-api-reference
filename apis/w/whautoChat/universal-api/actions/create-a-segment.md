# WhautoChat: Create a Segment

Creates a new segment in WhautoChat.

```
POST https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/create-a-segment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/create-a-segment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/create-a-segment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no |  |
| `type` | string | no |  |
| `status` | string | no |  |
| `segments[]` | array<object> | no |  |
| `retargetBroadcast.id` | string | no |  |
| `retargetEngagementType` | string | no |  |
| `scheduleDateTime` | date | no |  |
| `startedAt` | string | no |  |
| `completedAt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "id": "string",
      "name": "Ava Chen",
      "retargetBroadcast": {
        "id": "string"
      },
      "retargetEngagementType": "string",
      "scheduleDateTime": "2026-05-07T12:00:00.000Z",
      "segments": [
        {}
      ],
      "startedAt": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string |  |
| `id` | string |  |
| `name` | string |  |
| `retargetBroadcast.id` | string |  |
| `retargetEngagementType` | string |  |
| `scheduleDateTime` | date |  |
| `segments` | array<object> |  |
| `startedAt` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `POST /v1/segments` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-segment.md) for the provider-specific parameters and requirements.


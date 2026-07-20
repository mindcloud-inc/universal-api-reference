# WhautoChat: Get Segment by ID

Retrieves a segment from WhautoChat by ID.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-segment-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-segment-by-id?connectionId=$CONNECTION_ID&segmentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "segmentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/get-segment-by-id?${params}`, {
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
| `segmentId` | string | yes | Segment unique ID |

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

Through the native WhautoChat API, this operation is `GET /v1/segments/{segmentId}` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-segment-by-id.md) for the provider-specific parameters and requirements.


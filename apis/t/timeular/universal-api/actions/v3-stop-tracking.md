# Timeular: V3 Stop Tracking

Creates a time entry by stopping tracking in the Timeular v3 API.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-stop-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-stop-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-stop-tracking', {
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
| `stoppedAt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTimeEntry": {
        "activityId": "string",
        "duration": {
          "startedAt": "string",
          "stoppedAt": "string"
        },
        "id": "string",
        "note": {
          "mentions": [
            [
              "string"
            ]
          ],
          "tags": [
            [
              "string"
            ]
          ],
          "text": "string"
        }
      },
      "errors": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTimeEntry.activityId` | string |  |
| `createdTimeEntry.duration.startedAt` | string |  |
| `createdTimeEntry.duration.stoppedAt` | string |  |
| `createdTimeEntry.id` | string |  |
| `createdTimeEntry.note.mentions[]` | array<string> |  |
| `createdTimeEntry.note.tags[]` | array<string> |  |
| `createdTimeEntry.note.text` | string |  |
| `errors[]` | array<string> |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v3/tracking/stop` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-stop-tracking.md) for the provider-specific parameters and requirements.


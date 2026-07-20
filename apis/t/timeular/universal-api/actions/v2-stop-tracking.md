# Timeular: V2 Stop Tracking

Creates a time entry by stopping tracking in the Timeular v2 API.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-stop-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-stop-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-stop-tracking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stoppedAt` | string | no |  |
| `trackingId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTimeEntry": {
        "activity": {
          "color": "string",
          "id": "string",
          "integration": "string",
          "name": "Ava Chen"
        },
        "duration": {
          "startedAt": "string",
          "stoppedAt": "string"
        },
        "id": "string",
        "note": {
          "mentions": [
            {
              "indices": [
                [
                  1
                ]
              ],
              "key": "string"
            }
          ],
          "tags": [
            {
              "indices": [
                [
                  1
                ]
              ],
              "key": "string"
            }
          ],
          "text": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTimeEntry.activity.color` | string |  |
| `createdTimeEntry.activity.id` | string |  |
| `createdTimeEntry.activity.integration` | string |  |
| `createdTimeEntry.activity.name` | string |  |
| `createdTimeEntry.duration.startedAt` | string |  |
| `createdTimeEntry.duration.stoppedAt` | string |  |
| `createdTimeEntry.id` | string |  |
| `createdTimeEntry.note.mentions[].indices[]` | array<number> |  |
| `createdTimeEntry.note.mentions[].key` | string |  |
| `createdTimeEntry.note.tags[].indices[]` | array<number> |  |
| `createdTimeEntry.note.tags[].key` | string |  |
| `createdTimeEntry.note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v2/tracking/:trackingId/stop` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-stop-tracking.md) for the provider-specific parameters and requirements.


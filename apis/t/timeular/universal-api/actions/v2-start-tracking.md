# Timeular: V2 Start Tracking

Creates a tracking session in the Timeular v2 API.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-start-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-start-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-start-tracking', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes |  |
| `startedAt` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentTracking": {
        "activity": {
          "color": "string",
          "id": "string",
          "integration": "string",
          "name": "Ava Chen"
        },
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
        },
        "startedAt": "string"
      },
      "errors": {
        "errors": [
          [
            "string"
          ]
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentTracking.activity.color` | string |  |
| `currentTracking.activity.id` | string |  |
| `currentTracking.activity.integration` | string |  |
| `currentTracking.activity.name` | string |  |
| `currentTracking.note.mentions[].indices[]` | array<number> |  |
| `currentTracking.note.mentions[].key` | string |  |
| `currentTracking.note.tags[].indices[]` | array<number> |  |
| `currentTracking.note.tags[].key` | string |  |
| `currentTracking.note.text` | string |  |
| `currentTracking.startedAt` | string |  |
| `errors.errors[]` | array<string> |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v2/tracking/:activityId/start` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-start-tracking.md) for the provider-specific parameters and requirements.


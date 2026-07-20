# Timeular: V2 Edit Tracking

Updates the current tracking session in the Timeular v2 API.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-edit-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-edit-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-edit-tracking', {
  method: 'PUT',
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
| `note` | string | no |  |
| `trackingId` | string | yes |  |

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

## Native endpoint

Through the native Timeular API, this operation is `PATCH /api/v2/tracking/:trackingId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-edit-tracking.md) for the provider-specific parameters and requirements.


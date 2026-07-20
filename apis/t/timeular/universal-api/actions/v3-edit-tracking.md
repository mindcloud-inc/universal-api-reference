# Timeular: V3 Edit Tracking

Updates the current tracking session in the Timeular v3 API.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-tracking', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "currentTracking": {
        "activityId": "string",
        "id": 1,
        "note": {
          "mentions": [
            {
              "id": 1,
              "key": "string",
              "label": "string",
              "scope": "string",
              "spaceId": "string"
            }
          ],
          "tags": [
            {
              "id": 1,
              "key": "string",
              "label": "string",
              "scope": "string",
              "spaceId": "string"
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
| `currentTracking.activityId` | string |  |
| `currentTracking.id` | number |  |
| `currentTracking.note.mentions[].id` | number |  |
| `currentTracking.note.mentions[].key` | string |  |
| `currentTracking.note.mentions[].label` | string |  |
| `currentTracking.note.mentions[].scope` | string |  |
| `currentTracking.note.mentions[].spaceId` | string |  |
| `currentTracking.note.tags[].id` | number |  |
| `currentTracking.note.tags[].key` | string |  |
| `currentTracking.note.tags[].label` | string |  |
| `currentTracking.note.tags[].scope` | string |  |
| `currentTracking.note.tags[].spaceId` | string |  |
| `currentTracking.note.text` | string |  |
| `currentTracking.startedAt` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `PATCH /api/v3/tracking` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-edit-tracking.md) for the provider-specific parameters and requirements.


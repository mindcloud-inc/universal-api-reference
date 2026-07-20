# Timeular: V2 Show current Tracking

Retrieves the current tracking session from the Timeular v2 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-show-current-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-show-current-tracking?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-show-current-tracking?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Timeular API, this operation is `GET /api/v2/tracking` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-show-current-tracking.md) for the provider-specific parameters and requirements.


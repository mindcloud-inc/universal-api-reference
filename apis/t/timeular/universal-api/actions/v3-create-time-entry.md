# Timeular: V3 Create Time Entry

Creates a new time entry in the Timeular v3 API.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-create-time-entry', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "activityId": "string",
      "duration": {
        "startedAt": "string",
        "stoppedAt": "string"
      },
      "errors": [
        [
          "string"
        ]
      ],
      "id": "string",
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
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityId` | string |  |
| `duration.startedAt` | string |  |
| `duration.stoppedAt` | string |  |
| `errors[]` | array<string> |  |
| `id` | string |  |
| `note.mentions[].id` | number |  |
| `note.mentions[].key` | string |  |
| `note.mentions[].label` | string |  |
| `note.mentions[].scope` | string |  |
| `note.mentions[].spaceId` | string |  |
| `note.tags[].id` | number |  |
| `note.tags[].key` | string |  |
| `note.tags[].label` | string |  |
| `note.tags[].scope` | string |  |
| `note.tags[].spaceId` | string |  |
| `note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v3/time-entries` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-create-time-entry.md) for the provider-specific parameters and requirements.


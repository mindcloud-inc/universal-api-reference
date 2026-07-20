# Timeular: Stop Tracking

Creates a time entry by stopping tracking in your Timeular workspace.

```
POST https://connect.mindcloud.co/v1/universal/timeular/latest/actions/stop-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/stop-tracking" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/stop-tracking', {
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
      "activity": {
        "color": "string",
        "folderId": "string",
        "id": "string",
        "name": "Ava Chen"
      },
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity.color` | string |  |
| `activity.folderId` | string |  |
| `activity.id` | string |  |
| `activity.name` | string |  |
| `duration.startedAt` | string |  |
| `duration.stoppedAt` | string |  |
| `errors[]` | array<string> |  |
| `id` | string |  |
| `note.mentions[]` | array<string> |  |
| `note.tags[]` | array<string> |  |
| `note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `POST /api/v4/tracking/stop` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-tracking.md) for the provider-specific parameters and requirements.


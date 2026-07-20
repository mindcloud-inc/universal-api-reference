# Timeular: V2 Edit Time Entry

Updates an existing time entry in the Timeular v2 API.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-edit-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-edit-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeEntryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-edit-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeEntryId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | no |  |
| `note` | string | no |  |
| `startedAt` | string | no |  |
| `stoppedAt` | string | no |  |
| `timeEntryId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity.color` | string |  |
| `activity.id` | string |  |
| `activity.integration` | string |  |
| `activity.name` | string |  |
| `duration.startedAt` | string |  |
| `duration.stoppedAt` | string |  |
| `id` | string |  |
| `note.mentions[].indices[]` | array<number> |  |
| `note.mentions[].key` | string |  |
| `note.tags[].indices[]` | array<number> |  |
| `note.tags[].key` | string |  |
| `note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `PATCH /api/v2/time-entries/:timeEntryId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-edit-time-entry.md) for the provider-specific parameters and requirements.


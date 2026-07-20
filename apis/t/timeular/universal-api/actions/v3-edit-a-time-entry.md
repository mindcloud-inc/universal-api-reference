# Timeular: V3 Edit a Time Entry

Updates an existing time entry in the Timeular v3 API.

```
PUT https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-a-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-a-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeEntryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-edit-a-time-entry', {
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
| `timeEntryId` | string | yes |  |

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

Through the native Timeular API, this operation is `PATCH /api/v3/time-entries/:timeEntryId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-edit-a-time-entry.md) for the provider-specific parameters and requirements.


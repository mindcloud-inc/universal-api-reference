# Timeular: V2 Find Time Entry

Retrieves a time entry from the Timeular v2 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-find-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-find-time-entry?connectionId=$CONNECTION_ID&timeEntryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "timeEntryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-find-time-entry?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
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

Through the native Timeular API, this operation is `GET /api/v2/time-entries/:timeEntryId` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-find-time-entry.md) for the provider-specific parameters and requirements.


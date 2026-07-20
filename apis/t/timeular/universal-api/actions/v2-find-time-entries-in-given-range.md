# Timeular: V2 Find Time Entries in given range

Retrieves time entries in a date range from the Timeular v2 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-find-time-entries-in-given-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-find-time-entries-in-given-range?connectionId=$CONNECTION_ID&end=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-find-time-entries-in-given-range?${params}`, {
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
| `end` | string | yes |  |
| `start` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timeEntries": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timeEntries[].activity.color` | string |  |
| `timeEntries[].activity.id` | string |  |
| `timeEntries[].activity.integration` | string |  |
| `timeEntries[].activity.name` | string |  |
| `timeEntries[].duration.startedAt` | string |  |
| `timeEntries[].duration.stoppedAt` | string |  |
| `timeEntries[].id` | string |  |
| `timeEntries[].note.mentions[].indices[]` | array<number> |  |
| `timeEntries[].note.mentions[].key` | string |  |
| `timeEntries[].note.tags[].indices[]` | array<number> |  |
| `timeEntries[].note.tags[].key` | string |  |
| `timeEntries[].note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v2/time-entries/:start/:end` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-find-time-entries-in-given-range.md) for the provider-specific parameters and requirements.


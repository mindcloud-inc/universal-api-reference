# Timeular: List Time Entries in Range

Retrieves time entries in a date range from your Timeular workspace.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-time-entries-in-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-time-entries-in-range?connectionId=$CONNECTION_ID&end=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/list-time-entries-in-range?${params}`, {
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
            "folderId": "string",
            "id": "string",
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
                "folderId": "string",
                "id": 1,
                "key": "string",
                "label": "string",
                "scope": "string"
              }
            ],
            "tags": [
              {
                "folderId": "string",
                "id": 1,
                "key": "string",
                "label": "string",
                "scope": "string"
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
| `timeEntries[].activity.folderId` | string |  |
| `timeEntries[].activity.id` | string |  |
| `timeEntries[].activity.name` | string |  |
| `timeEntries[].duration.startedAt` | string |  |
| `timeEntries[].duration.stoppedAt` | string |  |
| `timeEntries[].id` | string |  |
| `timeEntries[].note.mentions[].folderId` | string |  |
| `timeEntries[].note.mentions[].id` | number |  |
| `timeEntries[].note.mentions[].key` | string |  |
| `timeEntries[].note.mentions[].label` | string |  |
| `timeEntries[].note.mentions[].scope` | string |  |
| `timeEntries[].note.tags[].folderId` | string |  |
| `timeEntries[].note.tags[].id` | number |  |
| `timeEntries[].note.tags[].key` | string |  |
| `timeEntries[].note.tags[].label` | string |  |
| `timeEntries[].note.tags[].scope` | string |  |
| `timeEntries[].note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v4/time-entries/:start/:end` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries-in-range.md) for the provider-specific parameters and requirements.


# Timeular: V3 All Data as JSON

Retrieves report data as JSON from the Timeular v3 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-all-data-as-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-all-data-as-json?connectionId=$CONNECTION_ID&end=string&start=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "end": "string",
  "start": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v3-all-data-as-json?${params}`, {
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
            "name": "Ava Chen",
            "spaceId": "string"
          },
          "creator": "string",
          "duration": {
            "startedAt": "string",
            "stoppedAt": "string"
          },
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
              [
                "string"
              ]
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
| `timeEntries[].activity.spaceId` | string |  |
| `timeEntries[].creator` | string |  |
| `timeEntries[].duration.startedAt` | string |  |
| `timeEntries[].duration.stoppedAt` | string |  |
| `timeEntries[].id` | string |  |
| `timeEntries[].note.mentions[].id` | number |  |
| `timeEntries[].note.mentions[].key` | string |  |
| `timeEntries[].note.mentions[].label` | string |  |
| `timeEntries[].note.mentions[].scope` | string |  |
| `timeEntries[].note.mentions[].spaceId` | string |  |
| `timeEntries[].note.tags[]` | array<string> |  |
| `timeEntries[].note.text` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v3/report/data/:start/:end` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v3-all-data-as-json.md) for the provider-specific parameters and requirements.


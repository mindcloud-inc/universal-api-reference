# Timing: Batch Update Time Entries

Updates multiple time entries at once in Timing.

```
PUT https://connect.mindcloud.co/v1/universal/timing/latest/actions/batch-update-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timing/latest/actions/batch-update-time-entries" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeEntries[]": [
    "string"
  ],
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timing/latest/actions/batch-update-time-entries', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "timeEntries[]": ["string"],
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `timeEntries[]` | array<string> | yes |  |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billingStatus": "string",
      "creatorId": "string",
      "creatorName": "Ava Chen",
      "customFields": {},
      "duration": 1,
      "endDate": "2026-05-07T12:00:00.000Z",
      "isRunning": true,
      "notes": "string",
      "project": {
        "self": "string"
      },
      "self": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billingStatus` | string |  |
| `creatorId` | string |  |
| `creatorName` | string |  |
| `customFields` | object |  |
| `duration` | number |  |
| `endDate` | date |  |
| `isRunning` | boolean |  |
| `notes` | string |  |
| `project` | object |  |
| `project.self` | string |  |
| `self` | string |  |
| `startDate` | date |  |
| `title` | string |  |

## Native endpoint

Through the native Timing API, this operation is `PATCH /time-entries/batch-update` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-update-time-entries.md) for the provider-specific parameters and requirements.


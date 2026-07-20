# Timing: Update Time Entry

Updates an existing time entry in Timing.

```
PUT https://connect.mindcloud.co/v1/universal/timing/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/timing/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "timeEntryId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/timing/latest/actions/update-time-entry', {
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
| `timeEntryId` | string | yes | The Timing time entry ID to update. |
| `title` | string | no |  |

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

Through the native Timing API, this operation is `PUT /time-entries/:time_entry_id` (base URL `https://web.timingapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.


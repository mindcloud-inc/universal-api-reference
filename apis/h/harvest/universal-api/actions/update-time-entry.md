# Harvest: Update Time Entry

Updates an existing time entry in Harvest.

```
PUT https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/update-time-entry', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `projectId` | number | no |  |
| `taskId` | number | no |  |
| `spentDate` | string | no |  |
| `startedTime` | string | no |  |
| `endedTime` | string | no |  |
| `hours` | number | no |  |
| `notes` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalReference` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approvalStatus": "string",
      "billable": true,
      "billableRate": 1,
      "budgeted": true,
      "client": {},
      "costRate": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "endedTime": "string",
      "externalReference": {},
      "hours": 1,
      "hoursWithoutTimer": 1,
      "id": 1,
      "invoice": {},
      "isBilled": true,
      "isClosed": true,
      "isLocked": true,
      "isRunning": true,
      "lockedReason": "string",
      "notes": "string",
      "project": {},
      "roundedHours": 1,
      "spentDate": "2026-05-07T12:00:00.000Z",
      "startedTime": "string",
      "task": {},
      "taskAssignment": {},
      "timerStartedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": {},
      "userAssignment": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approvalStatus` | string |  |
| `billable` | boolean |  |
| `billableRate` | number |  |
| `budgeted` | boolean |  |
| `client` | object |  |
| `costRate` | number |  |
| `createdAt` | date |  |
| `endedTime` | string |  |
| `externalReference` | object |  |
| `hours` | number |  |
| `hoursWithoutTimer` | number |  |
| `id` | number |  |
| `invoice` | object |  |
| `isBilled` | boolean |  |
| `isClosed` | boolean |  |
| `isLocked` | boolean |  |
| `isRunning` | boolean |  |
| `lockedReason` | string |  |
| `notes` | string |  |
| `project` | object |  |
| `roundedHours` | number |  |
| `spentDate` | date |  |
| `startedTime` | string |  |
| `task` | object |  |
| `taskAssignment` | object |  |
| `timerStartedAt` | date |  |
| `updatedAt` | date |  |
| `user` | object |  |
| `userAssignment` | object |  |

## Native endpoint

Through the native Harvest API, this operation is `PATCH /v2/time_entries/:id` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-time-entry.md) for the provider-specific parameters and requirements.


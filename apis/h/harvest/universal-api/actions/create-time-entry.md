# Harvest: Create Time Entry

Creates a new time entry in Harvest.

```
POST https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-time-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "taskId": 1,
  "spentDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harvest/latest/actions/create-time-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "taskId": 1,
    "spentDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | number | yes |  |
| `taskId` | number | yes |  |
| `spentDate` | string | yes |  |
| `hours` | number | no |  |
| `startedTime` | string | no |  |
| `endedTime` | string | no |  |
| `notes` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | no |  |
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

Through the native Harvest API, this operation is `POST /v2/time_entries` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-time-entry.md) for the provider-specific parameters and requirements.


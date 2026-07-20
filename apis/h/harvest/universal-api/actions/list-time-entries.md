# Harvest: List Time Entries

Retrieves time entries from Harvest.

```
GET https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harvest `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harvest/latest/actions/list-time-entries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Harvest API, this operation is `GET /v2/time_entries` (base URL `https://api.harvestapp.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.


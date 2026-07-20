# CentralStationCRM: Create Task

Creates a new task in CentralStationCRM.

```
POST https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CentralStationCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/centralStationCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "attachableId": 1,
      "attachableType": "string",
      "badge": "string",
      "commentsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByUserId": 1,
      "endTime": "2026-05-07T12:00:00.000Z",
      "finished": true,
      "fuzzy": true,
      "id": 1,
      "name": "Ava Chen",
      "preciseTime": "2026-05-07T12:00:00.000Z",
      "taskListId": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedByUserId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `attachableId` | number |  |
| `attachableType` | string |  |
| `badge` | string |  |
| `commentsCount` | number |  |
| `createdAt` | date |  |
| `createdByUserId` | number |  |
| `endTime` | date |  |
| `finished` | boolean |  |
| `fuzzy` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `preciseTime` | date |  |
| `taskListId` | number |  |
| `updatedAt` | date |  |
| `updatedByUserId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native CentralStationCRM API, this operation is `POST /api/tasks` (base URL `https://api.centralstationcrm.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.


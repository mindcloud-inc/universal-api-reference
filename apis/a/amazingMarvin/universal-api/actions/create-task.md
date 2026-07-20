# Amazing Marvin: Create Task

Creates a task in Amazing Marvin.

```
POST https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Task title. |
| `day` | string | no | Schedule date in YYYY-MM-DD format. |
| `dueDate` | string | no | Due date in YYYY-MM-DD format. |
| `parentId` | string | no | Optional parent category or project ID. |
| `timeZoneOffset` | number | no | Timezone offset in minutes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "backburner": true,
      "bonusSection": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customSection": "string",
      "dailySection": "string",
      "day": "2026-05-07T12:00:00.000Z",
      "db": "string",
      "done": true,
      "doneAt": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "echo": true,
      "echoId": "string",
      "email": "ava@example.com",
      "firstScheduled": "2026-05-07T12:00:00.000Z",
      "isFrogged": 1,
      "isPinned": true,
      "isReward": true,
      "isStarred": 1,
      "masterRank": 1,
      "note": "string",
      "parentId": "string",
      "pinId": "string",
      "plannedMonth": "string",
      "plannedWeek": "string",
      "rank": 1,
      "recurringTaskId": "string",
      "reviewDate": "string",
      "rewardPoints": 1,
      "taskTime": "string",
      "timeBlockSection": "string",
      "timeEstimate": 1,
      "times": {},
      "timeZoneOffset": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `backburner` | boolean |  |
| `bonusSection` | string |  |
| `createdAt` | date |  |
| `customSection` | string |  |
| `dailySection` | string |  |
| `day` | date |  |
| `db` | string |  |
| `done` | boolean |  |
| `doneAt` | date |  |
| `dueDate` | date |  |
| `duration` | number |  |
| `echo` | boolean |  |
| `echoId` | string |  |
| `email` | string |  |
| `firstScheduled` | date |  |
| `isFrogged` | number |  |
| `isPinned` | boolean |  |
| `isReward` | boolean |  |
| `isStarred` | number |  |
| `masterRank` | number |  |
| `note` | string |  |
| `parentId` | string |  |
| `pinId` | string |  |
| `plannedMonth` | string |  |
| `plannedWeek` | string |  |
| `rank` | number |  |
| `recurringTaskId` | string |  |
| `reviewDate` | string |  |
| `rewardPoints` | number |  |
| `taskTime` | string |  |
| `timeBlockSection` | string |  |
| `timeEstimate` | number |  |
| `times` | object |  |
| `timeZoneOffset` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /addTask` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.


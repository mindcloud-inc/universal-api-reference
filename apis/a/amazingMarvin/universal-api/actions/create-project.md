# Amazing Marvin: Create Project

Creates a project in Amazing Marvin.

```
POST https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazing Marvin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/amazingMarvin/latest/actions/create-project', {
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
| `title` | string | yes | Project title. |
| `day` | string | no | Schedule date in YYYY-MM-DD format or null. |
| `priority` | string | no | low, mid, or high. |
| `parentId` | string | no | Optional parent category or project ID. |
| `dueDate` | string | no | Due date in YYYY-MM-DD format. |
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
      "dailySection": 1,
      "day": "string",
      "db": "string",
      "done": true,
      "dueDate": "string",
      "email": "ava@example.com",
      "firstScheduled": "string",
      "isFrogged": 1,
      "itemSnoozeTime": "string",
      "note": "string",
      "parentId": "string",
      "permaSnoozeTime": "string",
      "plannedMonth": "string",
      "plannedWeek": "string",
      "priority": "string",
      "rank": 1,
      "reviewDate": "string",
      "rewardId": "string",
      "rewardPoints": 1,
      "timeBlockSection": "string",
      "timeEstimate": 1,
      "timeZoneOffset": 1,
      "title": "string",
      "type": "string"
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
| `dailySection` | number |  |
| `day` | string |  |
| `db` | string |  |
| `done` | boolean |  |
| `dueDate` | string |  |
| `email` | string |  |
| `firstScheduled` | string |  |
| `isFrogged` | number |  |
| `itemSnoozeTime` | string |  |
| `note` | string |  |
| `parentId` | string |  |
| `permaSnoozeTime` | string |  |
| `plannedMonth` | string |  |
| `plannedWeek` | string |  |
| `priority` | string |  |
| `rank` | number |  |
| `reviewDate` | string |  |
| `rewardId` | string |  |
| `rewardPoints` | number |  |
| `timeBlockSection` | string |  |
| `timeEstimate` | number |  |
| `timeZoneOffset` | number |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Amazing Marvin API, this operation is `POST /addProject` (base URL `https://serv.amazingmarvin.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.


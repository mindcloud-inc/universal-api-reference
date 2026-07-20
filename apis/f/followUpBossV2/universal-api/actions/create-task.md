# Follow Up Boss: Create Task

Creates a new task in Follow Up Boss.

```
POST https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/create-task', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `personId` | number | no |  |
| `name` | string | no |  |
| `type` | string | no |  |
| `dueDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": "string",
      "assignedUserId": 1,
      "completed": {},
      "created": "string",
      "createdBy": "string",
      "createdById": 1,
      "dueDate": "string",
      "dueDateTime": {},
      "externalCalendarId": {},
      "externalTaskLink": {},
      "id": 1,
      "isCompleted": 1,
      "name": "Ava Chen",
      "personId": 1,
      "remindSecondsBefore": {},
      "type": "string",
      "updated": "string",
      "updatedBy": "string",
      "updatedById": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | string |  |
| `assignedUserId` | number |  |
| `completed` | object |  |
| `created` | string |  |
| `createdBy` | string |  |
| `createdById` | number |  |
| `dueDate` | string |  |
| `dueDateTime` | object |  |
| `externalCalendarId` | object |  |
| `externalTaskLink` | object |  |
| `id` | number |  |
| `isCompleted` | number |  |
| `name` | string |  |
| `personId` | number |  |
| `remindSecondsBefore` | object |  |
| `type` | string |  |
| `updated` | string |  |
| `updatedBy` | string |  |
| `updatedById` | number |  |

## Native endpoint

Through the native Follow Up Boss API, this operation is `POST tasks` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.


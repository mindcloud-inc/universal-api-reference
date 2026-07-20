# Follow Up Boss: Get Task

Retrieves a task from Follow Up Boss.

```
GET https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Follow Up Boss `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-task?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/followUpBossV2/latest/actions/get-task?${params}`, {
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
| `id` | string | yes | The task ID. |

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

Through the native Follow Up Boss API, this operation is `GET tasks/:id` (base URL `https://api.followupboss.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.


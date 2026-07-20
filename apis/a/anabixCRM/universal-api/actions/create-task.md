# Anabix CRM: Create Task

Creates a new task in Anabix CRM.

```
POST https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.body` | string | yes | Task body. Anabix requires body when creating a task. |
| `data.idContact` | number | no | Optional related contact ID for the task. |
| `data.title` | string | no | Optional task title. If omitted, Anabix creates a title from the task body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedUserId": 1,
      "assignedUsername": "Ava Chen",
      "body": "string",
      "category": "string",
      "completedDate": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "deadline": "2026-05-07T12:00:00.000Z",
      "deadlineTime": "string",
      "duration": "string",
      "idContact": 1,
      "idDeal": 1,
      "idTask": 1,
      "priority": "string",
      "revisionInfo": {},
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedUserId` | number |  |
| `assignedUsername` | string |  |
| `body` | string |  |
| `category` | string |  |
| `completedDate` | date |  |
| `customFields` | array<object> |  |
| `deadline` | date |  |
| `deadlineTime` | string |  |
| `duration` | string |  |
| `idContact` | number |  |
| `idDeal` | number |  |
| `idTask` | number | Anabix task ID. |
| `priority` | string |  |
| `revisionInfo` | object |  |
| `status` | string |  |
| `title` | string | Task title. |

## Native endpoint

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.


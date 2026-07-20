# Anabix CRM: Update Task

Updates an existing task in Anabix CRM.

```
PUT https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.idTask": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.idTask": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.idTask` | number | yes |  |
| `data.body` | string | no | Updated task body from Anabix task data. |

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

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.


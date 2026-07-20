# Anabix CRM: Get Task

Retrieves a task from Anabix CRM.

```
GET https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anabix CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-task?connectionId=$CONNECTION_ID&data.idTask=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data.idTask": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anabixCRM/latest/actions/get-task?${params}`, {
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
| `data.idTask` | number | yes |  |

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

Through the native Anabix CRM API, this operation is `POST /api` (base URL `https://app.anabix.cz`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task.md) for the provider-specific parameters and requirements.


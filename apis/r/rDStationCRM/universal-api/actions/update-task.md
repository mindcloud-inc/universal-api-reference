# RD Station CRM: Update Task

Updates an existing task in RD Station CRM.

```
PUT https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RD Station CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {},
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rDStationCRM/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {},
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Task payload documented in endpoint reference. |
| `data.completed_by_id` | string | no | ID do usuário que concluiu a tarefa. |
| `data.created_by_id` | string | no | ID do usuário que criou a tarefa. |
| `data.deal_id` | string | no | ID da negociação associada. |
| `data.description` | string | no | Notas ou descrição adicional da tarefa. |
| `data.due_date` | date | no | Data limite para conclusão da tarefa. |
| `data.name` | string | no | Assunto da tarefa. |
| `data.owner_ids[]` | array<string> | no | IDs dos usuários responsáveis pela tarefa. |
| `data.status` | string | no | Status da tarefa. |
| `data.type` | string | no | Tipo da tarefa. |
| `id` | string | yes | Task identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createdAt": "string",
        "createdById": "string",
        "dealId": "string",
        "dueDate": "string",
        "id": "string",
        "name": "Ava Chen",
        "ownerIds": [
          [
            "string"
          ]
        ],
        "status": "string",
        "type": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.createdAt` | string |  |
| `data.createdById` | string |  |
| `data.dealId` | string |  |
| `data.dueDate` | string |  |
| `data.id` | string |  |
| `data.name` | string |  |
| `data.ownerIds[]` | array<string> |  |
| `data.status` | string |  |
| `data.type` | string |  |
| `data.updatedAt` | string |  |

## Native endpoint

Through the native RD Station CRM API, this operation is `PUT /tasks/:id` (base URL `https://api.rd.services/crm/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.


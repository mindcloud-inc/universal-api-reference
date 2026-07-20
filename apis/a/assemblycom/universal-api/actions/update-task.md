# Assembly.com: Update Task

Updates an existing task in Assembly.com.

```
PUT https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the task to update. |
| `name` | string | no | The name of the task. |
| `description` | string | no | The description of the task. |
| `status` | string | no | The status of the task. One of: `0`, `1`, `2`. |
| `internalUserId` | string | no | The UUID of the internal user assigned to this task. |
| `clientId` | string | no | The UUID of the client user assigned to this task. |
| `companyId` | string | no | The UUID of the company assigned to this task. If assigning to a client user, this field should also be set. |
| `dueDate` | date | no | The date the task is due, in RFC3339 format. |
| `isArchived` | boolean | no | Whether to archive the task or not. |
| `viewers` | object | no | The company or client to grant viewing access to the task. |
| `viewers.clientId` | string | no | If the task viewer is a client, add both the clientId and their companyId. |
| `viewers.companyId` | string | no | If the task viewer is a company, only add the companyId and leave clientId empty. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `PATCH /tasks/:id` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.


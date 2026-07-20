# Assembly.com: Create Task

Creates a task in Assembly.com.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-task', {
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
| `name` | string | no | The name of the task. |
| `description` | string | no | The description of the task. |
| `parentTaskId` | string | no | The parent task of the task, if the task should be a subtask. |
| `status` | string | no | The status of the task, one of todo, inProgress, completed. One of: `0`, `1`, `2`. |
| `internalUserId` | string | no | The UUID of the internal user assigned to this task. |
| `clientId` | string | no | The UUID of the client user assigned to this task. Company ID is required if this field is used. |
| `companyId` | string | no | The UUID of the company assigned to this task. If assigning to a client user, this field is required. |
| `dueDate` | date | no | The date the task is due, in RFC3339 format. |
| `templateId` | string | no | ID of the template to use when creating this task. |
| `viewers[]` | array<object> | no | The company or client to grant viewing access to the task. |
| `viewers[].clientId` | string | no | If the task viewer is a client, add both the clientId and their companyId. |
| `viewers[].companyId` | string | no | If the task viewer is a company, only add the companyId and leave clientId empty. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Assembly.com API returns.

## Native endpoint

Through the native Assembly.com API, this operation is `POST /tasks` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.


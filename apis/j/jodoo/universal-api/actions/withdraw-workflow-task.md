# Jodoo: Withdraw Workflow Task



```
PUT https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/withdraw-workflow-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jodoo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/withdraw-workflow-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "username": "jdy-57q312f65pz7",
  "instanceId": "64c72910561073000755af52",
  "taskId": "64c72910561073000755af7c"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jodoo/latest/actions/withdraw-workflow-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "username": "jdy-57q312f65pz7",
    "instanceId": "64c72910561073000755af52",
    "taskId": "64c72910561073000755af7c"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `username` | string | yes | Username assigned to the workflow task. Example: `jdy-57q312f65pz7`. |
| `instanceId` | string | yes | Workflow instance ID, which is the same as the record data ID. Example: `64c72910561073000755af52`. |
| `taskId` | string | yes | Workflow task ID assigned to the username. Example: `64c72910561073000755af7c`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Jodoo API, this operation is `POST https://api.jodoo.com/api/v1/workflow/task/revoke` (base URL `https://api.jodoo.com/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/withdraw-workflow-task.md) for the provider-specific parameters and requirements.


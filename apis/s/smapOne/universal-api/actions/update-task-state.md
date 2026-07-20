# smapOne: Update task state

Updates an existing task state in smapOne.

```
PUT https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/update-task-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smapOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/update-task-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "0",
  "smap_id": "string",
  "task_id": "string",
  "version": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smapOne/latest/actions/update-task-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "0",
    "smap_id": "string",
    "task_id": "string",
    "version": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | list | yes | Task state operation. Allowed values are Assign or Remove. One of: `0`, `1`. |
| `smap_id` | string | yes | The smap id. |
| `task_id` | string | yes | The task record id. |
| `user_email` | string | no | User email for task assignment. |
| `version` | string | yes | The smap version in major.minor format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "recordType": "string",
      "userEmail": "ava@example.com",
      "userName": "Ava Chen",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `id` | string |  |
| `recordType` | string |  |
| `userEmail` | string |  |
| `userName` | string |  |
| `version` | string |  |

## Native endpoint

Through the native smapOne API, this operation is `PUT /preview/Smaps/{smapId}/Versions/{version}/Tasks/{taskId}/State` (base URL `https://platform.smapone.com/Backend`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-state.md) for the provider-specific parameters and requirements.


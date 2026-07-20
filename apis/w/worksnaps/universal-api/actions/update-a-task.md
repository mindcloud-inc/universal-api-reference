# Worksnaps: Update a Task

Updates an existing task in a Worksnaps project.

```
PUT https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worksnaps `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-a-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksnaps/latest/actions/update-a-task', {
  method: 'PUT',
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
| `body` | string | no | Raw XML request body for this Worksnaps endpoint. |
| `project_id` | string | no | ID of the project that the task to be updated is in |
| `task_id` | string | no | ID of the target task that needs to be updated. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | the description of the task |
| `id` | number | the ID of the task |
| `name` | string | the name of the task |

## Native endpoint

Through the native Worksnaps API, this operation is `PUT /projects/{project_id}/tasks/{task_id}.xml` (base URL `https://api.worksnaps.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-task.md) for the provider-specific parameters and requirements.


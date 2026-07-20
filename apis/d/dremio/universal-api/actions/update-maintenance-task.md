# Dremio: Update Maintenance Task

Updates an existing maintenance task in a Dremio project.

```
PUT https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-maintenance-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dremio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-maintenance-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "task": {},
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dremio/latest/actions/update-maintenance-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "task": {},
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes |  |
| `task` | object | yes |  |
| `taskId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "config": {},
      "id": "string",
      "isEnabled": true,
      "level": "string",
      "sourceName": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `config` | object |  |
| `id` | string |  |
| `isEnabled` | boolean |  |
| `level` | string |  |
| `sourceName` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Dremio API, this operation is `PUT /projects/:project_id/maintenance/tasks/:taskId` (base URL `https://api.dremio.cloud/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-maintenance-task.md) for the provider-specific parameters and requirements.


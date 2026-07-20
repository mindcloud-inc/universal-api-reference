# Asana: Duplicate a task

Duplicates a task in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/duplicate-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/duplicate-a-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataInclude": "string",
  "dataName": "Ava Chen",
  "taskGid": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/duplicate-a-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataInclude": "string",
    "dataName": "Ava Chen",
    "taskGid": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataInclude` | string | yes |  |
| `dataName` | string | yes |  |
| `optFields[]` | array<string> | no |  |
| `taskGid` | string | yes | Path parameter: task_gid |
| `data` | object | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "gid": "string",
      "newTask": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceSubtype": "string",
        "resourceType": "string"
      },
      "resourceSubtype": "string",
      "resourceType": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `gid` | string |  |
| `newTask.gid` | string |  |
| `newTask.name` | string |  |
| `newTask.resourceSubtype` | string |  |
| `newTask.resourceType` | string |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST tasks/:task_gid/duplicate` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-a-task.md) for the provider-specific parameters and requirements.


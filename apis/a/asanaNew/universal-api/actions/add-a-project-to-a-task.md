# Asana: Add a project to a task

Adds a project to a task in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-project-to-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-project-to-a-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataInsertAfter": "string",
  "dataInsertBefore": "string",
  "dataProject": "string",
  "dataSection": "string",
  "taskGid": "string",
  "data.project": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/add-a-project-to-a-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataInsertAfter": "string",
    "dataInsertBefore": "string",
    "dataProject": "string",
    "dataSection": "string",
    "taskGid": "string",
    "data.project": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataInsertAfter` | string | yes |  |
| `dataInsertBefore` | string | yes |  |
| `dataProject` | string | yes |  |
| `dataSection` | string | yes |  |
| `taskGid` | string | yes | Asana task gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `data.project` | string | yes | Asana project parameter. |
| `data.insert_after` | string | no | Asana insert after parameter. |
| `data.insert_before` | string | no | Asana insert before parameter. |
| `data.section` | string | no | Asana section parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST tasks/:task_gid/addProject` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-project-to-a-task.md) for the provider-specific parameters and requirements.


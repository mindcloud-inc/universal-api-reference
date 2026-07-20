# Asana: Unlink dependents from a task

Removes dependents from a task in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/unlink-dependents-from-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/unlink-dependents-from-a-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataDependents[]": [
    "string"
  ],
  "taskGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/unlink-dependents-from-a-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataDependents[]": ["string"],
    "taskGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataDependents[]` | array<string> | yes |  |
| `taskGid` | string | yes | Asana task gid parameter. |
| `opt_pretty` | boolean | no | Asana opt pretty parameter. |
| `data.dependents` | list<string> | no | Asana dependents parameter. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Asana API returns.

## Native endpoint

Through the native Asana API, this operation is `POST tasks/:task_gid/removeDependents` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unlink-dependents-from-a-task.md) for the provider-specific parameters and requirements.


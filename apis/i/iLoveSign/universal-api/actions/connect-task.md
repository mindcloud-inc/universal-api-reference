# iLoveSign: Connect Task



```
POST https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/connect-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/connect-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "server": "api11.ilovepdf.com",
  "task": "string",
  "tool": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/connect-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "server": "api11.ilovepdf.com",
    "task": "string",
    "tool": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `server` | string | yes | Task-assigned host returned by the start call. Example: `api11.ilovepdf.com`. |
| `task` | string | yes | Parent task identifier to connect from. |
| `tool` | string | yes | Tool to use for the next connected task. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `POST https://:server/v1/task/next` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-task.md) for the provider-specific parameters and requirements.


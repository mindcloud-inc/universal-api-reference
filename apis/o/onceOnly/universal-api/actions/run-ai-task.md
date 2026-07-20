# OnceOnly: Run AI Task

Runs an AI task in OnceOnly.

```
POST https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/run-ai-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceOnly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/run-ai-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/run-ai-task', {
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
| `key` | string | no | Mode A background-run key. |
| `ttl` | number | no | Mode A lease duration in seconds. |
| `metadata` | object | no | Mode A metadata object. Can include run_id, agent_id, actions, and dry_run. |
| `agentId` | string | no | Mode B agent id. |
| `tool` | string | no | Mode B governed tool name. |
| `args` | object | no | Mode B tool arguments object. |
| `spendUsd` | number | no | Optional spend estimate in USD. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceOnly API returns.

## Native endpoint

Through the native OnceOnly API, this operation is `POST /v1/ai/run` (base URL `https://api.onceonly.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-ai-task.md) for the provider-specific parameters and requirements.


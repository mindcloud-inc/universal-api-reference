# E2B: Set Sandbox Timeout

Sets a sandbox timeout in E2B.

```
PUT https://connect.mindcloud.co/v1/universal/e2B/latest/actions/set-sandbox-timeout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/set-sandbox-timeout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sandboxId": "string",
  "timeout": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/e2B/latest/actions/set-sandbox-timeout', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sandboxId": "string",
    "timeout": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sandboxId` | string | yes | Identifier of the sandbox. |
| `timeout` | number | yes | Timeout in seconds from now after which the sandbox should expire. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native E2B API returns.

## Native endpoint

Through the native E2B API, this operation is `POST /sandboxes/{sandboxID}/timeout` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-sandbox-timeout.md) for the provider-specific parameters and requirements.


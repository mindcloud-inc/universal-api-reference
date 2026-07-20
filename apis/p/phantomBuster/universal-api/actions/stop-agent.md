# PhantomBuster: Stop Agent

Stops a running agent in PhantomBuster.

```
PUT https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/stop-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/stop-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/stop-agent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cascadeToAllSlaves` | boolean | no |  |
| `dontLaunchSoon` | boolean | no |  |
| `id` | string | yes | The PhantomBuster agent ID to stop. |
| `softAbort` | boolean | no |  |
| `switchToManualLaunch` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PhantomBuster API returns.

## Native endpoint

Through the native PhantomBuster API, this operation is `POST /agents/stop` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-agent.md) for the provider-specific parameters and requirements.


# PhantomBuster: Schedule Agent Launch

Schedules an agent launch in PhantomBuster.

```
POST https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/schedule-agent-launch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PhantomBuster `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/schedule-agent-launch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "minutes": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phantomBuster/latest/actions/schedule-agent-launch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "minutes": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `argument` | object | no |  |
| `arguments` | object | no |  |
| `id` | string | yes | The PhantomBuster agent ID to schedule for launch. |
| `minutes` | number | yes |  |
| `saveArgument` | boolean | no |  |
| `saveArguments` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native PhantomBuster API returns.

## Native endpoint

Through the native PhantomBuster API, this operation is `POST /agents/launch-soon` (base URL `https://api.phantombuster.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-agent-launch.md) for the provider-specific parameters and requirements.


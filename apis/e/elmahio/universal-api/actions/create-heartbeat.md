# elmah.io: Create Heartbeat

Creates a new heartbeat in elmah.io.

```
POST https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-heartbeat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a elmah.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-heartbeat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "logId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/create-heartbeat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "logId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `logId` | string | yes | The ID of the log containing the heartbeat check. |
| `id` | string | yes | The ID of the heartbeat check. |
| `result` | string | no | The result of this heartbeat. |
| `reason` | string | no | Why the heartbeat is degraded or unhealthy. |
| `application` | string | no | Optional application name to associate with the heartbeat. |
| `version` | string | no | Optional application version to associate with the heartbeat. |
| `took` | number | no | How many milliseconds the task took to execute. |
| `checks[]` | array<object> | no | A list of individual checks included in the heartbeat. |
| `checks[].name` | string | no | The name of the individual check. |
| `checks[].took` | number | no | How many milliseconds the individual check took. |
| `checks[].result` | string | no | The result of the individual check. |
| `checks[].reason` | string | no | Why the individual check is degraded or unhealthy. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native elmah.io API returns.

## Native endpoint

Through the native elmah.io API, this operation is `POST /v3/heartbeats/:logId/:id` (base URL `https://api.elmah.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-heartbeat.md) for the provider-specific parameters and requirements.


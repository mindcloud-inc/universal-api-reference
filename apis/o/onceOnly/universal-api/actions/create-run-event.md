# OnceOnly: Create Run Event

Creates a run event in OnceOnly.

```
POST https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-run-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceOnly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-run-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "runId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-run-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "runId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `runId` | string | yes | Run id that owns the event. |
| `type` | string | yes | Event type. |
| `ts` | number | no | Optional event timestamp. |
| `status` | string | no | Optional event status. |
| `durationMs` | number | no | Optional duration in milliseconds. |
| `step` | string | no | Optional step label. |
| `tool` | string | no | Optional tool name. |
| `reqId` | string | no | Optional request id. |
| `leaseId` | string | no | Optional lease id. |
| `agentId` | string | no | Optional agent id. |
| `message` | string | no | Optional human-readable event message. |
| `data` | object | no | Optional structured event data object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceOnly API returns.

## Native endpoint

Through the native OnceOnly API, this operation is `POST /v1/events` (base URL `https://api.onceonly.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-run-event.md) for the provider-specific parameters and requirements.


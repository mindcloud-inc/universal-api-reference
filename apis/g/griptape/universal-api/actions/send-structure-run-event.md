# Griptape: Send Structure Run Event

Sends a structure run event to Griptape.

```
POST https://connect.mindcloud.co/v1/universal/griptape/latest/actions/send-structure-run-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/send-structure-run-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "structureRunId": "string",
  "payload": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/griptape/latest/actions/send-structure-run-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "structureRunId": "string",
    "payload": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `structureRunId` | string | yes | The structure run ID to publish events to. |
| `payload` | object | yes | Event payload object to publish into the Structure Run event stream. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Optional event type. Griptape defaults this to UserEvent when omitted. |
| `timestamp` | number | no | Optional UNIX timestamp for the event. If omitted, Griptape sets the current time. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Griptape API returns.

## Native endpoint

Through the native Griptape API, this operation is `POST /api/structure-runs/:structure_run_id/events` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-structure-run-event.md) for the provider-specific parameters and requirements.


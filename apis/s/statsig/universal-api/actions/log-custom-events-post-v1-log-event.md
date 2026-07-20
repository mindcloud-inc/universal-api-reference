# Statsig: Log Custom Events

Logs custom events to Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/log-custom-events-post-v1-log-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/log-custom-events-post-v1-log-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/log-custom-events-post-v1-log-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events` | list<object> | yes | Array of events to log. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `user` | object | no | Shared user object for all events; individual events may override it. |
| `statsigMetadata` | object | no | SDK metadata for diagnostics and exposure behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether events were accepted. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/log_event` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-custom-events-post-v1-log-event.md) for the provider-specific parameters and requirements.


# Mixpanel: Track Events

Creates new tracked events in Mixpanel.

```
POST https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/track-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mixpanel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/track-events" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "events[].event": "string",
  "events[].properties.time": 1,
  "events[].properties.distinctId": "string",
  "events[].properties.insertId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mixpanel/latest/actions/track-events', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "events[].event": "string",
    "events[].properties.time": 1,
    "events[].properties.distinctId": "string",
    "events[].properties.insertId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `events[].event` | string | yes | The event name for one tracked event row. |
| `events[].properties.time` | number | yes | Event time in seconds or milliseconds since UTC epoch. |
| `events[].properties.distinctId` | string | yes | Distinct ID for the user who performed the event. |
| `events[].properties.insertId` | string | yes | Unique event identifier used for deduplication. |
| `events[].properties.extraProperties` | object | no | Additional custom event properties to merge into the event properties object. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `verbose` | number | no | When 1, Mixpanel responds with a JSON object describing success or failure. Default: `1`. |
| `ip` | number | no | When 1, Mixpanel uses the request IP to compute a distinct ID if one is not provided. |
| `img` | number | no | When 1, Mixpanel returns a 1x1 transparent pixel response. |
| `callback` | string | no | Optional JavaScript callback name for JSONP-style responses. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message returned when Mixpanel rejects the track request. |
| `status` | number | Verbose track result status where 1 indicates success and 0 indicates failure. |

## Native endpoint

Through the native Mixpanel API, this operation is `POST https://api.mixpanel.com/track` (base URL `https://mixpanel.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-events.md) for the provider-specific parameters and requirements.


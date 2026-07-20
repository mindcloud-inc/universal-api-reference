# Dashly: Track User Event

Tracks an event for a Dashly user.

```
POST https://connect.mindcloud.co/v1/universal/dashly/latest/actions/track-user-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashly/latest/actions/track-user-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashly/latest/actions/track-user-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "event": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `byUserId` | boolean | no | Default: `true`. |
| `event` | string | yes |  |
| `params` | string | no | JSON object string with event properties, for example {"item":"chicken"}. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idAsString` | boolean | no | Default: `true`. |
| `created` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dashly API returns.

## Native endpoint

Through the native Dashly API, this operation is `POST users/:id/events` (base URL `https://api.dashly.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-user-event.md) for the provider-specific parameters and requirements.


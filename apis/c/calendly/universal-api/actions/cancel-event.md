# Calendly: Cancel Event

Cancels a scheduled event in Calendly.

```
POST https://connect.mindcloud.co/v1/universal/calendly/latest/actions/cancel-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calendly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/cancel-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event_uuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/calendly/latest/actions/cancel-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event_uuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event_uuid` | string | yes | Scheduled event UUID to cancel. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reason` | string | no | Cancellation reason. Default: `Canceled via API`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Calendly API returns.

## Native endpoint

Through the native Calendly API, this operation is `POST /scheduled_events/:event_uuid/cancellation` (base URL `https://api.calendly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-event.md) for the provider-specific parameters and requirements.


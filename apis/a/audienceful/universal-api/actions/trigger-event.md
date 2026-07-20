# Audienceful: Trigger Event

Triggers Audienceful automations by event name.

```
POST https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/trigger-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Audienceful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/trigger-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "event": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audienceful/latest/actions/trigger-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "event": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `event` | string | yes | The event name to trigger. |
| `email` | string | yes | The person's email. |
| `eventProperties` | object | no | Event property payload used in automations. |
| `fields` | object | no | Field values to merge onto the person before the event runs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Audienceful API, this operation is `POST /automations/event/` (base URL `https://app.audienceful.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-event.md) for the provider-specific parameters and requirements.


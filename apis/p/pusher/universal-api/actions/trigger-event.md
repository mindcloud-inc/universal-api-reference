# Pusher: Trigger Event

Triggers an event in Pusher.

```
POST https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pusher `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pusher/latest/actions/trigger-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | no | Publish to a single channel. Use this instead of Channels when sending to one channel. |
| `channels[]` | array<string> | no | Publish to one or more channels. Pusher limits this array to 100 channels. |
| `data` | string | yes | The event payload. Pusher expects this as the event data value and limits it to 10KB. |
| `info` | string | no | Comma-separated channel attributes to return, such as user_count or subscription_count. |
| `name` | string | yes | The event name to publish. |
| `socketId` | string | no | Exclude the event from being sent to a specific connection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channels": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channels` | object | Returned only when the request asks for channel info. |

## Native endpoint

Through the native Pusher API, this operation is `POST /apps/{{credentials.appId}}/events` (base URL `https://api-{{credentials.cluster}}.pusher.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-event.md) for the provider-specific parameters and requirements.


# Element: Send Room Message

Creates a message in an Element room.

```
POST https://connect.mindcloud.co/v1/universal/element/latest/actions/send-room-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Element `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/element/latest/actions/send-room-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": "string",
  "txnId": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/element/latest/actions/send-room-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": "string",
    "txnId": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | yes | Room ID that should receive the message. |
| `txnId` | string | yes | Client-generated transaction ID for idempotent message sends. |
| `body` | string | yes | Plain-text message body to send. |
| `msgtype` | string | no | Matrix message type. Defaults to m.text. Default: `m.text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_id` | string |  |

## Native endpoint

Through the native Element API, this operation is `PUT /_matrix/client/v3/rooms/:roomId/send/m.room.message/:txnId` (base URL `{{credentials.homeserverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-room-message.md) for the provider-specific parameters and requirements.


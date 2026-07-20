# MojoTxt: Update Message

Updates a message in MojoTxt.

```
PUT https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/update-message', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Lists[]` | array<number> | no | One or more list IDs to send the message to. |
| `media` | string | no | Media URL required when sending an MMS. |
| `message` | string | no | The updated message body. |
| `messageId` | string | yes | The message identifier to update. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `publishTime` | number | no | UNIX timestamp for when the message should be sent. |
| `scheduleType` | string | no | S for a specific send time or R for a time relative to subscription. |
| `sendAfter` | number | no | Delay before sending a relative message. |
| `sendAfterUnit` | string | no | Unit for SendAfter: hour, day, week, month, or year. |
| `type` | string | no | SMS or MMS. |
| `url` | string | no | Tracking URL to append to the outgoing message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "result": "string",
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable update result message. |
| `result` | string | Whether the update request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `POST /:phoneNumber/messages/update/:messageId` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-message.md) for the provider-specific parameters and requirements.


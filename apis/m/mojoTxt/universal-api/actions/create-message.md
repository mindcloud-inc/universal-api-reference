# MojoTxt: Create Message

Creates a message in MojoTxt.

```
POST https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MojoTxt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Lists[]": [
    1
  ],
  "message": "string",
  "phoneNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/create-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Lists[]": [1],
    "message": "string",
    "phoneNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Lists[]` | array<number> | yes | One or more list IDs to send the message to. |
| `media` | string | no | Media URL required when sending an MMS. |
| `message` | string | yes | The message body to send. |
| `phoneNumber` | string | yes | The MojoTxt phone number in international format, like +17792533748. |
| `publishTime` | number | no | UNIX timestamp for when the message should be sent. |
| `scheduleType` | string | no | S for a specific send time or R for a time relative to subscription. |
| `sendAfter` | number | no | Delay before sending a relative message. |
| `sendAfterUnit` | string | no | Unit for SendAfter: hour, day, week, month, or year. |
| `type` | string | no | The message type, either SMS or MMS. |
| `url` | string | no | Tracking URL to append to the outgoing message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_id": 1,
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
| `created_id` | number | ID of the newly created message. |
| `message` | string | Human-readable create result message. |
| `result` | string | Whether the create request succeeded. |
| `timestamp` | number | MojoTxt server timestamp for the response. |

## Native endpoint

Through the native MojoTxt API, this operation is `POST /:phoneNumber/messages/add` (base URL `https://app.mojotxt.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-message.md) for the provider-specific parameters and requirements.


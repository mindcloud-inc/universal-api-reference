# SMS.to: Send Flash Message

Sends a single flash SMS message through SMS.to.

```
POST https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/send-flash-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/send-flash-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSto/latest/actions/send-flash-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | yes | Your message. |
| `to` | string | yes | Phone number. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bypassOptout` | boolean | no | True will bypass opt-outs. |
| `senderId` | string | no | The displayed value of who sent the message. |
| `callbackUrl` | string | no | A callback URL for message status updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "messageId": "string",
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
| `messageId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native SMS.to API, this operation is `POST /fsms/send` (base URL `https://api.sms.to`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-flash-message.md) for the provider-specific parameters and requirements.


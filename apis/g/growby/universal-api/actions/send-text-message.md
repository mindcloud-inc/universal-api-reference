# Growby: Send Text Message

Sends a text message through Growby.

```
POST https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-text-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-text-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "15551234567",
  "to": "15551234567",
  "message.text": "This is a simple text message."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-text-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "15551234567",
    "to": "15551234567",
    "message.text": "This is a simple text message."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | WhatsApp business phone number with country code, for example 15551234567 or +15551234567. Example: `15551234567`. |
| `to` | string | yes | Recipient phone number with country code, for example 15551234567 or +15551234567. Example: `15551234567`. |
| `message.text` | string | yes | Text content to send. Growby documents a maximum length of 4096 characters. Example: `This is a simple text message.`. |
| `showInInbox` | boolean | no | Whether to show the message in the Growby inbox. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Growby API, this operation is `POST /v3/messages` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-text-message.md) for the provider-specific parameters and requirements.


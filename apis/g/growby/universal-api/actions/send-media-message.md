# Growby: Send Media Message

Sends a media message through Growby.

```
POST https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-media-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-media-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "15551234567",
  "to": "15551234567",
  "message.link": "https://upload.wikimedia.org/wikipedia/commons/3/3f/JPEG_example_flower.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-media-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "15551234567",
    "to": "15551234567",
    "message.link": "https://upload.wikimedia.org/wikipedia/commons/3/3f/JPEG_example_flower.jpg"
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
| `message.link` | string | yes | Publicly accessible image URL. Growby supports JPEG and PNG images up to 5 MB. Example: `https://upload.wikimedia.org/wikipedia/commons/3/3f/JPEG_example_flower.jpg`. |
| `message.text` | string | no | Optional caption shown with the media. Example: `Here is the image you requested.`. |
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

Through the native Growby API, this operation is `POST /v3/messages` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-media-message.md) for the provider-specific parameters and requirements.


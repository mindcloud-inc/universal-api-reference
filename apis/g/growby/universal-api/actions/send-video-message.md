# Growby: Send Video Message

Sends a video message through Growby.

```
POST https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-video-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Growby `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-video-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "15551234567",
  "to": "15551234567",
  "message.link": "https://samplelib.com/lib/preview/mp4/sample-5s.mp4"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/growby/latest/actions/send-video-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "15551234567",
    "to": "15551234567",
    "message.link": "https://samplelib.com/lib/preview/mp4/sample-5s.mp4"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | WhatsApp business phone number with country code. Example: `15551234567`. |
| `message.text` | string | no | Optional caption shown with the video. |
| `showInInbox` | string | no | Whether to show the message in the Growby inbox. |
| `to` | string | yes | Recipient phone number with country code. Example: `15551234567`. |
| `message.link` | string | yes | Publicly accessible MP4 or 3GP video URL. Example: `https://samplelib.com/lib/preview/mp4/sample-5s.mp4`. |

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

Through the native Growby API, this operation is `POST /v3/messages` (base URL `https://api.growby.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-video-message.md) for the provider-specific parameters and requirements.


# SendApp: Send Media Message



```
POST https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-media-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SendApp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-media-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://example.com",
  "number": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendApp/latest/actions/send-media-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://example.com",
    "number": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | no | Optional filename sent with the media. |
| `mediaUrl` | string | yes | Public URL of the file to send. |
| `message` | string | no | Optional caption for the media. |
| `number` | string | yes | WhatsApp number in international format with the + prefix. |
| `type` | string | yes | Media type to send: image, video, audio, or document. |

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
| `response` | string | Provider docs do not publish a structured send-media success response example. |

## Native endpoint

Through the native SendApp API, this operation is `GET /send/media` (base URL `https://official.sendapp.cloud/apiv3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-media-message.md) for the provider-specific parameters and requirements.


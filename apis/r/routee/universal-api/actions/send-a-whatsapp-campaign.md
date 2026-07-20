# Routee: Send a Whatsapp campaign

Sends a WhatsApp campaign with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-whatsapp-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-whatsapp-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "string",
  "to": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-whatsapp-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "string",
    "to": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | The phone provided by the customer during the WABA account setup. It is the phone that receives the verification pin. |
| `to` | string | yes | The recipient of the message. Could be one of - phone number in international format. In this it should follow the guidelines of E.164 but leading 00 is as well accepted - group id |
| `text` | string | yes | The text to be sent. 4069 chars, UTF-8 support |
| `imageURL` | string | no | the url of the location where the image is stored. http or https, ASCII char set, supported formats are png, jpeg. Post-Processing Media Size 5MB. |
| `videoURL` | string | no | the url of the location where the video file is stored. http or https, ASCII char set, supported formats video/mp4, video/3gpp. Post-Processing media size 16MB. |
| `documentURL` | string | no | the url of the location where the document is stored. Any valid MIME-type is supported, post-Processing Media Size 100 MB. |
| `filename` | string | no | File name of the document to be shown. It is shown on the uploaded document when the channel supports this. Max 512 chars, UTF-8. |
| `caption` | string | no | Additional caption for the image / document / video. It is shown on the uploaded image / document / video when the Whatsapp supports this. Max 512 chars, UTF-8 |
| `audioURL` | string | no | the url of the location where the audio file is stored. Supported content is audio/aac, audio/mp4, audio/amr, audio/mpeg, audio/ogg; codecs=opus Note: The base audio/ogg type is not supported. Post-Processing Media Size 16MB |
| `stickerURL` | string | no | the url of the location where the sticker is stored. http or https, ASCII char set. Supported formats image/webp, post processing media size 100KB. |
| `longitude` | number | no | Longitude part of the coordinate. +/-180 |
| `latitude` | number | no | Latitude part of the coordinate. +/-180 |
| `locationName` | string | no | Optional name of location. 256 chars. |
| `locationAddress` | string | no | Optional address, will only be rendered if name is set. 256 chars. |
| `template` | object | no | The message template to be send. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "trackingId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /campaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-whatsapp-campaign.md) for the provider-specific parameters and requirements.


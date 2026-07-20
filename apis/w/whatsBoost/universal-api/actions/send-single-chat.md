# WhatsBoost: Send Single Chat

Sends a single chat message from WhatsBoost.

```
POST https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-single-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-single-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "recipient": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-single-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "recipient": "string",
    "message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account` | string | yes | WhatsApp account you want to use for sending. You can get the account unique ID from /get/wa.accounts or in the dashboard. |
| `recipient` | string | yes | Recipient mobile number or group address. Accepts WhatsApp group address or E.164 formatted number and locally formatted numbers using the country code from your profile settings. Example: E.164: +34612345678, Local: 612345678. |
| `type` | string | no | Type of WhatsApp message. |
| `message` | string | yes | Message or caption you want to send. Spintax is also supported. |
| `priority` | number | no | If you want to send the message as priority, it will be sent immediately. 1 for yes and 2 for no. |
| `media_file` | string | no | For 'media' type messages only. The media file you want to attach in the WhatsApp message. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_url` | string | no | For 'media' type messages only. The media file URL. Must be a direct link to the media file. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_type` | string | no | For 'media' type messages only. Required if using 'media_url'. Specifies the file type of the media in the provided URL. |
| `document_file` | string | no | For 'document' type messages only. The document file you want to attach in the WhatsApp message. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_url` | string | no | For 'document' type messages only. The document file URL. Must be a direct link to the document file. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_name` | string | no | For 'document' type with 'document_url' messages only. The document file name. Include the file extension (e.g., document.pdf). |
| `document_type` | string | no | For 'document' type messages only. Required if using 'document_url'. Specifies the file type of the document in the provided URL. |
| `shortener` | number | no | Shortener ID. Specify the shortener you want to use to shorten links in your message. Get the list of available shorteners from /get/shorteners. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /send/whatsapp` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-single-chat.md) for the provider-specific parameters and requirements.


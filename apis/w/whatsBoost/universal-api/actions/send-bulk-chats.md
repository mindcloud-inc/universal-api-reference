# WhatsBoost: Send Bulk Chats

Sends bulk chat messages from WhatsBoost.

```
POST https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-bulk-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-bulk-chats" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account": "string",
  "campaign": "string",
  "type": "string",
  "message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-bulk-chats', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account": "string",
    "campaign": "string",
    "type": "string",
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
| `campaign` | string | yes | Name of the campaign, you will see this in the WhatsApp campaign manager. |
| `recipients` | string | no | List of phone numbers or group addresses separated by commas. Optional if 'groups' parameter is not empty. Accepts WhatsApp group address, E.164 formatted number, or locally formatted numbers using the country code from your profile settings. |
| `groups` | string | no | List of contact group IDs separated by commas. Optional if 'recipients' parameter is not empty. You can get group IDs from /get/groups (Your contact groups). |
| `type` | string | yes | Type of WhatsApp message. |
| `message` | string | yes | Message or caption you want to send. Spintax and shortcodes are supported. |
| `media_file` | string | no | For 'media' type messages only. The media file to attach to the WhatsApp message. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_url` | string | no | For 'media' type messages only. URL to the media file. Must be a direct link. Supports jpg, png, gif, mp4, mp3, and ogg files. |
| `media_type` | string | no | For 'media' type messages only. Required if using 'media_url' instead of 'media_file'. Declares the file type of the media in the provided URL. |
| `document_file` | string | no | For 'document' type messages only. The document file to attach to the WhatsApp message. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_url` | string | no | For 'document' type messages only. URL to the document file. Must be a direct link. Supports pdf, xml, xls, xlsx, doc, and docx files. |
| `document_name` | string | no | For 'document' type messages with 'document_url'. File name of the document. Include the file extension (e.g., document.pdf). |
| `document_type` | string | no | For 'document' type messages only. Required if using 'document_url' instead of 'document_file'. Declares the file type of the document in the provided URL. |
| `shortener` | number | no | Shortener ID. Specify the shortener to use for shortening links in your message. Get the list of available shorteners from /get/shorteners. |

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

Through the native WhatsBoost API, this operation is `POST /send/whatsapp.bulk` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-bulk-chats.md) for the provider-specific parameters and requirements.


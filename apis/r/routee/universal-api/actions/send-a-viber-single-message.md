# Routee: Send a Viber Single Message

Sends a Viber single message with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-single-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-single-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderInfoTrackingId": "string",
  "to": "string",
  "body.viberFile.fileName": "Ava Chen",
  "body.viberFile.fileType": "string",
  "body.viberFile.fileURL": "https://example.com",
  "body.viberVideo.videoURL": "https://example.com",
  "body.viberVideo.videoThumbnail": "string",
  "body.viberVideo.fileSize": 1,
  "body.viberVideo.duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-single-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderInfoTrackingId": "string",
    "to": "string",
    "body.viberFile.fileName": "Ava Chen",
    "body.viberFile.fileType": "string",
    "body.viberFile.fileURL": "https://example.com",
    "body.viberVideo.videoURL": "https://example.com",
    "body.viberVideo.videoThumbnail": "string",
    "body.viberVideo.fileSize": 1,
    "body.viberVideo.duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderInfoTrackingId` | string | yes | The unique sender id. You can find it at [Routee Platform-applications page](https://dev.routee.net/#/management/applications). |
| `to` | string | yes | The phone number the message is about to be sent to. Format with a '+' and country code e.g., +3069xxxxxxxx (E.164 format). |
| `body` | object | no | The body containing the content of the message. |
| `body.text` | string | no | The text of Viber message. Maximum number of characters supported in a Viber message is 1000 characters. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. [Text only messages are billed as Transactional. All the other message types are charged as Promotional]. |
| `body.imageURL` | string | no | The URL of the image (recommended image size: 400KB for optimal delivery; image URL length: max 1000 characters; only valid and secure URL starting with https://). |
| `body.action` | object | no | Represents the action (button) of the Viber message. |
| `body.action.caption` | string | no | The displayed text on the button (1-30 characters). |
| `body.action.targetUrl` | string | no | The target URL of the Viber action. |
| `body.viberFile` | object | no | Represents the Viber file of the Viber message. |
| `body.viberFile.fileName` | string | yes | The name of the file. Max size 25 chars. |
| `body.viberFile.fileType` | string | yes | Type of Viber message file. The supported file types are following: For document: doc, .docx, .rtf, .dot, .dotx, .odt ,odf, .fodt, .txt, .info; For PDF: pdf, .xps, .pdax, .eps; For Spreadsheet: .xls, .xlsx, .ods, .fods, .csv, .xlsm, .xltx . |
| `body.viberFile.fileURL` | string | yes | The URL of the document (recommended file size: 600KB for optimal delivery) (document URL length: up to 1000; only valid and secure URL starting with https://). |
| `body.viberVideo` | object | no | Represents the Viber video of the Viber message. |
| `body.viberVideo.videoURL` | string | yes | The URL where the video is hosted (1000 max chars, only https). |
| `body.viberVideo.videoThumbnail` | string | yes | The URL of a thumbnail for the video (1000 max chars, only https). |
| `body.viberVideo.fileSize` | number | yes | The file size in MB (positive number, 200 max). |
| `body.viberVideo.duration` | number | yes | The video’s duration in seconds (positive number, 600 max). |
| `ttl` | number | no | Time range until message expires. TTL range in seconds: 30 - 86400 seconds. If it is not set, the default range is 14 days. |
| `callbackUrl` | string | no | Defines the callback URL that will receive all the individual messages' progress of the Viber campaign. |
| `inboundUrl` | string | no | Defines the callback URL that will receive the inbound messages. |
| `label` | string | no | A generic label which can be used for tagging the Viber message. Maximum length is 350 characters. |
| `isSessionMessage` | boolean | no | Indicates a Viber Single is a Viber Session if the value is true. False by default. Learn more about session messaging at our [documentation](https://docs.routee.net/docs/send-a-viber-session). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "callbackUrl": "https://example.com",
      "country": "string",
      "direction": "string",
      "from": "string",
      "imageUrl": "https://example.com",
      "inboundUrl": "https://example.com",
      "message": "string",
      "sessionMessage": true,
      "status": {
        "date": "string",
        "status": "string"
      },
      "to": "string",
      "trackingId": "string",
      "ttl": "string",
      "viberAction": {
        "caption": "string",
        "targetUrl": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationName` | string |  |
| `callbackUrl` | string |  |
| `country` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `imageUrl` | string |  |
| `inboundUrl` | string |  |
| `message` | string |  |
| `sessionMessage` | boolean |  |
| `status` | object |  |
| `status.date` | string |  |
| `status.status` | string |  |
| `to` | string |  |
| `trackingId` | string |  |
| `ttl` | string |  |
| `viberAction` | object |  |
| `viberAction.caption` | string |  |
| `viberAction.targetUrl` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /viber` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-viber-single-message.md) for the provider-specific parameters and requirements.


# Routee: Send a Viber Campaign

Sends a Viber campaign with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "senderInfoTrackingId": "string",
  "body": {},
  "body.viberFile.fileName": "Ava Chen",
  "body.viberFile.fileType": "string",
  "body.viberFile.fileUrl": "https://example.com",
  "body.viberVideo.videoURL": "https://example.com",
  "body.viberVideo.fileSize": 1,
  "body.viberVideo.videoThumbnail": "string",
  "body.viberVideo.duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-viber-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "senderInfoTrackingId": "string",
    "body": {},
    "body.viberFile.fileName": "Ava Chen",
    "body.viberFile.fileType": "string",
    "body.viberFile.fileUrl": "https://example.com",
    "body.viberVideo.videoURL": "https://example.com",
    "body.viberVideo.fileSize": 1,
    "body.viberVideo.videoThumbnail": "string",
    "body.viberVideo.duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `senderInfoTrackingId` | string | yes | The unique sender id. You can find it at [Routee Platform-applications page](https://go.routee.net/#/management/applications). |
| `to[]` | array<string> | no | The phone numbers (array) the message is about to be sent to. Format with a '+' and country code e.g., +306948530920 (E.164 format). Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `contacts[]` | array<string> | no | The contact ids that the message will be sent to. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `groups[]` | array<string> | no | The groups of contacts in the account selected as recipients. Groups have to be created at the system. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `campaignName` | string | no | The name of the viber campaign. If you want to be able to track the whole campaign from Routee web platform use a name. Must be between 2 and 30 characters and contain only latin letters, numbers, spaces and - |
| `isSessionMessage` | boolean | no | Indicates a Viber Campaign is initiated to be a Viber Session. The session rate is applied ONLY after recipient response. Billed per session not per each delivered message. Supported session types are: Text-Only, Image and File. Default value false. Learn more about it at [our documention](https://docs.routee.net/docs/send-a-viber-session) |
| `scheduledDate` | date | no | Defines the scheduled date and time in UTC. (eg YYYY-MM-DDThh:mm:ssTZD where TZD is the time zone designator (Z or +hh:mm or -hh:mm)) |
| `body` | object | yes | Represents the viber message. When the viber message has only text, then the message is transactional. Otherwise, it is promotional. The supported viber message layouts are: Text, Image, Text + Action, Text + Action + Image. Check [here](/docs/other-viber-messaging-concept) for details. |
| `body.text` | string | no | The text of viber message. Maximum number of characters supported in a Viber message is 1000 characters. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. [Text only messages are billed as Transactional. All the other message types are charged as Promotional] |
| `body.imageURL` | string | no | The url of the image. (recommended image size: 400KB for optimal delivery; image url length: max 1000 characters; only valid and secure URL starting with https:/) |
| `body.action` | object | no | Represents the action(button) of the viber message. |
| `body.action.caption` | string | no | The displayed text on the button (1-30 characters). |
| `body.action.targetUrl` | string | no | The target URL of the viber action. |
| `body.viberFile` | object | no | Represents the Viber file of the Viber message. |
| `body.viberFile.fileName` | string | yes | The name of the file. Max size 25 chars |
| `body.viberFile.fileType` | string | yes | Type of viber message file. The supported file types are following: For document: doc, .docx, .rtf, .dot, .dotx, .odt ,odf, .fodt, .txt, .info For PDF: pdf, .xps, .pdax, .eps For Spreadsheet: .xls, .xlsx, .ods, .fods, .csv, .xlsm, .xltx |
| `body.viberFile.fileUrl` | string | yes | The url of the document. (recommended file size: 600KB for optimal delivery) (document url length: up to 1000; only valid and secure URL starting with https:/) |
| `ttl` | number | no | Time range until message expires. TTL range in seconds: 30 - 86400 seconds. If it is not set, the default range is 14 days. TTL range in seconds for web clients: 300 - 86400 seconds. |
| `callbackUrl` | string | no | Defines the callback URL that will receive all the individual messages' progress of the Viber campaign. Check [here](/docs/viber-callback) for details. |
| `inboundUrl` | string | no | Defines the callback URL that will receive the inbound messages. Check [here](/docs/viber-inbound-messages) for details. |
| `label` | string | no | A generic label which can be used for tagging the Viber message. Maximum length is 350 characters. |
| `body.viberVideo` | object | no | Represents the Viber video of the Viber message. |
| `body.viberVideo.videoURL` | string | yes | The URL where the video is hosted (1000 max chars, only https). |
| `body.viberVideo.fileSize` | number | yes | The file size in MB (positive number, 200 max). |
| `body.viberVideo.videoThumbnail` | string | yes | The URL of a thumbnail for the video (1000 max chars, only https). |
| `body.viberVideo.duration` | number | yes | The video’s duration in seconds (positive number, 600 max). |
| `body.fallbackValues` | object | no | Defines the default values in case a contact does not contain any of the selected personalized labels. It is an object with key-values pairs. The key refers to the label name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "action": {
          "caption": "string",
          "targetUrl": "https://example.com"
        },
        "imageURL": "https://example.com",
        "text": "string"
      },
      "callbackUrl": "https://example.com",
      "campaignName": "Ava Chen",
      "cost": 1,
      "createdAt": "string",
      "groups": [
        [
          "string"
        ]
      ],
      "inboundUrl": "https://example.com",
      "isSessionMessage": true,
      "label": "string",
      "respectQuietHours": true,
      "scheduledDate": "string",
      "senderInfoName": "Ava Chen",
      "senderInfoTrackingId": "string",
      "state": "string",
      "to": [
        [
          "string"
        ]
      ],
      "totalMessages": 1,
      "trackingId": "string",
      "ttl": 1,
      "type": "string",
      "viberAnalysis": {
        "bodyAnalysis": {
          "characters": 1
        },
        "contacts": {},
        "numberOfRecipients": 1,
        "recipientCountries": {
          "+37xxxxxxxxxx": "string"
        },
        "recipientsPerCountry": {
          "XX": 1
        },
        "recipientsPerGroup": {
          "Group name": 1
        },
        "totalInGroups": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | object |  |
| `body.action` | object |  |
| `body.action.caption` | string |  |
| `body.action.targetUrl` | string |  |
| `body.imageURL` | string |  |
| `body.text` | string |  |
| `callbackUrl` | string |  |
| `campaignName` | string |  |
| `cost` | number |  |
| `createdAt` | string |  |
| `groups[]` | array<string> |  |
| `inboundUrl` | string |  |
| `isSessionMessage` | boolean |  |
| `label` | string |  |
| `respectQuietHours` | boolean |  |
| `scheduledDate` | string |  |
| `senderInfoName` | string |  |
| `senderInfoTrackingId` | string |  |
| `state` | string |  |
| `to[]` | array<string> |  |
| `totalMessages` | number |  |
| `trackingId` | string |  |
| `ttl` | number |  |
| `type` | string |  |
| `viberAnalysis` | object |  |
| `viberAnalysis.bodyAnalysis` | object |  |
| `viberAnalysis.bodyAnalysis.characters` | number |  |
| `viberAnalysis.contacts` | object |  |
| `viberAnalysis.numberOfRecipients` | number |  |
| `viberAnalysis.recipientCountries` | object |  |
| `viberAnalysis.recipientCountries.+37xxxxxxxxxx` | string |  |
| `viberAnalysis.recipientsPerCountry` | object |  |
| `viberAnalysis.recipientsPerCountry.XX` | number |  |
| `viberAnalysis.recipientsPerGroup` | object |  |
| `viberAnalysis.recipientsPerGroup.Group name` | number |  |
| `viberAnalysis.totalInGroups` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /viber/campaign` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-viber-campaign.md) for the provider-specific parameters and requirements.


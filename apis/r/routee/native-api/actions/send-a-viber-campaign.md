# Send a Viber Campaign with Routee

Sends a Viber campaign with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber/campaign`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Viber Campaign](https://docs.routee.net/reference/send-a-viber-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `senderInfoTrackingId` | body | `string` | yes | The unique sender id. You can find it at [Routee Platform-applications page](https://go.routee.net/#/management/applications). |
| `to[]` | body | `array<string>` | no | The phone numbers (array) the message is about to be sent to. Format with a '+' and country code e.g., +306948530920 (E.164 format). Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `contacts[]` | body | `array<string>` | no | The contact ids that the message will be sent to. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `groups[]` | body | `array<string>` | no | The groups of contacts in the account selected as recipients. Groups have to be created at the system. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `campaignName` | body | `string` | no | The name of the viber campaign. If you want to be able to track the whole campaign from Routee web platform use a name. Must be between 2 and 30 characters and contain only latin letters, numbers, spaces and - |
| `isSessionMessage` | body | `boolean` | no | Indicates a Viber Campaign is initiated to be a Viber Session. The session rate is applied ONLY after recipient response. Billed per session not per each delivered message. Supported session types are: Text-Only, Image and File. Default value false. Learn more about it at  [our documention](https://docs.routee.net/docs/send-a-viber-session) |
| `scheduledDate` | body | `date` | no | Defines the scheduled date and time in UTC. (eg YYYY-MM-DDThh:mm:ssTZD where TZD is the time zone designator (Z or +hh:mm or -hh:mm)) |
| `body` | body | `object` | yes | Represents the viber message. When the viber message has only text, then the message is transactional. Otherwise, it is promotional. The supported viber message layouts are: Text, Image, Text + Action, Text + Action + Image. Check [here](/docs/other-viber-messaging-concept) for details. |
| `body.text` | body | `string` | no | The text of viber message. Maximum number of characters supported in a Viber message is 1000 characters. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. [Text only messages are billed as Transactional. All the other message types are charged as Promotional] |
| `body.imageURL` | body | `string` | no | The url of the image. (recommended image size: 400KB for optimal delivery; image url length: max 1000 characters; only valid and secure URL starting with https:/) |
| `body.action` | body | `object` | no | Represents the action(button) of the viber message. |
| `body.action.caption` | body | `string` | no | The displayed text on the button (1-30 characters). |
| `body.action.targetUrl` | body | `string` | no | The target URL of the viber action. |
| `body.viberFile` | body | `object` | no | Represents the Viber file of the Viber message. |
| `body.viberFile.fileName` | body | `string` | yes | The name of the file. Max size 25 chars |
| `body.viberFile.fileType` | body | `string` | yes | Type of viber message file. The supported file types are following:  For document: doc, .docx, .rtf, .dot, .dotx, .odt ,odf, .fodt, .txt, .info  For PDF: pdf, .xps, .pdax, .eps  For Spreadsheet: .xls, .xlsx, .ods, .fods, .csv, .xlsm, .xltx |
| `body.viberFile.fileUrl` | body | `string` | yes | The url of the document. (recommended file size: 600KB for optimal delivery) (document url length: up to 1000; only valid and secure URL starting with https:/) |
| `ttl` | body | `number` | no | Time range until message expires. TTL range in seconds: 30 - 86400 seconds. If it is not set, the default range is 14 days. TTL range in seconds for web clients: 300 - 86400 seconds. |
| `callbackUrl` | body | `string` | no | Defines the callback URL that will receive all the individual messages' progress of the Viber campaign. Check [here](/docs/viber-callback) for details. |
| `inboundUrl` | body | `string` | no | Defines the callback URL that will receive the inbound messages. Check [here](/docs/viber-inbound-messages) for details. |
| `label` | body | `string` | no | A generic label which can be used for tagging the Viber message. Maximum length is 350 characters. |
| `body.viberVideo` | body | `object` | no | Represents the Viber video of the Viber message. |
| `body.viberVideo.videoURL` | body | `string` | yes | The URL where the video is hosted (1000 max chars, only https). |
| `body.viberVideo.fileSize` | body | `number` | yes | The file size in MB (positive number, 200 max). |
| `body.viberVideo.videoThumbnail` | body | `string` | yes | The URL of a thumbnail for the video (1000 max chars, only https). |
| `body.viberVideo.duration` | body | `number` | yes | The video’s duration in seconds (positive number, 600 max). |
| `body.fallbackValues` | body | `object` | no | Defines the default values in case a contact does not contain any of the selected personalized labels. It is an object with key-values pairs. The key refers to the label name. |

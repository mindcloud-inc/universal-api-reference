# Send a Viber Single Message with Routee

Sends a Viber single message with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/viber`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Viber Single Message](https://docs.routee.net/reference/send-a-viber-single-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `senderInfoTrackingId` | body | `string` | yes | The unique sender id. You can find it at  [Routee Platform-applications page](https://dev.routee.net/#/management/applications). |
| `to` | body | `string` | yes | The phone number the message is about to be sent to. Format with a '+' and country code e.g., +3069xxxxxxxx (E.164 format). |
| `body` | body | `object` | no | The body containing the content of the message. |
| `body.text` | body | `string` | no | The text of Viber message. Maximum number of characters supported in a Viber message is 1000 characters. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. [Text only messages are billed as Transactional. All the other message types are charged as Promotional]. |
| `body.imageURL` | body | `string` | no | The URL of the image (recommended image size: 400KB for optimal delivery; image URL length: max 1000 characters; only valid and secure URL starting with https://). |
| `body.action` | body | `object` | no | Represents the action (button) of the Viber message. |
| `body.action.caption` | body | `string` | no | The displayed text on the button (1-30 characters). |
| `body.action.targetUrl` | body | `string` | no | The target URL of the Viber action. |
| `body.viberFile` | body | `object` | no | Represents the Viber file of the Viber message. |
| `body.viberFile.fileName` | body | `string` | yes | The name of the file. Max size 25 chars. |
| `body.viberFile.fileType` | body | `string` | yes | Type of Viber message file. The supported file types are following: For document: doc, .docx, .rtf, .dot, .dotx, .odt ,odf, .fodt, .txt, .info; For PDF: pdf, .xps, .pdax, .eps; For Spreadsheet: .xls, .xlsx, .ods, .fods, .csv, .xlsm, .xltx . |
| `body.viberFile.fileURL` | body | `string` | yes | The URL of the document (recommended file size: 600KB for optimal delivery) (document URL length: up to 1000; only valid and secure URL starting with https://). |
| `body.viberVideo` | body | `object` | no | Represents the Viber video of the Viber message. |
| `body.viberVideo.videoURL` | body | `string` | yes | The URL where the video is hosted (1000 max chars, only https). |
| `body.viberVideo.videoThumbnail` | body | `string` | yes | The URL of a thumbnail for the video (1000 max chars, only https). |
| `body.viberVideo.fileSize` | body | `number` | yes | The file size in MB (positive number, 200 max). |
| `body.viberVideo.duration` | body | `number` | yes | The video’s duration in seconds (positive number, 600 max). |
| `ttl` | body | `number` | no | Time range until message expires. TTL range in seconds: 30 - 86400 seconds. If it is not set, the default range is 14 days. |
| `callbackUrl` | body | `string` | no | Defines the callback URL that will receive all the individual messages' progress of the Viber campaign. |
| `inboundUrl` | body | `string` | no | Defines the callback URL that will receive the inbound messages. |
| `label` | body | `string` | no | A generic label which can be used for tagging the Viber message. Maximum length is 350 characters. |
| `isSessionMessage` | body | `boolean` | no | Indicates a Viber Single is a Viber Session if the value is true. False by default. Learn more about session messaging at our [documentation](https://docs.routee.net/docs/send-a-viber-session). |

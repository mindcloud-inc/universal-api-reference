# Routee: Send a Failover Message

Sends a failover message with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-failover-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-failover-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "flow[].from": "string",
  "flow[].to": "string",
  "flow[].message.body": "string",
  "flow[].senderInfoTrackingId": "string",
  "flow[].message.viberVideo.videoUrl": "https://example.com",
  "flow[].message.viberVideo.videoThumbnail": "string",
  "flow[].message.viberVideo.fileSize": 1,
  "flow[].message.viberVideo.duration": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-a-failover-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "flow[].from": "string",
    "flow[].to": "string",
    "flow[].message.body": "string",
    "flow[].senderInfoTrackingId": "string",
    "flow[].message.viberVideo.videoUrl": "https://example.com",
    "flow[].message.viberVideo.videoThumbnail": "string",
    "flow[].message.viberVideo.fileSize": 1,
    "flow[].message.viberVideo.duration": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `flow[]` | array<object> | no | SMS, Viber or Voice |
| `flow[].type` | string | no | The type of the flow channel. Supported values: *Sms* , *Viber* or *Voice* |
| `flow[].from` | string | yes | [For SMS and Voice] The name of the sender id, it can be a telephone number or an alphanumeric string. NOTICE FOR VOICE: Alphanumeric sender is not supported by all networks (e.g. Greek networks). Check restrictions and features here: https://go.routee.net/#/management/restrictions-and-features. |
| `flow[].to` | string | yes | [For Voice] The recipient number. |
| `flow[].ttl` | number | no | [For SMS and Viber] Time range until message expires in minutes (min 0.5 minute, max 1440 minutes). Default values 10 minutes for Viber messages and 1200 minutes for SMS. |
| `flow[].message` | object | no | Details about the message you want to send |
| `flow[].message.body` | string | yes | [For SMS only] The message you want to send. Use "\n" to create a new line in your message. |
| `flow[].message.flash` | boolean | no | [For SMS only] Indicates if the SMS is a flash SMS. A flash SMS is a type of SMS that appears directly on the main screen without user interaction and is not automatically stored in the inbox. It can be useful in emergencies, such as a fire alarm or cases of confidentiality, as in delivering one-time passwords. Default value false. |
| `flow[].message.label` | string | no | [For SMS only] A generic label which can be used for tagging the failover message. The maximum length is 350 characters. |
| `flow[].message.transcode` | boolean | no | [For SMS only] If “transcode” is set to true/false, then the message body will be/not be transcoded. If the “transcode” parameter is not set, then the application level setting will be used |
| `flow[].order` | number | no | Defines the priority order. |
| `flow[].failoverOnStatuses` | string | no | Defines the status which will trigger the next channel. Values for SMS channel can be: **Undelivered**, **Failed** Values for Viber channel can be: **Expired**, **Failed**, **Undelivered** Values for Voice channel can be **Completed**, **Busy**, **NoAnswer**, **Failed**, **Unsent**, **Terminated**. Values must be comma separated. The statuses are not case-sensitive Default values for SMS: **Undelivered**, **Failed** Default values for Viber: **Expired**, **Failed**, **Undelivered** Default values for Voice:**Busy**, **NoAnswer** *The statuses are not case-sensitive* |
| `flow[].senderInfoTrackingId` | string | yes | [For Viber only] The unique sender id. You can find it at: [Routee Platform-applications page](https://dev.routee.net/#/management/applications). |
| `flow[].inboundUrl` | string | no | [For Viber only] Defines the callback URL that will receive the inbound messages. Check [here](/docs/viber-inbound-messages) for details. |
| `flow[].message.text` | string | no | [For Viber only] The text of Viber message. The maximum number of characters supported in a Viber message is 1000 characters. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. [Text only messages are billed as Transactional. All the other message types are charged as Promotional] |
| `flow[].message.imageUrl` | string | no | [For Viber only] The URL of the image. (recommended image size: 400KB for optimal delivery; image url length: max 1000 characters; only valid and secure URL starting with https:/) |
| `flow[].message.action` | object | no | [For Viber only] Details about the action - caption and target url |
| `flow[].message.action.caption` | string | no | [For Viber only] The displayed text on the button (1-30 characters). |
| `flow[].message.action.targetUrl` | string | no | [For Viber only] The target URL of the Viber action. |
| `flow[].message.viberFile` | object | no | [For Viber only] Represents the viber file of the viber message. |
| `flow[].message.viberFile.fileName` | string | no | The name of the file. Max size 25 chars |
| `flow[].message.viberFile.fileType` | string | no | Type of viber message file. The supported file types are following: For document: doc, .docx, .rtf, .dot, .dotx, .odt ,odf, .fodt, .txt, .info For PDF: pdf, .xps, .pdax, .eps For Spreadsheet: .xls, .xlsx, .ods, .fods, .csv, .xlsm, .xltx |
| `flow[].message.viberFile.fileUrl` | string | no | The url of the document. (recommended file size: 600KB for optimal delivery) (document url length: up to 1000; only valid and secure URL starting with https:/) |
| `callback` | object | no | Details about the callback, more information at [Callbacks (Webhook)](doc:failover-callbacks) |
| `callback.strategy` | string | no | When the URL will be called. Two possible values: on every status change (OnStep) or when a final status arrives (OnCompletion). |
| `callback.url` | string | no | Defines the URL in which a payload with the information about the request will be posted |
| `flow[].expireOnDelivery` | boolean | no | If it's set to true then the service will set the status of the **Delivered** messages to **Expired** if the TTL value has passed and no **Seen** status has arrived. (Default value is false) |
| `restrictions` | object | no | [For SMS] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |
| `flow[].urlShortener` | object | no | [For SMS only] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination.. |
| `flow[].urlShortener.urlValidity` | number | no | [Optional]. Possible values: 3600 up to 2592000. Indicates the time in seconds that the shorten url will be valid (min: 3600 [one hour] - max: 2592000 [30 days]). Default value 2592000 |
| `flow[].to.phone` | string | no | The recipient phone [must exist (NotBlank) if viber and sip are both null] |
| `flow[].to.sip` | string | no | A valid sip address. (ex 1111@test.com:55080) [must exist (NotBlank) if phone and viber are both null] |
| `flow[].to.viber` | string | no | A valid phone number. The recipient should have the Viber application installed to be able to receive a Viber call. [must exist (NotBlank) if phone and sip are both null] |
| `flow[].dialplan` | object | no | A combination of action verbs to be executed. Can not be empty. Check [here](/docs/dialplan-verbs) for possible "SAY" and "PLAY" avalues. |
| `flow[].machineDetection` | object | no | [For Voice only] It is used to detect if the call is answered by human or machine and define the desired actions (in case of machine). |
| `flow[].message.viberVideo` | object | no | Represents the Viber video of the Viber message. |
| `flow[].message.viberVideo.videoUrl` | string | yes | The Url where the video is hosted (1000 max chars, only https). |
| `flow[].message.viberVideo.videoThumbnail` | string | yes | The Url of a thumbnail for the video (1000 max chars, only https). |
| `flow[].message.viberVideo.fileSize` | number | yes | The file size in MB (positive number, 200 max). |
| `flow[].message.viberVideo.duration` | number | yes | The video’s duration in seconds (positive number, 600 max). |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Routee API returns.

## Native endpoint

Through the native Routee API, this operation is `POST /failover` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-a-failover-message.md) for the provider-specific parameters and requirements.


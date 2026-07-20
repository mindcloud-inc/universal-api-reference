# Send a Failover Message with Routee

Sends a failover message with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/failover`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Failover Message](https://docs.routee.net/reference/send-a-failover-message)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `flow[]` | body | `array<object>` | no | SMS, Viber or Voice |
| `flow[].type` | body | `string` | no | The type of the flow channel. Supported values: *Sms* , *Viber* or *Voice* |
| `flow[].from` | body | `string` | yes | [For SMS and Voice] The name of the sender id, it can be a telephone number or an alphanumeric string. NOTICE FOR VOICE: Alphanumeric sender is not supported by all networks (e.g. Greek networks). Check restrictions and features here: https://go.routee.net/#/management/restrictions-and-features. |
| `flow[].to` | body | `string` | yes | [For Voice] The recipient number. |
| `flow[].ttl` | body | `number` | no | [For SMS and Viber] Time range until message expires in minutes (min 0.5 minute, max 1440 minutes). Default values 10 minutes for Viber messages and 1200 minutes for SMS. |
| `flow[].message` | body | `object` | no | Details about the message you want to send |
| `flow[].message.body` | body | `string` | yes | [For SMS only] The message you want to send. Use "\n" to create a new line in your message. |
| `flow[].message.flash` | body | `boolean` | no | [For SMS only] Indicates if the SMS is a flash SMS. A flash SMS is a type of SMS that appears directly on the main screen without user interaction and is not automatically stored in the inbox. It can be useful in emergencies, such as a fire alarm or cases of confidentiality, as in delivering one-time passwords. Default value false. |
| `flow[].message.label` | body | `string` | no | [For SMS only] A generic label which can be used for tagging the failover message. The maximum length is 350 characters. |
| `flow[].message.transcode` | body | `boolean` | no | [For SMS only] If “transcode” is set to true/false, then the message body will be/not be transcoded. If the “transcode” parameter is not set, then the application level setting will be used |
| `flow[].order` | body | `number` | no | Defines the priority order. |
| `flow[].failoverOnStatuses` | body | `string` | no | Defines the status which will trigger the next channel. Values for SMS channel can be: **Undelivered**, **Failed** Values for Viber channel can be: **Expired**, **Failed**, **Undelivered** Values for Voice channel can be **Completed**, **Busy**, **NoAnswer**, **Failed**, **Unsent**, **Terminated**.    Values must be comma separated.  The statuses are not case-sensitive Default values for SMS: **Undelivered**, **Failed** Default values for Viber: **Expired**, **Failed**, **Undelivered** Default values for Voice:**Busy**, **NoAnswer**   *The statuses are not case-sensitive* |
| `flow[].senderInfoTrackingId` | body | `string` | yes | [For Viber only] The unique sender id. You can find it at: [Routee Platform-applications page](https://dev.routee.net/#/management/applications). |
| `flow[].inboundUrl` | body | `string` | no | [For Viber only] Defines the callback URL that will receive the inbound messages. Check [here](/docs/viber-inbound-messages) for details. |
| `flow[].message.text` | body | `string` | no | [For Viber only] The text of Viber message. The maximum number of characters supported in a Viber message is 1000 characters. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. [Text only messages are billed as Transactional. All the other message types are charged as Promotional] |
| `flow[].message.imageUrl` | body | `string` | no | [For Viber only] The URL of the image.  (recommended image size: 400KB for optimal delivery; image url length: max 1000 characters; only valid and secure URL starting with https:/) |
| `flow[].message.action` | body | `object` | no | [For Viber only] Details about the action - caption and target url |
| `flow[].message.action.caption` | body | `string` | no | [For Viber only] The displayed text on the button (1-30 characters). |
| `flow[].message.action.targetUrl` | body | `string` | no | [For Viber only] The target URL of the Viber action. |
| `flow[].message.viberFile` | body | `object` | no | [For Viber only] Represents the viber file of the viber message. |
| `flow[].message.viberFile.fileName` | body | `string` | no | The name of the file. Max size 25 chars |
| `flow[].message.viberFile.fileType` | body | `string` | no | Type of viber message file. The supported file types are following:  For document: doc, .docx, .rtf, .dot, .dotx, .odt ,odf, .fodt, .txt, .info  For PDF: pdf, .xps, .pdax, .eps  For Spreadsheet: .xls, .xlsx, .ods, .fods, .csv, .xlsm, .xltx |
| `flow[].message.viberFile.fileUrl` | body | `string` | no | The url of the document. (recommended file size: 600KB for optimal delivery) (document url length: up to 1000; only valid and secure URL starting with https:/) |
| `callback` | body | `object` | no | Details about the callback, more information at [Callbacks (Webhook)](doc:failover-callbacks) |
| `callback.strategy` | body | `string` | no | When the URL will be called. Two possible values: on every status change (OnStep) or when a final status arrives (OnCompletion). |
| `callback.url` | body | `string` | no | Defines the URL in which a payload with the information about the request will be posted |
| `flow[].expireOnDelivery` | body | `boolean` | no | If it's set to true then the service will set the status of the **Delivered** messages to **Expired** if the TTL value has passed and no **Seen** status has arrived. (Default value is false) |
| `restrictions` | body | `object` | no | [For SMS] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |
| `flow[].urlShortener` | body | `object` | no | [For SMS only] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination.. |
| `flow[].urlShortener.urlValidity` | body | `number` | no | [Optional]. Possible values: 3600 up to 2592000. Indicates the time in seconds that the shorten url will be valid (min: 3600 [one hour] - max: 2592000 [30 days]). Default value 2592000 |
| `flow[].to.phone` | body | `string` | no | The recipient phone [must exist (NotBlank) if viber and sip are both null] |
| `flow[].to.sip` | body | `string` | no | A valid sip address. (ex 1111@test.com:55080) [must exist (NotBlank) if phone and viber are both null] |
| `flow[].to.viber` | body | `string` | no | A valid phone number. The recipient should have the Viber application installed to be able to receive a Viber call. [must exist (NotBlank) if phone and sip are both null] |
| `flow[].dialplan` | body | `object` | no | A combination of action verbs to be executed. Can not be empty. Check [here](/docs/dialplan-verbs) for possible "SAY" and "PLAY" avalues. |
| `flow[].machineDetection` | body | `object` | no | [For Voice only] It is used to detect if the call is answered by human or machine and define the desired actions (in case of machine). |
| `flow[].message.viberVideo` | body | `object` | no | Represents the Viber video of the Viber message. |
| `flow[].message.viberVideo.videoUrl` | body | `string` | yes | The Url where the video is hosted (1000 max chars, only https). |
| `flow[].message.viberVideo.videoThumbnail` | body | `string` | yes | The Url of a thumbnail for the video (1000 max chars, only https). |
| `flow[].message.viberVideo.fileSize` | body | `number` | yes | The file size in MB (positive number, 200 max). |
| `flow[].message.viberVideo.duration` | body | `number` | yes | The video’s duration in seconds (positive number, 600 max). |

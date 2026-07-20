# Update a scheduled bulk send out - campaign with Routee

Updates a scheduled bulk send out - campaign in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sms/:trackingId`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Update a scheduled bulk send out - campaign](https://docs.routee.net/reference/update-a-scheduled-message-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignTrackingId` | path | `string` | yes | the campaign’s tracking id. |
| `trackingId` | path | `string` | yes | — |
| `contacts[]` | body | `array<string>` | no | The contact ids that the message will be sent to. Contacts have to be uploaded to the system. One of "groups", "to", "contacts" parameters is required. |
| `groups[]` | body | `array<string>` | no | The groups of contacts in the account selected as recipients. Groups have to be created at the system. One of "groups", "to", "contacts" parameters is required. |
| `to[]` | body | `array<string>` | no | The phone numbers (array) the message is about to be sent to. Format with a '+' and country code e.g., +306948530920 (E.164 format). Maximum array of number allowed 30k. One of "groups", "to", "contacts" parameters is required. |
| `from` | body | `string` | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length 11 characters). When you want to use a number, you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | body | `string` | yes | The message you want to send. Use "\n" to create a new line in your message. Use [~{labelName}] in order to send personalized messages, by using the labels of your contacts. |
| `scheduledDate` | body | `date` | no | Defines the scheduled date and time in UTC. (eg YYYY-MM-DDThh:mm:ssTZD where TZD is the time zone designator (Z or +hh:mm or -hh:mm)) |
| `campaignName` | body | `string` | no | The name of the campaign. If you want to be able to track the whole campaign from Routee web platform use a name, if no name is provided you won’t be able to see the campaign from Routee web platform but you can track all the individual messages. Must be between 2 and 30 characters and contain only latin letters, numbers, spaces and - |
| `flash` | body | `boolean` | no | Indicates if the SMS is a flash SMS. A flash SMS is a type of SMS that appears directly on the main screen without user interaction and is not automatically stored in the inbox. It can be useful in emergencies, such as a fire alarm or cases of confidentiality, as in delivering one-time passwords. Default value false |
| `respectQuietHours` | body | `boolean` | no | Indicates if the SMS should respect the quiet hours. Quiet Hours are set by default to 23.00 - 08.00 and 14.00-17.00 destination local time. Please note that not all countries are supported with this feature due to multiple time zones within the country. Default value false |
| `campaignCallback` | body | `object` | no | Defines the notification callback information for the progress of the SMS campaign. Check [here](/docs/callbacks) for the payload information |
| `callback` | body | `object` | no | Defines the notification callback information for an individual message progress of the SMS campaign. Check [here](/docs/callbacks) for the payload information |
| `reminder` | body | `object` | no | Defines the recipients that will receive a test SMS before the actual SMS campaign is sent. |
| `fallbackValues[]` | body | `array<string>` | no | Defines the default values when the SMS has labels, in case a contact does not contain any of these labels. |
| `transcode` | body | `boolean` | no | If “transcode” is set to true/false, then the message body will be/not be transcoded. If the “transcode” parameter is not set, then the application level setting will be used. In case the message can be sent as UTF in one part, it will not be transcoded. |

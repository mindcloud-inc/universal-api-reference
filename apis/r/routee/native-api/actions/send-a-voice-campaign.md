# Send a Voice Campaign with Routee

Sends a voice campaign with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice/campaign`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send a Voice Campaign](https://docs.routee.net/reference/send-a-voice-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The sender id for this call. The sender id can be a telephone number or an alphanumeric string. NOTICE: Alphanumeric sender is not supported by all networks (e.g. Greek networks). Check restrictions and features here: https://go.routee.net/#/management/restrictions-and-features |
| `to[]` | body | `array<string>` | no | The recipients of this call, must be a list with valid numbers (mobiles or landlines). Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `contacts[]` | body | `array<string>` | no | The contacts of this call, must be a list with valid contact ids. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `groups[]` | body | `array<string>` | no | The lists of this call, must be a list with valid group names. Max length: 1000. One of "groups", "to", "contacts" parameters are required. |
| `name` | body | `string` | no | The name of the voice campaign. The name of the campaign. If you want to be able to track the whole campaign from Routee web platform use a name. Must be between 2 and 30 characters and contain only latin letters, numbers, spaces and - |
| `fileURL` | body | `string` | no | The url of the wav file to play. One of fileURL or message parameters is required. |
| `message` | body | `object` | no | Represents the text message to be converted to speech. One of fileURL or message parameters is required. |
| `message.gender` | body | `string` | no | The gender of the voice message to be played. Check [here](/docs/text-to-speech) for possible values |
| `message.language` | body | `string` | no | The language of the voice message to be played. Check [here](/docs/text-to-speech) for possible values |
| `message.text` | body | `string` | no | The text of the voice message to be played |
| `respectQuietHours` | body | `boolean` | no | Indicates if the call should respect the quiet hours, default value: false. |
| `ignoreDnd` | body | `boolean` | no | Use this option when sending transactional messages. By enabling this option, Routee will ignore any Do Not Disturb list and will send the campaign to all the recipients you have provided. This option may violate user privacy. |
| `scheduledDate` | body | `date` | no | The date and time (in UTC), that the call campaign will be executed at. (eg YYYY-MM-DDThh:mm:ssTZD where TZD is the time zone designator (Z or +hh:mm or -hh:mm)) |
| `hangupDelay` | body | `number` | no | The time to wait for the call to be answered |
| `campaignCallback` | body | `object` | no | Information about a DLR callback for the progress of the Voice campaign. |
| `callback` | body | `object` | no | Defines the notification callback information for an individual message progress of the Voice campaign |
| `collectDtmfDigits` | body | `boolean` | no | Indicates if the voice campaign should collect DTMF digits at the end of the voice message. |
| `collectDtmfAwaitSeconds` | body | `number` | no | If you enable the collectDtmfDigits you can set the duration of the pause that will be added at the end of the voice message. |

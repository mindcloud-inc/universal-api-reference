# Send an SMS with Routee

Sends an SMS message with Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Send an SMS](https://docs.routee.net/reference/send-single-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The sender of the message. This can be a telephone number (numeric string with maximum length 16 characters) or an alphanumeric string (maximum length of 11 characters). When you want to use a [number](/docs/numbers), you have to enter it without the '+' before the country code (eg 447123123456). |
| `body` | body | `string` | yes | The message you want to send. Use "\n" to create a new line in your message. |
| `to` | body | `string` | yes | The destination phone number. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `flash` | body | `boolean` | no | Indicates if the SMS is a flash SMS. A flash SMS is a type of SMS that appears directly on the main screen without user interaction and is not automatically stored in the inbox. It can be useful in emergencies, such as a fire alarm or cases of confidentiality, as in delivering one-time passwords. Default value false. |
| `label` | body | `string` | no | A generic label which can be used for tagging the SMS. The maximum length is 350 characters. |
| `callback` | body | `object` | no | Defines the callback information for an individual message. Check [here](/docs/callbacks) for payload information. You can also set this value from Routee [Platform](https://go.routee.net/#/management/applications) on the Applications menu. |
| `ttl` | body | `number` | no | The duration in minutes the delivery of an SMS will be attempted. Must be between 1-4320. By default Routee will attempt delivery for 72 hours. If the SMS is not delivered within the validity period, then the SMS status will be "Undelivered", with "detailedStatus": "Expired". |
| `transcode` | body | `boolean` | no | If “transcode” is set to true/false, then the message body will be/not be transcoded. If the “transcode” parameter is not set, then the application level setting will be used. In case the message can be sent as UTF in one part, it will not be transcoded. |
| `urlShortener` | body | `object` | no | [OPTIONAL] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination. |
| `restrictions` | body | `object` | no | [OPTIONAL] Provide the registered Content Template ID and Principal Entity ID to ensure the message is not rejected by TRAI regulations. |

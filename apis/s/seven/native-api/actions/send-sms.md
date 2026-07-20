# Send SMS with Seven

Creates a new SMS in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Send SMS](https://docs.seven.io/en/rest-api/endpoints/sms#send-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient number of the SMS. This can also be the name of a contact or a group. Our API accepts all common formats such as 0049171999999999 , 49171999999999 , +49171999999999 . Multiple recipients are transferred comma-separated. Ideally, you should enter the phone number in international format after  E.164 . |
| `text` | body | `string` | yes | Text of the SMS message. |
| `from` | body | `string` | no | Sender of the SMS. This may contain a maximum of 11 alphanumeric or 16 numeric characters. |
| `delay` | body | `date` | no | Date/time for delayed sending. Optionally Unix timestamp or a timestamp in the format YYYY-MM-DD hh:mm:ss. |
| `flash` | body | `boolean` | no | Send SMS as Flash SMS. These are shown directly on the recipient&#x27;s display. On most devices, no sender is displayed for Flash SMS, with the exception of some older models. |
| `udh` | body | `string` | no | Individual User Data Header (UDH) of the SMS. If specified and variable text contains hex code, the message is sent as an 8-bit binary SMS. 050003CC0201 (concatenated message: reference number 204, part 1 of 2) |
| `ttl` | body | `number` | no | Specifies the validity period of the SMS in minutes. The default is 2880, i.e. 48 hours. Please note that not all networks allow a different setting. |
| `label` | body | `string` | no | Optionally set a separate label for each SMS so that you can assign it to your statistics. Max. 100 characters, permitted characters: a-z, A-Z, 0-9, .-_@. |
| `performance_tracking` | body | `boolean` | no | Activate click and performance tracking for URLs found in the SMS text. This also activates the URL shortener. |
| `foreign_id` | body | `string` | no | Enter your own ID for this message. You will receive the foreign_id in turn for callbacks for status reports etc. Max. 64 characters, permitted characters: a-z, A-Z, 0-9, .-_@. |
| `is_binary` | body | `boolean` | no | If true , the SMS will be sent as binary data. |
| `get_replies` | body | `boolean` | no | Activates the reply function. Replies are assigned for 48 hours. The sender is automatically overwritten. |
| `unicode` | body | `string` | no | — |
| `utf8` | body | `string` | no | — |
| `return_msg_id` | body | `string` | no | — |
| `details` | body | `string` | no | — |
| `json` | body | `string` | no | — |
| `no_reload` | body | `string` | no | — |

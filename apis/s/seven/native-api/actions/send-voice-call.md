# Send Voice Call with Seven

Creates a new voice call in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/voice`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Send Voice Call](https://docs.seven.io/en/rest-api/endpoints/voice#send-voice-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `to` | body | `string` | yes | Recipient number(s) of the voice calls. This can also be the name of a contact or a group. Our API accepts all common formats like 0049171123456789 , 49171123456789 , +49171123456789 . Multiple recipients are passed separated by commas. Ideally, you should provide the phone number in the international format according to  E.164 . |
| `text` | body | `string` | yes | Text message to be read out. Optionally as simple text or as SSML . |
| `from` | body | `string` | no | Caller ID of the call. Please only use verified sender IDs or one of your numbers booked with us here. |
| `ringtime` | body | `number` | no | The duration of how long it should ring at the recipient&#x27;s end before hanging up. Here, 5 to 60 seconds are possible. |
| `foreign_id` | body | `string` | no | A unique ID that you can use for later assignment of the call. This ID is passed in the webhook events. |
| `xml` | body | `string` | no | — |

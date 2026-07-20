# Send 2FA PIN Code Over SMS with Infobip

## Endpoint

- **Method:** `POST`
- **Path:** `/2fa/2/pin`
- **Base URL:** `https://rkpzwe.api.infobip.com`
- **Official documentation:** [Send 2FA PIN Code Over SMS](https://www.infobip.com/docs/api/platform/2fa/pin-sending-and-verification/send-2fa-pin-code-over-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ncNeeded` | query | `boolean` | no | Indicates if [Number Lookup](https://www.infobip.com/docs/api/connectivity/number-lookup) is needed before sending the 2FA message. If the parameter value is true, Number Lookup will be requested before sending the SMS. If the value is false, the SMS will be sent without requesting Number Lookup. Field's default value is `true`. |
| `applicationId` | body | `string` | yes | The ID of the application that represents your service, e.g. 2FA for login, 2FA for changing the password, etc. |
| `from` | body | `string` | no | Use this parameter if you wish to override the sender ID from the [created](#channels/sms/create-2fa-message-template) message template parameter `senderId`. |
| `messageId` | body | `string` | yes | The ID of the message template (message body with the PIN placeholder) that is sent to the recipient. |
| `placeholders` | body | `object` | no | Key value pairs that will be replaced during message sending. Placeholder keys should NOT contain curly brackets and should NOT contain a `pin` placeholder. Valid example: `"placeholders":{"firstName":"John"}` |
| `to` | body | `string` | yes | Phone number to which the 2FA message will be sent. Example: 41793026727. |
| `trackDelivery` | body | `boolean` | no | Enables sending of delivery reports via [Subscriptions](https://www.infobip.com/docs/cpaas-x/subscriptions-management). The [retry cycle](https://www.infobip.com/docs/sms/sms-over-api#push-retry-cycle-notify-url) for when your URL becomes unavailable uses the following formula: `1min + (1min * retryNumber * retryNumber)`. |

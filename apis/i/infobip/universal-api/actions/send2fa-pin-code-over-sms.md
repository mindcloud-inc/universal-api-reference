# Infobip: Send 2FA PIN Code Over SMS



```
POST https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send2fa-pin-code-over-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send2fa-pin-code-over-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "applicationId": "string",
  "messageId": "string",
  "to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/send2fa-pin-code-over-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "applicationId": "string",
    "messageId": "string",
    "to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ncNeeded` | boolean | no | Indicates if [Number Lookup](https://www.infobip.com/docs/api/connectivity/number-lookup) is needed before sending the 2FA message. If the parameter value is true, Number Lookup will be requested before sending the SMS. If the value is false, the SMS will be sent without requesting Number Lookup. Field's default value is `true`. |
| `applicationId` | string | yes | The ID of the application that represents your service, e.g. 2FA for login, 2FA for changing the password, etc. |
| `from` | string | no | Use this parameter if you wish to override the sender ID from the [created](#channels/sms/create-2fa-message-template) message template parameter `senderId`. |
| `messageId` | string | yes | The ID of the message template (message body with the PIN placeholder) that is sent to the recipient. |
| `placeholders` | object | no | Key value pairs that will be replaced during message sending. Placeholder keys should NOT contain curly brackets and should NOT contain a `pin` placeholder. Valid example: `"placeholders":{"firstName":"John"}` |
| `to` | string | yes | Phone number to which the 2FA message will be sent. Example: 41793026727. |
| `trackDelivery` | boolean | no | Enables sending of delivery reports via [Subscriptions](https://www.infobip.com/docs/cpaas-x/subscriptions-management). The [retry cycle](https://www.infobip.com/docs/sms/sms-over-api#push-retry-cycle-notify-url) for when your URL becomes unavailable uses the following formula: `1min + (1min * retryNumber * retryNumber)`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callStatus": "string",
      "externalMessageId": "string",
      "ncStatus": "string",
      "pinId": "string",
      "smsStatus": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callStatus` | string |  |
| `externalMessageId` | string |  |
| `ncStatus` | string |  |
| `pinId` | string |  |
| `smsStatus` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /2fa/2/pin` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send2fa-pin-code-over-sms.md) for the provider-specific parameters and requirements.


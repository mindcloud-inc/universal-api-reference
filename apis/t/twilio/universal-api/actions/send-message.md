# Twilio: Send Message

Sends a new message with Twilio.

```
POST https://connect.mindcloud.co/v1/universal/twilio/latest/actions/send-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/send-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "to": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twilio/latest/actions/send-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "to": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | yes | Recipient phone number in E.164 format. |
| `body` | string | yes | SMS text content. |
| `from` | string | no | Optional sender phone number or sender address. Uses the connection default when configured. Default: `{{credentials.twilioPhoneNumber}}`. |
| `messagingServiceSid` | string | no | Optional Twilio Messaging Service SID. Leave blank unless this workflow uses a Messaging Service. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statusCallback` | string | no | Optional URL to receive Twilio message status callbacks. |
| `validityPeriod` | number | no | Optional maximum queue time in seconds (1-36000). |
| `smartEncoded` | boolean | no | Replace supported Unicode characters with GSM-7 equivalents when enabled. |
| `provideFeedback` | boolean | no | Indicate that this workflow will provide delivery feedback to Twilio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountSid": "string",
      "apiVersion": "string",
      "body": "string",
      "dateCreated": "string",
      "dateSent": "string",
      "dateUpdated": "string",
      "direction": "string",
      "errorCode": 1,
      "errorMessage": "string",
      "from": "string",
      "messagingServiceSid": "string",
      "numMedia": "string",
      "numSegments": "string",
      "price": "string",
      "priceUnit": "string",
      "sid": "string",
      "status": "string",
      "subresourceUris": {},
      "to": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountSid` | string | Twilio account SID associated with the message. |
| `apiVersion` | string | Twilio API version used to process the message. |
| `body` | string | Message text content. |
| `dateCreated` | string | Timestamp when the message was created. |
| `dateSent` | string | Timestamp when the message was sent or received. |
| `dateUpdated` | string | Timestamp when the message was last updated. |
| `direction` | string | Message direction. |
| `errorCode` | number | Twilio error code when delivery fails. |
| `errorMessage` | string | Twilio error description when delivery fails. |
| `from` | string | Sender phone number or sender address. |
| `messagingServiceSid` | string | Twilio Messaging Service SID, when used. |
| `numMedia` | string | Number of media attachments. |
| `numSegments` | string | Number of SMS segments. |
| `price` | string | Message price, when available. |
| `priceUnit` | string | Currency for the message price. |
| `sid` | string | Twilio Message SID. |
| `status` | string | Current message delivery status. |
| `subresourceUris` | object | URIs for related Twilio message resources. |
| `to` | string | Recipient phone number or channel address. |
| `uri` | string | Twilio message resource URI. |

## Native endpoint

Through the native Twilio API, this operation is `POST /Accounts/:AccountSid/Messages.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.


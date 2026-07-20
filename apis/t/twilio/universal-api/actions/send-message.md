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
| `to` | string | yes |  |
| `body` | string | yes |  |
| `from` | string | no | Default: `{{credentials.twilioPhoneNumber}}`. |
| `messagingServiceSid` | string | no | Default: `{{credentials.twilioMessagingServiceSid}}`. |

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
      "subresourceUris": {
        "feedback": "string",
        "media": "string"
      },
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
| `accountSid` | string |  |
| `apiVersion` | string |  |
| `body` | string |  |
| `dateCreated` | string |  |
| `dateSent` | string |  |
| `dateUpdated` | string |  |
| `direction` | string |  |
| `errorCode` | number |  |
| `errorMessage` | string |  |
| `from` | string |  |
| `messagingServiceSid` | string |  |
| `numMedia` | string |  |
| `numSegments` | string |  |
| `price` | string |  |
| `priceUnit` | string |  |
| `sid` | string |  |
| `status` | string |  |
| `subresourceUris.feedback` | string |  |
| `subresourceUris.media` | string |  |
| `to` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `POST /Accounts/:AccountSid/Messages.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-message.md) for the provider-specific parameters and requirements.


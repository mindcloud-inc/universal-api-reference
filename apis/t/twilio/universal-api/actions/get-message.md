# Twilio: Get Message

Retrieves a message from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-message?connectionId=$CONNECTION_ID&messageSid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageSid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-message?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageSid` | string | yes | Twilio Message SID to retrieve. |

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

Through the native Twilio API, this operation is `GET /Accounts/:AccountSid/Messages/:MessageSid.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.


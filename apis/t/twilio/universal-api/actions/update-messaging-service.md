# Twilio: Update Messaging Service

Updates an existing messaging service in Twilio.

```
PUT https://connect.mindcloud.co/v1/universal/twilio/latest/actions/update-messaging-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/update-messaging-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sid": "string",
  "friendlyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twilio/latest/actions/update-messaging-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sid": "string",
    "friendlyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sid` | string | yes | Messaging Service SID to update |
| `friendlyName` | string | yes | Updated friendly name for the messaging service |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountSid": "string",
      "areaCodeGeomatch": true,
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "dateUpdated": "2026-05-07T12:00:00.000Z",
      "fallbackMethod": "string",
      "fallbackToLongCode": true,
      "fallbackUrl": "https://example.com",
      "friendlyName": "Ava Chen",
      "inboundMethod": "string",
      "inboundRequestUrl": "https://example.com",
      "links": {
        "alphaSenders": "https://example.com",
        "channelSenders": "https://example.com",
        "destinationAlphaSenders": "https://example.com",
        "messages": "https://example.com",
        "phoneNumbers": "https://example.com",
        "shortCodes": "https://example.com",
        "usAppToPerson": "https://example.com",
        "usAppToPersonUsecases": "https://example.com"
      },
      "mmsConverter": true,
      "scanMessageContent": "string",
      "sid": "string",
      "smartEncoding": true,
      "statusCallback": "string",
      "stickySender": true,
      "synchronousValidation": true,
      "url": "https://example.com",
      "usAppToPersonRegistered": true,
      "usecase": "string",
      "useInboundWebhookOnNumber": true,
      "validityPeriod": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountSid` | string |  |
| `areaCodeGeomatch` | boolean |  |
| `dateCreated` | date |  |
| `dateUpdated` | date |  |
| `fallbackMethod` | string |  |
| `fallbackToLongCode` | boolean |  |
| `fallbackUrl` | string |  |
| `friendlyName` | string |  |
| `inboundMethod` | string |  |
| `inboundRequestUrl` | string |  |
| `links.alphaSenders` | string |  |
| `links.channelSenders` | string |  |
| `links.destinationAlphaSenders` | string |  |
| `links.messages` | string |  |
| `links.phoneNumbers` | string |  |
| `links.shortCodes` | string |  |
| `links.usAppToPerson` | string |  |
| `links.usAppToPersonUsecases` | string |  |
| `mmsConverter` | boolean |  |
| `scanMessageContent` | string |  |
| `sid` | string |  |
| `smartEncoding` | boolean |  |
| `statusCallback` | string |  |
| `stickySender` | boolean |  |
| `synchronousValidation` | boolean |  |
| `url` | string |  |
| `usAppToPersonRegistered` | boolean |  |
| `usecase` | string |  |
| `useInboundWebhookOnNumber` | boolean |  |
| `validityPeriod` | number |  |

## Native endpoint

Through the native Twilio API, this operation is `POST https://messaging.twilio.com/v1/Services/:Sid` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-messaging-service.md) for the provider-specific parameters and requirements.


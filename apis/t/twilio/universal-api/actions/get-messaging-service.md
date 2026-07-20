# Twilio: Get Messaging Service

Retrieves a messaging service from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-messaging-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-messaging-service?connectionId=$CONNECTION_ID&sid=%7B%7Bcredentials.twilioMessagingServiceSid%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sid": "{{credentials.twilioMessagingServiceSid}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/get-messaging-service?${params}`, {
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
| `sid` | string | yes | Default: `{{credentials.twilioMessagingServiceSid}}`. |

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

Through the native Twilio API, this operation is `GET https://messaging.twilio.com/v1/Services/:Sid` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-messaging-service.md) for the provider-specific parameters and requirements.


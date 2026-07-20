# Twilio: List Messaging Services

Retrieves messaging services from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-services?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "firstPageUrl": "https://example.com",
        "key": "string",
        "nextPageUrl": "https://example.com",
        "page": 1,
        "pageSize": 1,
        "previousPageUrl": "https://example.com",
        "url": "https://example.com"
      },
      "services": [
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.firstPageUrl` | string |  |
| `meta.key` | string |  |
| `meta.nextPageUrl` | string |  |
| `meta.page` | number |  |
| `meta.pageSize` | number |  |
| `meta.previousPageUrl` | string |  |
| `meta.url` | string |  |
| `services[].accountSid` | string |  |
| `services[].areaCodeGeomatch` | boolean |  |
| `services[].dateCreated` | date |  |
| `services[].dateUpdated` | date |  |
| `services[].fallbackMethod` | string |  |
| `services[].fallbackToLongCode` | boolean |  |
| `services[].fallbackUrl` | string |  |
| `services[].friendlyName` | string |  |
| `services[].inboundMethod` | string |  |
| `services[].inboundRequestUrl` | string |  |
| `services[].links.alphaSenders` | string |  |
| `services[].links.channelSenders` | string |  |
| `services[].links.destinationAlphaSenders` | string |  |
| `services[].links.messages` | string |  |
| `services[].links.phoneNumbers` | string |  |
| `services[].links.shortCodes` | string |  |
| `services[].links.usAppToPerson` | string |  |
| `services[].links.usAppToPersonUsecases` | string |  |
| `services[].mmsConverter` | boolean |  |
| `services[].scanMessageContent` | string |  |
| `services[].sid` | string |  |
| `services[].smartEncoding` | boolean |  |
| `services[].statusCallback` | string |  |
| `services[].stickySender` | boolean |  |
| `services[].synchronousValidation` | boolean |  |
| `services[].url` | string |  |
| `services[].usAppToPersonRegistered` | boolean |  |
| `services[].usecase` | string |  |
| `services[].useInboundWebhookOnNumber` | boolean |  |
| `services[].validityPeriod` | number |  |

## Native endpoint

Through the native Twilio API, this operation is `GET https://messaging.twilio.com/v1/Services` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messaging-services.md) for the provider-specific parameters and requirements.


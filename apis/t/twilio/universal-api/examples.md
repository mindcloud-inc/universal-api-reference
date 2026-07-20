# Twilio Universal API Examples

These examples use the MindCloud API key and Twilio connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Messages

Retrieves messages from Twilio.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messages?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "end": 1,
      "firstPageUri": "string",
      "messages": [
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
      "nextPageUri": "string",
      "page": 1,
      "pageSize": 1,
      "previousPageUri": "string",
      "start": 1,
      "uri": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Messages action reference](actions/list-messages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twilio/latest/actions/list-messages).

## Create Messaging Service

Creates a new messaging service in Twilio.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/create-messaging-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "friendlyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/twilio/latest/actions/create-messaging-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "friendlyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Messaging Service action reference](actions/create-messaging-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/twilio/latest/actions/create-messaging-service).

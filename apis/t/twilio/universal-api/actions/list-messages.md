# Twilio: List Messages

Retrieves messages from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

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

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `to` | string | no |  |
| `from` | string | no |  |
| `dateSent` | date | no |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | number |  |
| `firstPageUri` | string |  |
| `messages[].accountSid` | string |  |
| `messages[].apiVersion` | string |  |
| `messages[].body` | string |  |
| `messages[].dateCreated` | string |  |
| `messages[].dateSent` | string |  |
| `messages[].dateUpdated` | string |  |
| `messages[].direction` | string |  |
| `messages[].errorCode` | number |  |
| `messages[].errorMessage` | string |  |
| `messages[].from` | string |  |
| `messages[].messagingServiceSid` | string |  |
| `messages[].numMedia` | string |  |
| `messages[].numSegments` | string |  |
| `messages[].price` | string |  |
| `messages[].priceUnit` | string |  |
| `messages[].sid` | string |  |
| `messages[].status` | string |  |
| `messages[].subresourceUris.feedback` | string |  |
| `messages[].subresourceUris.media` | string |  |
| `messages[].to` | string |  |
| `messages[].uri` | string |  |
| `nextPageUri` | string |  |
| `page` | number |  |
| `pageSize` | number |  |
| `previousPageUri` | string |  |
| `start` | number |  |
| `uri` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET /Accounts/:AccountSid/Messages.json` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messages.md) for the provider-specific parameters and requirements.


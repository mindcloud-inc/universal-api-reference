# smsmode: Get RCS Message



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-rcs-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-rcs-message?connectionId=$CONNECTION_ID&channelId=string&campaignId=string&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "channelId": "string",
  "campaignId": "string",
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/get-rcs-message?${params}`, {
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
| `channelId` | string | yes | Channel ID path parameter from the smsmode API route. |
| `campaignId` | string | yes | Campaign ID path parameter from the smsmode API route. |
| `messageId` | string | yes | Message ID path parameter from the smsmode API route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedAt": "2026-05-07T12:00:00.000Z",
      "body": {
        "type": "string"
      },
      "callbackUrlMo": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "channel": {
        "channelId": "string",
        "flow": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "direction": "string",
      "from": "string",
      "href": "string",
      "messageId": "string",
      "originMessageId": "string",
      "price": {
        "amount": 1,
        "currency": "string"
      },
      "recipient": {
        "to": "string"
      },
      "refClient": "string",
      "sentDate": "2026-05-07T12:00:00.000Z",
      "status": {
        "deliveryDate": "2026-05-07T12:00:00.000Z",
        "detail": "string",
        "value": "string"
      },
      "type": "string",
      "validity": {
        "amount": 1,
        "timeUnit": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedAt` | date |  |
| `body.type` | string |  |
| `callbackUrlMo` | string |  |
| `callbackUrlStatus` | string |  |
| `channel.channelId` | string |  |
| `channel.flow` | string |  |
| `channel.name` | string |  |
| `channel.type` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `href` | string |  |
| `messageId` | string |  |
| `originMessageId` | string |  |
| `price.amount` | number |  |
| `price.currency` | string |  |
| `recipient.to` | string |  |
| `refClient` | string |  |
| `sentDate` | date |  |
| `status.deliveryDate` | date |  |
| `status.detail` | string |  |
| `status.value` | string |  |
| `type` | string |  |
| `validity.amount` | number |  |
| `validity.timeUnit` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET rcs/v1/channels/:channelId/campaigns/:campaignId/messages/:messageId` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-rcs-message.md) for the provider-specific parameters and requirements.


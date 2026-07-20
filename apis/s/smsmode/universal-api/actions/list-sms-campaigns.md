# smsmode: List SMS Campaigns



```
GET https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-sms-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a smsmode `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-sms-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0&channelId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "channelId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-sms-campaigns?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedAt": "2026-05-07T12:00:00.000Z",
      "body": {
        "encoding": "string",
        "length": 1,
        "messagePartCount": 1,
        "stop": true,
        "text": "string"
      },
      "callbackUrlMo": "https://example.com",
      "callbackUrlStatus": "https://example.com",
      "campaignId": "string",
      "channel": {
        "channelId": "string",
        "flow": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "endDate": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "href": "string",
      "price": {
        "amount": 1,
        "currency": "string"
      },
      "quantity": 1,
      "recipients": [
        {
          "refClient": "string",
          "to": "string"
        }
      ],
      "refClient": "string",
      "sentDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "statuses": [
        {
          "quantity": 1,
          "value": "string"
        }
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedAt` | date |  |
| `body.encoding` | string |  |
| `body.length` | number |  |
| `body.messagePartCount` | number |  |
| `body.stop` | boolean |  |
| `body.text` | string |  |
| `callbackUrlMo` | string |  |
| `callbackUrlStatus` | string |  |
| `campaignId` | string |  |
| `channel.channelId` | string |  |
| `channel.flow` | string |  |
| `channel.name` | string |  |
| `channel.type` | string |  |
| `endDate` | date |  |
| `from` | string |  |
| `href` | string |  |
| `price.amount` | number |  |
| `price.currency` | string |  |
| `quantity` | number |  |
| `recipients[].refClient` | string |  |
| `recipients[].to` | string |  |
| `refClient` | string |  |
| `sentDate` | date |  |
| `status` | string |  |
| `statuses[].quantity` | number |  |
| `statuses[].value` | string |  |
| `type` | string |  |

## Native endpoint

Through the native smsmode API, this operation is `GET sms/v1/channels/:channelId/campaigns` (base URL `https://rest.smsmode.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sms-campaigns.md) for the provider-specific parameters and requirements.


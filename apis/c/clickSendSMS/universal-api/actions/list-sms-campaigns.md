# ClickSend SMS: List SMS Campaigns

Retrieves SMS campaigns from ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/list-sms-campaigns?${params}`, {
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
| `page` | number | no |  |
| `limit` | number | no |  |
| `q` | string | no |  |
| `order_by` | string | no |  |
| `date_from` | number | no |  |
| `date_to` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "data": [
        {
          "body": "string",
          "customString": {},
          "dateAdded": 1,
          "from": "string",
          "listId": 1,
          "listName": "Ava Chen",
          "name": "Ava Chen",
          "schedule": 1,
          "senders": [
            {
              "recipientCountryCode": "string",
              "senderCountryCode": "string",
              "senderId": "string",
              "senderType": "string"
            }
          ],
          "smsCampaignId": 1,
          "source": {},
          "status": "string",
          "subaccountId": 1,
          "totalCount": 1,
          "unsubscribeLink": 1,
          "urlToShorten": {},
          "userId": 1
        }
      ],
      "from": 1,
      "lastPage": 1,
      "nextPageUrl": {},
      "perPage": 1,
      "prevPageUrl": {},
      "to": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `data[].body` | string |  |
| `data[].customString` | object |  |
| `data[].dateAdded` | number |  |
| `data[].from` | string |  |
| `data[].listId` | number |  |
| `data[].listName` | string |  |
| `data[].name` | string |  |
| `data[].schedule` | number |  |
| `data[].senders[].recipientCountryCode` | string |  |
| `data[].senders[].senderCountryCode` | string |  |
| `data[].senders[].senderId` | string |  |
| `data[].senders[].senderType` | string |  |
| `data[].smsCampaignId` | number |  |
| `data[].source` | object |  |
| `data[].status` | string |  |
| `data[].subaccountId` | number |  |
| `data[].totalCount` | number |  |
| `data[].unsubscribeLink` | number |  |
| `data[].urlToShorten` | object |  |
| `data[].userId` | number |  |
| `from` | number |  |
| `lastPage` | number |  |
| `nextPageUrl` | object |  |
| `perPage` | number |  |
| `prevPageUrl` | object |  |
| `to` | number |  |
| `total` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `GET /v3/sms-campaigns` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sms-campaigns.md) for the provider-specific parameters and requirements.


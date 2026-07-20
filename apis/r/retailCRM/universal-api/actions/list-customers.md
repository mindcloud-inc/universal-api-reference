# retailCRM: List Customers

Retrieves customers from retailCRM.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/list-customers?${params}`, {
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
      "averageSumm": 1,
      "bad": true,
      "contragent": {
        "contragentType": "string"
      },
      "createdAt": "string",
      "customerSubscriptions": [
        {
          "subscribed": true,
          "subscription": {
            "active": true,
            "autoSubscribe": true,
            "channel": "string",
            "code": "string",
            "id": 1,
            "name": "Ava Chen",
            "ordering": 1
          }
        }
      ],
      "customFields": [
        "string"
      ],
      "firstName": "Ava",
      "id": 1,
      "isContact": true,
      "lastName": "Chen",
      "managerId": 1,
      "marginSumm": 1,
      "mgCustomers": [
        "string"
      ],
      "ordersCount": 1,
      "personalDiscount": 1,
      "phones": [
        {
          "number": "string"
        }
      ],
      "segments": [
        "string"
      ],
      "site": "string",
      "tags": [
        "string"
      ],
      "totalSumm": 1,
      "type": "string",
      "vip": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageSumm` | number |  |
| `bad` | boolean |  |
| `contragent.contragentType` | string |  |
| `createdAt` | string |  |
| `customerSubscriptions[].subscribed` | boolean |  |
| `customerSubscriptions[].subscription.active` | boolean |  |
| `customerSubscriptions[].subscription.autoSubscribe` | boolean |  |
| `customerSubscriptions[].subscription.channel` | string |  |
| `customerSubscriptions[].subscription.code` | string |  |
| `customerSubscriptions[].subscription.id` | number |  |
| `customerSubscriptions[].subscription.name` | string |  |
| `customerSubscriptions[].subscription.ordering` | number |  |
| `customFields` | array |  |
| `firstName` | string |  |
| `id` | number |  |
| `isContact` | boolean |  |
| `lastName` | string |  |
| `managerId` | number |  |
| `marginSumm` | number |  |
| `mgCustomers` | array |  |
| `ordersCount` | number |  |
| `personalDiscount` | number |  |
| `phones[].number` | string |  |
| `segments` | array |  |
| `site` | string |  |
| `tags` | array |  |
| `totalSumm` | number |  |
| `type` | string |  |
| `vip` | boolean |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /customers` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.


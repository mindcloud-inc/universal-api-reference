# GoTeamup: List Orders

Finds orders in GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/list-orders?${params}`, {
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
      "count": 1,
      "next": {},
      "previous": {},
      "results": [
        {
          "cartUuid": "string",
          "comments": "string",
          "completedAt": {},
          "createdAt": "string",
          "customer": 1,
          "id": 1,
          "isDelivered": true,
          "isPaymentConfirmed": true,
          "items": "string",
          "itemsCount": {},
          "lockedAt": {},
          "modifiedAt": "string",
          "number": "string",
          "object": "string",
          "paymentConfirmedAt": {},
          "status": "string",
          "totalPrice": {
            "currencySymbol": "string",
            "currencySymbolPosition": "string",
            "decimal": 1,
            "isoCurrencyCode": "string",
            "string": "string"
          },
          "totalPriceForDisplay": {
            "currencySymbol": "string",
            "currencySymbolPosition": "string",
            "decimal": 1,
            "isoCurrencyCode": "string",
            "string": "string"
          }
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
| `count` | number |  |
| `next` | object |  |
| `previous` | object |  |
| `results[].cartUuid` | string |  |
| `results[].comments` | string |  |
| `results[].completedAt` | object |  |
| `results[].createdAt` | string |  |
| `results[].customer` | number |  |
| `results[].id` | number |  |
| `results[].isDelivered` | boolean |  |
| `results[].isPaymentConfirmed` | boolean |  |
| `results[].items` | string |  |
| `results[].itemsCount` | object |  |
| `results[].lockedAt` | object |  |
| `results[].modifiedAt` | string |  |
| `results[].number` | string |  |
| `results[].object` | string |  |
| `results[].paymentConfirmedAt` | object |  |
| `results[].status` | string |  |
| `results[].totalPrice.currencySymbol` | string |  |
| `results[].totalPrice.currencySymbolPosition` | string |  |
| `results[].totalPrice.decimal` | number |  |
| `results[].totalPrice.isoCurrencyCode` | string |  |
| `results[].totalPrice.string` | string |  |
| `results[].totalPriceForDisplay.currencySymbol` | string |  |
| `results[].totalPriceForDisplay.currencySymbolPosition` | string |  |
| `results[].totalPriceForDisplay.decimal` | number |  |
| `results[].totalPriceForDisplay.isoCurrencyCode` | string |  |
| `results[].totalPriceForDisplay.string` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /store/orders` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.


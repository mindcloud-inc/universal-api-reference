# GoTeamup: Retrieve Order

Retrieves an order from GoTeamup.

```
GET https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/retrieve-order?${params}`, {
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
| `id` | number | yes | The TeamUp order ID |

## Response

```json
{
  "success": true,
  "data": [
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cartUuid` | string |  |
| `comments` | string |  |
| `completedAt` | object |  |
| `createdAt` | string |  |
| `customer` | number |  |
| `id` | number |  |
| `isDelivered` | boolean |  |
| `isPaymentConfirmed` | boolean |  |
| `items` | string |  |
| `itemsCount` | object |  |
| `lockedAt` | object |  |
| `modifiedAt` | string |  |
| `number` | string |  |
| `object` | string |  |
| `paymentConfirmedAt` | object |  |
| `status` | string |  |
| `totalPrice.currencySymbol` | string |  |
| `totalPrice.currencySymbolPosition` | string |  |
| `totalPrice.decimal` | number |  |
| `totalPrice.isoCurrencyCode` | string |  |
| `totalPrice.string` | string |  |
| `totalPriceForDisplay.currencySymbol` | string |  |
| `totalPriceForDisplay.currencySymbolPosition` | string |  |
| `totalPriceForDisplay.decimal` | number |  |
| `totalPriceForDisplay.isoCurrencyCode` | string |  |
| `totalPriceForDisplay.string` | string |  |

## Native endpoint

Through the native GoTeamup API, this operation is `GET /store/orders/:id` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-order.md) for the provider-specific parameters and requirements.


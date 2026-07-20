# GoTeamup: Create Order

Creates a new order in GoTeamup.

```
POST https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoTeamup `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goTeamup/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | number | yes | Customer ID |

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

Through the native GoTeamup API, this operation is `POST /store/orders` (base URL `https://goteamup.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.


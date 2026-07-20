# Amazon Seller: Get Order

Retrieves an order from Amazon Seller.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-v2026
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-v2026?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-v2026?${params}`, {
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
| `orderId` | string | yes | An Amazon-defined order identifier. |
| `includedData` | list<string> | no | Specify which datasets to include in the response. - BUYER Information about the buyer who purchased the order. - RECIPIENT Information about the recipient to whom the order is delivered. - PROCEEDS The revenue and financial breakdown for the order and order items. - EXPENSE The cost information applied to the order and order items. - PROMOTION The discount and promotional offer details applied to the order and order items. - CANCELLATION Cancellation information applied to the order and order items. - FULFILLMENT Information about how this order and order items are processed and shipped. - PACKAGES Shipping packages and tracking information. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "order": {
        "createdTime": "string",
        "lastUpdatedTime": "string",
        "orderId": "string",
        "orderItems": [
          {
            "orderItemId": "string",
            "product": {
              "asin": "string",
              "condition": {
                "conditionSubtype": "string",
                "conditionType": "string"
              },
              "price": {
                "unitPrice": {
                  "amount": "string",
                  "currencyCode": "string"
                }
              },
              "sellerSku": "string",
              "title": "string"
            },
            "quantityOrdered": 1
          }
        ],
        "programs": [
          "string"
        ],
        "salesChannel": {
          "channelName": "Ava Chen",
          "marketplaceId": "string",
          "marketplaceName": "Ava Chen"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `order.createdTime` | string |  |
| `order.lastUpdatedTime` | string |  |
| `order.orderId` | string |  |
| `order.orderItems[].orderItemId` | string |  |
| `order.orderItems[].product.asin` | string |  |
| `order.orderItems[].product.condition.conditionSubtype` | string |  |
| `order.orderItems[].product.condition.conditionType` | string |  |
| `order.orderItems[].product.price.unitPrice.amount` | string |  |
| `order.orderItems[].product.price.unitPrice.currencyCode` | string |  |
| `order.orderItems[].product.sellerSku` | string |  |
| `order.orderItems[].product.title` | string |  |
| `order.orderItems[].quantityOrdered` | number |  |
| `order.programs[]` | string |  |
| `order.salesChannel.channelName` | string |  |
| `order.salesChannel.marketplaceId` | string |  |
| `order.salesChannel.marketplaceName` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET orders/2026-01-01/orders/:orderId` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-v2026.md) for the provider-specific parameters and requirements.


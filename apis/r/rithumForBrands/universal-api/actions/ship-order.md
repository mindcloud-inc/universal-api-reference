# Rithum for Brands: Ship Order

Mark an entire order as shipped or partially shipped.

```
PUT https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/ship-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum for Brands `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/ship-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumForBrands/latest/actions/ship-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `items[].orderItemID` | string | no | When the Items array is included in this request, one of: OrderItemID or ProductID or Sku is required. |
| `orderId` | string | no |  |
| `shippedDateUtc` | string | no |  |
| `items[].productID` | string | no | Identifies the item by Product ID. (conditionally required) |
| `trackingNumber` | string | no |  |
| `items[].sku` | string | no | (conditionally required) Identifies the SKU (as defined by the seller). |
| `returnTrackingNumber` | string | no |  |
| `items[].quantity` | string | no | Required if the Items array is included in this request. |
| `shippingCarrier` | string | no |  |
| `items[].sellerFulfillmentItemID` | string | no | (optional) Identifier provided by the seller. Usually a serial number or batch number. |
| `shippingClass` | string | no |  |
| `deliveryStatus` | string | no | Complete is the most common status used. See all here: https://knowledge.channeladvisor.com/kc?id=kb_article_view&sys_id=c568b05533206e10ae51a5373e5c7b0e&spa=1#concept-89__section-3115 |
| `trackingUrl` | string | no |  |
| `distributionCenterID` | number | no |  |
| `items[]` | array<object> | no | (optional) A list of items to mark as shipped for this order. Leaving this array empty will mark the entire order as shipped. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rithum for Brands API returns.

## Native endpoint

Through the native Rithum for Brands API, this operation is `POST Orders(:orderId)/Ship` (base URL `https://api.channeladvisor.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ship-order.md) for the provider-specific parameters and requirements.


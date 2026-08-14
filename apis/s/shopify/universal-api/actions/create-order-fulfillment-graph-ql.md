# Shopify: Create Order Fulfillment



```
POST https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-order-fulfillment-graph-ql
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-order-fulfillment-graph-ql" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "variables.fulfillment.lineItemsByFulfillmentOrder[]": [
    {}
  ],
  "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderId": "gid://shopify/FulfillmentOrder/10079785100",
  "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[]": [
    {}
  ],
  "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].id": "gid://shopify/FulfillmentOrderLineItem/123456789",
  "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].quantity": "1",
  "variables.fulfillment.trackingInfo.number": "1Z999AA10123456784"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopify/latest/actions/create-order-fulfillment-graph-ql', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "variables.fulfillment.lineItemsByFulfillmentOrder[]": [{}],
    "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderId": "gid://shopify/FulfillmentOrder/10079785100",
    "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[]": [{}],
    "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].id": "gid://shopify/FulfillmentOrderLineItem/123456789",
    "variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].quantity": "1",
    "variables.fulfillment.trackingInfo.number": "1Z999AA10123456784"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | GraphQL variables for the fulfillment. |
| `variables.fulfillment` | object | no | The fulfillment details sent to Shopify. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[]` | array<object> | yes | One or more fulfillment orders assigned to the same Shopify order and location. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderId` | string | yes | Shopify Fulfillment Order GID. Example: `gid://shopify/FulfillmentOrder/10079785100`. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[]` | array<object> | yes | Add each confirmed Fulfillment Order line item and quantity to ship. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].id` | string | yes | Shopify Fulfillment Order Line Item GID, not the ordinary Order Line Item GID. Example: `gid://shopify/FulfillmentOrderLineItem/123456789`. |
| `variables.fulfillment.lineItemsByFulfillmentOrder[].fulfillmentOrderLineItems[].quantity` | number | yes | Quantity of this fulfillment-order line item to fulfill. Example: `1`. |
| `variables.fulfillment.trackingInfo` | object | no | Tracking information for the shipment. |
| `variables.fulfillment.trackingInfo.company` | string | no | Carrier name. A Shopify-supported carrier can enable automatic tracking URLs. Example: `UPS`. |
| `variables.fulfillment.trackingInfo.number` | string | yes | Example: `1Z999AA10123456784`. |
| `variables.fulfillment.notifyCustomer` | boolean | no | Whether Shopify should email the customer about the fulfillment. Defaults to false. Default: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.fulfillment.trackingInfo.url` | string | no | Optional complete tracking URL. Example: `https://www.ups.com/track?tracknum=...`. |
| `variables.message` | string | no | Optional message associated with the fulfillment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopify API returns.

## Native endpoint

Through the native Shopify API, this operation is `POST 2026-07/graphql.json` (base URL `https://{{credentials.storeName}}.myshopify.com/admin/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order-fulfillment-graph-ql.md) for the provider-specific parameters and requirements.


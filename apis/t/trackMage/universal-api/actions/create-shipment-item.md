# TrackMage: Create Shipment Item

Creates a new shipment item in TrackMage.

```
POST https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-shipment-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TrackMage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-shipment-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipment": {},
  "orderItem": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackMage/latest/actions/create-shipment-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipment": {},
    "orderItem": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `shipment` | object | yes |  |
| `orderItem` | string | yes | The order item reference to which the shipment items item belongs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `qty` | number | no | The number of items in the shipment. Default and the minimum value is 0. The value cannot be greater than available quantity of the order item (orderItem.qty - orderItem.fulfilledQty). |
| `externalSourceSyncId` | string | no | The id of the shipment item in ecommerce store (WooCommerce, Shopify, etc.). |
| `externalSourceIntegration` | string | no | The workflow reference to integration for ecommerce store. |
| `fulfillmentIntegration` | string | no | The workflow reference to integration for fulfillment source. |
| `fulfillmentSyncId` | string | no | The id of the shipment item in the fulfillment source system (AliExpress, Amazon, etc.). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "externalSourceIntegration": "string",
      "externalSourceSyncId": "string",
      "fulfillmentIntegration": "string",
      "fulfillmentSyncId": "string",
      "id": "string",
      "orderItem": "string",
      "qty": 1,
      "shipment": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `externalSourceIntegration` | string |  |
| `externalSourceSyncId` | string |  |
| `fulfillmentIntegration` | string |  |
| `fulfillmentSyncId` | string |  |
| `id` | string |  |
| `orderItem` | string |  |
| `qty` | number |  |
| `shipment` | string |  |

## Native endpoint

Through the native TrackMage API, this operation is `POST /shipment_items` (base URL `https://api.trackmage.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment-item.md) for the provider-specific parameters and requirements.


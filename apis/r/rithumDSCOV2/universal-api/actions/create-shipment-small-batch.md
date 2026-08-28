# Rithum DSCO: Create Shipment Small Batch



```
POST https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/create-shipment-small-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/create-shipment-small-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipments[]": [
    {}
  ],
  "shipments[].lineItems[]": [
    {}
  ],
  "shipments[].trackingNumber": "string",
  "shipments[].lineItems[].quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/create-shipment-small-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipments[]": [{}],
    "shipments[].lineItems[]": [{}],
    "shipments[].trackingNumber": "string",
    "shipments[].lineItems[].quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dscoOrderId` | string | no | DSCO order ID. Provide this or poNumber or supplierOrderNumber to identify the order. |
| `poNumber` | string | no | Purchase order number. Provide this or dscoOrderId or supplierOrderNumber to identify the order. |
| `supplierOrderNumber` | string | no | Supplier order number. Provide this or dscoOrderId or poNumber to identify the order. |
| `shipments[]` | array<object> | yes | Array of shipment objects to add to the order. |
| `shipments[].lineItems[]` | array<object> | yes | Line items included in the shipment. |
| `shipments[].trackingNumber` | string | yes | Carrier tracking number for the shipment. |
| `shipments[].lineItems[].quantity` | number | yes | Quantity of this line item included in the shipment. |
| `shipments[].shipDate` | date | no | Shipment date in ISO 8601 format. |
| `shipments[].lineItems[].lineNumber` | number | no | Order line number for the shipped item when needed to disambiguate the item. |
| `shipments[].lineItems[].sku` | string | no | SKU of the shipped item. One item identifier is required on each shipment line item. |
| `shipments[].shipCarrier` | string | no | Carrier name for the shipment. |
| `shipments[].shipMethod` | string | no | Shipping method for the shipment. |
| `shipments[].warehouseCode` | string | no | Warehouse code for the shipment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventDate": "2026-05-07T12:00:00.000Z",
      "requestId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventDate` | date | Timestamp of the batch request. |
| `requestId` | string | DSCO request ID for the small batch shipment request. |
| `status` | string | Shipment batch creation status. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `POST order/shipment/batch/small` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-shipment-small-batch.md) for the provider-specific parameters and requirements.


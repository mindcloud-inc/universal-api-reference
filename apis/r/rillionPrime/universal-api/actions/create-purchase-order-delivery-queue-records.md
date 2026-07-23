# Rillion Prime: Create Purchase Order Delivery Queue Records



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-purchase-order-delivery-queue-records
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-purchase-order-delivery-queue-records" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-purchase-order-delivery-queue-records', {
  method: 'POST',
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
| `purchaseOrderDeliveries[]` | array<object> | no | Request body value for PurchaseOrderDeliveries. |
| `purchaseOrderDeliveries[].company` | string | no |  |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].purchaseOrderNo` | string | no |  |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].lineNo` | string | no |  |
| `purchaseOrderDeliveries[].supplier` | string | no |  |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].number` | number | no |  |
| `purchaseOrderDeliveries[].supplierDeliveryNote` | string | no |  |
| `purchaseOrderDeliveries[].deliveryNote` | string | no |  |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].amount` | number | no |  |
| `purchaseOrderDeliveries[].deliveryDate` | string | no |  |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[].queueStatus` | number | no |  |
| `purchaseOrderDeliveries[].queueStatus` | number | no |  |
| `purchaseOrderDeliveries[].purchaseOrderDeliveryLines[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Rillion Prime API, this operation is `PUT /purchaseorderdeliveryqueue` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order-delivery-queue-records.md) for the provider-specific parameters and requirements.


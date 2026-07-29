# Rillion Prime Web Service: Insert Purchase Order Receipt

Insert a purchase order receipt in Prime.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-purchase-order-receipt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-purchase-order-receipt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderReceipt": {},
  "purchaseOrderReceipt.ean": "string",
  "purchaseOrderReceipt.purchaseOrderNo": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-purchase-order-receipt', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderReceipt": {},
    "purchaseOrderReceipt.ean": "string",
    "purchaseOrderReceipt.purchaseOrderNo": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderReceipt` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, PurchaseOrderReceipt section. |
| `purchaseOrderReceipt.ean` | string | yes | EAN/GLN of the company to which the order belongs |
| `purchaseOrderReceipt.purchaseOrderNo` | string | yes | Order number |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderReceipt.supplierPurchaseOrderNo` | string | no | The supplier’s order number |
| `purchaseOrderReceipt.plannedDeliveryDate` | date | no | Planned delivery date |
| `purchaseOrderReceipt.confirmedDeliveryDate` | date | no | Planned delivery date |
| `purchaseOrderReceipt.status` | string | no | Purchase order status: 2=Order confirmed (default); 3=Delivery notified |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-purchase-order-receipt.md) for the provider-specific parameters and requirements.


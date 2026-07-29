# Rillion Prime Web Service: Insert Purchase Order Delivery

Register a delivery against a purchase order in Prime.

```
POST https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-purchase-order-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-purchase-order-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrderDelivery": {},
  "purchaseOrderDelivery.company": "string",
  "purchaseOrderDelivery.supplier": "string",
  "purchaseOrderDelivery.supplierDeliveryNote": "string",
  "purchaseOrderDelivery.deliveryDate": "2026-05-07T12:00:00.000Z",
  "purchaseOrderDelivery.purchaseOrderDeliveryLine[].purchaseOrderNo": "string",
  "purchaseOrderDelivery.purchaseOrderDeliveryLine[].lineNo": "string",
  "purchaseOrderDelivery.purchaseOrderDeliveryLine[].number": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/insert-purchase-order-delivery', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrderDelivery": {},
    "purchaseOrderDelivery.company": "string",
    "purchaseOrderDelivery.supplier": "string",
    "purchaseOrderDelivery.supplierDeliveryNote": "string",
    "purchaseOrderDelivery.deliveryDate": "2026-05-07T12:00:00.000Z",
    "purchaseOrderDelivery.purchaseOrderDeliveryLine[].purchaseOrderNo": "string",
    "purchaseOrderDelivery.purchaseOrderDeliveryLine[].lineNo": "string",
    "purchaseOrderDelivery.purchaseOrderDeliveryLine[].number": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderDelivery` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, PurchaseOrderDelivery section. |
| `purchaseOrderDelivery.company` | list<string> | yes | Company |
| `purchaseOrderDelivery.supplier` | string | yes | Supplier |
| `purchaseOrderDelivery.supplierDeliveryNote` | string | yes | Goods reciept number on the delivery reciept (can be used in PO matching) |
| `purchaseOrderDelivery.deliveryDate` | date | yes | Delivery date |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[]` | array<object> | no | Purchase Order Delivery Line lines. |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].purchaseOrderNo` | string | yes | Order number |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].lineNo` | string | yes | Order line number |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].number` | number | yes | Quantity delivered |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrderDelivery.deliveryNote` | string | no | Delivery slip |
| `purchaseOrderDelivery.note` | string | no | Free text |
| `purchaseOrderDelivery.group1` | string | no | Free group 1 |
| `purchaseOrderDelivery.group2` | string | no | Free group 2 |
| `purchaseOrderDelivery.group3` | string | no | Free group 3 |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].amount` | number | no | Amount delivered |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].note` | string | no | Free text |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].group1` | string | no | Free group 1 |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].group2` | string | no | Free group 2 |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].group3` | string | no | Free group 3 |
| `purchaseOrderDelivery.purchaseOrderDeliveryLine[].subDelivery` | string | no | Partial delivery id to purchase order line. |
| `purchaseOrderDelivery.externalId` | string | no |  |
| `purchaseOrderDelivery.externalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-purchase-order-delivery.md) for the provider-specific parameters and requirements.


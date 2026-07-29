# Rillion Prime Web Service: Synchronize Purchase Order

Synchronize an existing purchase order in Prime with the ERP version. Undocumented in the vendor guide — confirm semantics with Rillion before production use.

```
PUT https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/synchronize-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Web Service `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/synchronize-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "purchaseOrder": {},
  "purchaseOrder.company": "string",
  "purchaseOrder.purchaseOrderNo": "string",
  "purchaseOrder.purchaseOrderMatchType": 1,
  "purchaseOrder.supplier": "string",
  "purchaseOrder.currency": "string",
  "purchaseOrder.purchaseOrderLine[].company": "string",
  "purchaseOrder.purchaseOrderLine[].purchaseOrderNo": "string",
  "purchaseOrder.purchaseOrderLine[].lineNo": "string",
  "purchaseOrder.purchaseOrderLine[].item": "string",
  "purchaseOrder.purchaseOrderLine[].number": 1,
  "purchaseOrder.purchaseOrderLine[].price": 1,
  "purchaseOrder.purchaseOrderLine[].amount": 1,
  "purchaseOrder.purchaseOrderLine[].discount": 1,
  "transferFromQueue": "true"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrimeWebService/latest/actions/synchronize-purchase-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "purchaseOrder": {},
    "purchaseOrder.company": "string",
    "purchaseOrder.purchaseOrderNo": "string",
    "purchaseOrder.purchaseOrderMatchType": 1,
    "purchaseOrder.supplier": "string",
    "purchaseOrder.currency": "string",
    "purchaseOrder.purchaseOrderLine[].company": "string",
    "purchaseOrder.purchaseOrderLine[].purchaseOrderNo": "string",
    "purchaseOrder.purchaseOrderLine[].lineNo": "string",
    "purchaseOrder.purchaseOrderLine[].item": "string",
    "purchaseOrder.purchaseOrderLine[].number": 1,
    "purchaseOrder.purchaseOrderLine[].price": 1,
    "purchaseOrder.purchaseOrderLine[].amount": 1,
    "purchaseOrder.purchaseOrderLine[].discount": 1,
    "transferFromQueue": "true"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrder` | object | yes | Fill in the fields below, or use Use Variables ({}) on this object to map the whole payload from a previous step. Field semantics: Prime Integration Tables, PurchaseOrder section. |
| `purchaseOrder.company` | list<string> | yes | Company to which the orderline belongs (FK to purchase order line) |
| `purchaseOrder.purchaseOrderNo` | string | yes | Order number (FK to purchase order line) |
| `purchaseOrder.purchaseOrderMatchType` | number | yes | Type of matching: 0=Quantity matching (set by default by the system), 1=Amount matching. |
| `purchaseOrder.supplier` | string | yes | Supplier |
| `purchaseOrder.currency` | string | yes | Currency |
| `purchaseOrder.purchaseOrderLine[]` | array<object> | no | Purchase Order Line lines. |
| `purchaseOrder.purchaseOrderLine[].company` | list<string> | yes | Company to which the orderline belongs (FK to purchase order line) |
| `purchaseOrder.purchaseOrderLine[].purchaseOrderNo` | string | yes | Order number (FK to purchase order line) |
| `purchaseOrder.purchaseOrderLine[].lineNo` | string | yes | Line number (FK to purchase order line) |
| `purchaseOrder.purchaseOrderLine[].item` | string | yes | Item |
| `purchaseOrder.purchaseOrderLine[].number` | number | yes | Quantity |
| `purchaseOrder.purchaseOrderLine[].price` | number | yes | Unit price |
| `purchaseOrder.purchaseOrderLine[].amount` | number | yes | Line amount |
| `purchaseOrder.purchaseOrderLine[].discount` | number | yes | Discount in % |
| `transferFromQueue` | boolean | yes | Process the record from the queue immediately. Leave true unless your Rillion contact advises otherwise. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `purchaseOrder.status` | number | no | Purchase order status: 0=Created; 1=Ordered; 2=Order confirmed; 3=Delivery notified |
| `purchaseOrder.purchaseDate` | date | no | Order date |
| `purchaseOrder.supplierPurchaseOrderNo` | string | no | The supplier’s order number |
| `purchaseOrder.reference1` | string | no | Reference of type 1 |
| `purchaseOrder.reference2` | string | no | Reference of type 2 |
| `purchaseOrder.plannedDeliveryDate` | date | no | Planned delivery date |
| `purchaseOrder.plannedPaymentDueDate` | date | no | Planned payment date |
| `purchaseOrder.headerText` | string | no | Free text printed out on purchase order |
| `purchaseOrder.note` | string | no | Free text |
| `purchaseOrder.invoiceSeries` | string | no | Invoice series |
| `purchaseOrder.invoiceNo` | number | no | Invoice number |
| `purchaseOrder.remove` | number | no | Is the record to be deleted: 0=No; 1=Yes |
| `purchaseOrder.responsiblePurchaseOrderEmail` | string | no | E-mail adress to responsible purchaser |
| `purchaseOrder.autoDelivery` | boolean | no | AutoDelivery: 1=Delivery automatically created |
| `purchaseOrder.group1` | string | no | Free group 1 |
| `purchaseOrder.group2` | string | no | Free group 2 |
| `purchaseOrder.group3` | string | no | Free group 3 |
| `purchaseOrder.validTo` | date | no | Valid to date for PurchaseOrder. |
| `purchaseOrder.purchaseOrderLine[].fullyDelivered` | number | no | Set the purchase order line status to fully delivered: 0=No, 1=Yes |
| `purchaseOrder.purchaseOrderLine[].fullyInvoiced` | number | no | Set the purchase order line status to fully invoiced: 0=No, 1=Yes |
| `purchaseOrder.purchaseOrderLine[].yourReference` | string | no | Your reference |
| `purchaseOrder.purchaseOrderLine[].goodsLabel` | string | no | Goods labelling |
| `purchaseOrder.purchaseOrderLine[].description` | string | no | Description |
| `purchaseOrder.purchaseOrderLine[].attribute` | string | no | Attribute |
| `purchaseOrder.purchaseOrderLine[].unit` | string | no | Unit |
| `purchaseOrder.purchaseOrderLine[].supplierItem` | string | no | Supplier’s item number |
| `purchaseOrder.purchaseOrderLine[].plannedDeliveryDate` | date | no | Planned delivery date |
| `purchaseOrder.purchaseOrderLine[].note` | string | no | Free text |
| `purchaseOrder.purchaseOrderLine[].deliveryNote` | string | no |  |
| `purchaseOrder.purchaseOrderLine[].invoicedNumber` | number | no | Quantity of the order already matched to an invoice in the ERP system. |
| `purchaseOrder.purchaseOrderLine[].invoicedPrice` | number | no | Price of the order already matched to an invoice in the ERP system. |
| `purchaseOrder.purchaseOrderLine[].invoicedAmount` | number | no | Amount of the order already matched to an invoice in the ERP system. |
| `purchaseOrder.purchaseOrderLine[].invoiceSeries` | string | no | Invoice series |
| `purchaseOrder.purchaseOrderLine[].invoiceNo` | number | no | Invoice number |
| `purchaseOrder.purchaseOrderLine[].invoiceStatus` | number | no |  |
| `purchaseOrder.purchaseOrderLine[].remove` | number | no | Is the record to be deleted: 0=No; 1=Yes |
| `purchaseOrder.purchaseOrderLine[].group1` | string | no | Free group 1 |
| `purchaseOrder.purchaseOrderLine[].group2` | string | no | Free group 2 |
| `purchaseOrder.purchaseOrderLine[].group3` | string | no | Free group 3 |
| `purchaseOrder.purchaseOrderLine[].externalId` | string | no |  |
| `purchaseOrder.purchaseOrderLine[].externalSource` | string | no |  |
| `purchaseOrder.externalId` | string | no |  |
| `purchaseOrder.externalSource` | string | no |  |
| `purchaseOrder.currencyExternalId` | string | no |  |
| `purchaseOrder.currencyExternalSource` | string | no |  |
| `purchaseOrder.supplierExternalId` | string | no |  |
| `purchaseOrder.supplierExternalSource` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Web Service API returns.

## Native endpoint

Through the native Rillion Prime Web Service API, this operation is `POST` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/synchronize-purchase-order.md) for the provider-specific parameters and requirements.


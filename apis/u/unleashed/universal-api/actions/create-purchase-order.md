# Unleashed: Create Purchase Order

Creates a new purchase order in Unleashed.

```
POST https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "supplier.supplierCode": "string",
  "deliveryDate": "2026-05-07T12:00:00.000Z",
  "taxCode": "string",
  "taxRate": 1,
  "orderStatus": "string",
  "warehouse.warehouseCode": "string",
  "purchaseOrderLines[].lineNumber": 1,
  "purchaseOrderLines[].orderQuantity": 1,
  "purchaseOrderLines[].lineTotal": 1,
  "purchaseOrderLines[].lineTax": 1,
  "purchaseOrderLines[].product.productCode": "string",
  "subTotal": 1,
  "taxTotal": 1,
  "total": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-purchase-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "supplier.supplierCode": "string",
    "deliveryDate": "2026-05-07T12:00:00.000Z",
    "taxCode": "string",
    "taxRate": 1,
    "orderStatus": "string",
    "warehouse.warehouseCode": "string",
    "purchaseOrderLines[].lineNumber": 1,
    "purchaseOrderLines[].orderQuantity": 1,
    "purchaseOrderLines[].lineTotal": 1,
    "purchaseOrderLines[].lineTax": 1,
    "purchaseOrderLines[].product.productCode": "string",
    "subTotal": 1,
    "taxTotal": 1,
    "total": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `supplier` | object | no | Supplier object for the purchase order. |
| `supplier.supplierCode` | string | yes | Supplier code for the purchase order supplier. |
| `deliveryDate` | date | yes | Requested delivery date for the purchase order. |
| `taxCode` | string | yes | Tax code for the purchase order. |
| `taxRate` | number | yes | Tax rate for the purchase order. |
| `discountRate` | number | no | Overall purchase order discount rate. |
| `orderStatus` | string | yes | Order status for the purchase order. |
| `warehouse` | object | no | Warehouse object for the purchase order. |
| `warehouse.warehouseCode` | string | yes | Warehouse code for the purchase order warehouse. |
| `purchaseOrderLines[].lineNumber` | number | yes | Line number for the purchase order line. |
| `purchaseOrderLines[].orderQuantity` | number | yes | Ordered quantity for the purchase order line. |
| `purchaseOrderLines[].unitPrice` | number | no | Unit price for the purchase order line. |
| `purchaseOrderLines[].lineTotal` | number | yes | Line total for the purchase order line. |
| `purchaseOrderLines[].lineTax` | number | yes | Line tax for the purchase order line. |
| `purchaseOrderLines[].product.productCode` | string | yes | Product code for the purchase order line product. |
| `subTotal` | number | yes | Purchase order subtotal. |
| `taxTotal` | number | yes | Purchase order tax total. |
| `total` | number | yes | Purchase order total. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "completedDate": "string",
      "currency": {},
      "deliveryDate": "string",
      "discountRate": 1,
      "exchangeRate": 1,
      "guid": "string",
      "lastModifiedOn": "string",
      "orderDate": "string",
      "orderNumber": "string",
      "orderStatus": "string",
      "purchaseOrderLines": [
        {}
      ],
      "salesOrders": [
        {}
      ],
      "subTotal": 1,
      "supplier": {},
      "supplierInvoiceDate": "string",
      "supplierRef": "string",
      "tax": {},
      "taxCode": "string",
      "taxRate": 1,
      "taxTotal": 1,
      "total": 1,
      "warehouse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | string |  |
| `completedDate` | string |  |
| `currency` | object |  |
| `deliveryDate` | string |  |
| `discountRate` | number |  |
| `exchangeRate` | number |  |
| `guid` | string |  |
| `lastModifiedOn` | string |  |
| `orderDate` | string |  |
| `orderNumber` | string |  |
| `orderStatus` | string |  |
| `purchaseOrderLines` | array<object> |  |
| `salesOrders` | array<object> |  |
| `subTotal` | number |  |
| `supplier` | object |  |
| `supplierInvoiceDate` | string |  |
| `supplierRef` | string |  |
| `tax` | object |  |
| `taxCode` | string |  |
| `taxRate` | number |  |
| `taxTotal` | number |  |
| `total` | number |  |
| `warehouse` | object |  |

## Native endpoint

Through the native Unleashed API, this operation is `POST /PurchaseOrders` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-purchase-order.md) for the provider-specific parameters and requirements.


# Unleashed: Create Sales Order

Creates a new sales order in Unleashed.

```
POST https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customer.customerCode": "string",
  "warehouse.warehouseCode": "string",
  "exchangeRate": 1,
  "orderStatus": "string",
  "tax.taxCode": "string",
  "tax.taxRate": 1,
  "taxRate": 1,
  "subTotal": 1,
  "taxTotal": 1,
  "total": 1,
  "salesOrderLines[].lineNumber": 1,
  "salesOrderLines[].product.productCode": "string",
  "salesOrderLines[].orderQuantity": 1,
  "salesOrderLines[].unitPrice": 1,
  "salesOrderLines[].lineTotal": 1,
  "salesOrderLines[].lineTax": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-sales-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customer.customerCode": "string",
    "warehouse.warehouseCode": "string",
    "exchangeRate": 1,
    "orderStatus": "string",
    "tax.taxCode": "string",
    "tax.taxRate": 1,
    "taxRate": 1,
    "subTotal": 1,
    "taxTotal": 1,
    "total": 1,
    "salesOrderLines[].lineNumber": 1,
    "salesOrderLines[].product.productCode": "string",
    "salesOrderLines[].orderQuantity": 1,
    "salesOrderLines[].unitPrice": 1,
    "salesOrderLines[].lineTotal": 1,
    "salesOrderLines[].lineTax": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer.customerCode` | string | yes | Customer code for the sales order customer. |
| `warehouse.warehouseCode` | string | yes | Warehouse code for the sales order warehouse. |
| `exchangeRate` | number | yes | Exchange rate for the sales order. |
| `orderStatus` | string | yes | Order status for the sales order. |
| `tax.taxCode` | string | yes | Tax code for the sales order. |
| `tax.taxRate` | number | yes | Tax rate inside the sales order tax object. |
| `taxRate` | number | yes | Tax rate for the sales order. |
| `subTotal` | number | yes | Sales order subtotal. |
| `taxTotal` | number | yes | Sales order tax total. |
| `total` | number | yes | Sales order total. |
| `salesOrderLines[].lineNumber` | number | yes | Line number for the sales order line. |
| `salesOrderLines[].product.productCode` | string | yes | Product code for the sales order line product. |
| `salesOrderLines[].orderQuantity` | number | yes | Ordered quantity for the sales order line. |
| `salesOrderLines[].unitPrice` | number | yes | Unit price for the sales order line. |
| `salesOrderLines[].lineTotal` | number | yes | Line total for the sales order line. |
| `salesOrderLines[].lineTax` | number | yes | Line tax for the sales order line. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allocateProduct": true,
      "comments": "string",
      "completedDate": "string",
      "currency": {},
      "customer": {},
      "customerRef": "string",
      "customOrderStatus": "string",
      "exchangeRate": 1,
      "guid": "string",
      "lastModifiedOn": "string",
      "orderDate": "string",
      "orderNumber": "string",
      "orderStatus": "string",
      "paymentDueDate": "string",
      "requiredDate": "string",
      "salesOrderLines": [
        {}
      ],
      "salesPerson": "string",
      "subTotal": 1,
      "tax": {},
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
| `allocateProduct` | boolean |  |
| `comments` | string |  |
| `completedDate` | string |  |
| `currency` | object |  |
| `customer` | object |  |
| `customerRef` | string |  |
| `customOrderStatus` | string |  |
| `exchangeRate` | number |  |
| `guid` | string |  |
| `lastModifiedOn` | string |  |
| `orderDate` | string |  |
| `orderNumber` | string |  |
| `orderStatus` | string |  |
| `paymentDueDate` | string |  |
| `requiredDate` | string |  |
| `salesOrderLines` | array<object> |  |
| `salesPerson` | string |  |
| `subTotal` | number |  |
| `tax` | object |  |
| `taxRate` | number |  |
| `taxTotal` | number |  |
| `total` | number |  |
| `warehouse` | object |  |

## Native endpoint

Through the native Unleashed API, this operation is `POST /SalesOrders` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-sales-order.md) for the provider-specific parameters and requirements.


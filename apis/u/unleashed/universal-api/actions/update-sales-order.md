# Unleashed: Update Sales Order

Updates an existing sales order in Unleashed.

```
PUT https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderGuid": "string",
  "exchangeRate": 1,
  "orderStatus": "string",
  "tax.taxCode": "string",
  "warehouse.warehouseCode": "string",
  "tax.taxRate": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderGuid": "string",
    "exchangeRate": 1,
    "orderStatus": "string",
    "tax.taxCode": "string",
    "warehouse.warehouseCode": "string",
    "tax.taxRate": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderGuid` | string | yes | The Unleashed sales order GUID. |
| `exchangeRate` | number | yes | Exchange rate for the sales order. |
| `orderStatus` | string | yes | Order status for the sales order. |
| `tax.taxCode` | string | yes | Tax code for the sales order. |
| `warehouse.warehouseCode` | string | yes | Warehouse code for the sales order warehouse. |
| `tax.taxRate` | number | yes | Tax rate inside the sales order tax object. |
| `comments` | string | no | Comments for the sales order. |

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

Through the native Unleashed API, this operation is `PUT /SalesOrders/:orderGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sales-order.md) for the provider-specific parameters and requirements.


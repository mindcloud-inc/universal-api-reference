# Unleashed: Update Purchase Order

Updates an existing purchase order in Unleashed.

```
PUT https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderGuid": "string",
  "supplier.supplierCode": "string",
  "orderStatus": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/update-purchase-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "orderGuid": "string",
    "supplier.supplierCode": "string",
    "orderStatus": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderGuid` | string | yes | The Unleashed purchase order GUID. |
| `supplier.supplierCode` | string | yes | Supplier code for the purchase order supplier. |
| `orderStatus` | string | yes | Order status for the purchase order. |
| `comments` | string | no | Comments for the purchase order. |

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

Through the native Unleashed API, this operation is `PUT /PurchaseOrders/:orderGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-purchase-order.md) for the provider-specific parameters and requirements.


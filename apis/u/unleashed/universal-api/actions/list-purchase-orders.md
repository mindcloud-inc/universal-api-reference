# Unleashed: List Purchase Orders

Retrieves purchase orders from your Unleashed account.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-purchase-orders?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Unleashed API, this operation is `GET /PurchaseOrders/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-orders.md) for the provider-specific parameters and requirements.


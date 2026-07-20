# Unleashed: List Sales Orders

Retrieves sales orders from your Unleashed account.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-sales-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-sales-orders?${params}`, {
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

Through the native Unleashed API, this operation is `GET /SalesOrders/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-orders.md) for the provider-specific parameters and requirements.


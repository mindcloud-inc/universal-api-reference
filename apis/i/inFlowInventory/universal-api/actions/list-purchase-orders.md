# inFlow Inventory: List Purchase Orders

Retrieves purchase orders from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/list-purchase-orders?${params}`, {
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
      "amountPaid": "string",
      "balance": "string",
      "contactName": "Ava Chen",
      "currencyId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "freight": "string",
      "inventoryStatus": "string",
      "isCancelled": true,
      "isCompleted": true,
      "isQuote": true,
      "isTaxInclusive": true,
      "lastModifiedById": "string",
      "locationId": "string",
      "nonVendorCosts": {
        "isPercent": true,
        "value": "string"
      },
      "orderDate": "2026-05-07T12:00:00.000Z",
      "orderNumber": "string",
      "paidDate": "2026-05-07T12:00:00.000Z",
      "paymentStatus": "string",
      "paymentTermsId": "string",
      "phone": "string",
      "purchaseOrderId": "string",
      "requestShipDate": "2026-05-07T12:00:00.000Z",
      "shipToAddress": {
        "address1": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "subTotal": "string",
      "tax1": "string",
      "tax1Rate": "string",
      "tax2": "string",
      "tax2Rate": "string",
      "timestamp": "string",
      "total": "string",
      "vendorAddress": {
        "address1": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "vendorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amountPaid` | string |  |
| `balance` | string |  |
| `contactName` | string |  |
| `currencyId` | string |  |
| `dueDate` | date |  |
| `email` | string |  |
| `freight` | string |  |
| `inventoryStatus` | string |  |
| `isCancelled` | boolean |  |
| `isCompleted` | boolean |  |
| `isQuote` | boolean |  |
| `isTaxInclusive` | boolean |  |
| `lastModifiedById` | string |  |
| `locationId` | string |  |
| `nonVendorCosts.isPercent` | boolean |  |
| `nonVendorCosts.value` | string |  |
| `orderDate` | date |  |
| `orderNumber` | string |  |
| `paidDate` | date |  |
| `paymentStatus` | string |  |
| `paymentTermsId` | string |  |
| `phone` | string |  |
| `purchaseOrderId` | string |  |
| `requestShipDate` | date |  |
| `shipToAddress.address1` | string |  |
| `shipToAddress.city` | string |  |
| `shipToAddress.country` | string |  |
| `shipToAddress.postalCode` | string |  |
| `shipToAddress.state` | string |  |
| `subTotal` | string |  |
| `tax1` | string |  |
| `tax1Rate` | string |  |
| `tax2` | string |  |
| `tax2Rate` | string |  |
| `timestamp` | string |  |
| `total` | string |  |
| `vendorAddress.address1` | string |  |
| `vendorAddress.city` | string |  |
| `vendorAddress.country` | string |  |
| `vendorAddress.postalCode` | string |  |
| `vendorAddress.state` | string |  |
| `vendorId` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `GET /purchase-orders` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-orders.md) for the provider-specific parameters and requirements.


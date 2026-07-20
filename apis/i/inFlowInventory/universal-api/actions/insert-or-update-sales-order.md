# inFlow Inventory: Insert or Update Sales Order

Inserts or updates a sales order in inFlow Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/insert-or-update-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
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
      "billingAddress": {
        "address1": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "contactName": "Ava Chen",
      "currencyId": "string",
      "customerId": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "inventoryStatus": "string",
      "isCancelled": true,
      "isCompleted": true,
      "isInvoiced": true,
      "isPrioritized": true,
      "isQuote": true,
      "isTaxInclusive": true,
      "lastModifiedById": "string",
      "locationId": "string",
      "nonCustomerCost": {
        "isPercent": true,
        "value": "string"
      },
      "orderDate": "2026-05-07T12:00:00.000Z",
      "orderFreight": "string",
      "orderNumber": "string",
      "paidDate": "2026-05-07T12:00:00.000Z",
      "paymentStatus": "string",
      "paymentTermsId": "string",
      "phone": "string",
      "pricingSchemeId": "string",
      "requestedShipDate": "2026-05-07T12:00:00.000Z",
      "salesOrderId": "string",
      "shippedDate": "2026-05-07T12:00:00.000Z",
      "shippingAddress": {
        "address1": "string",
        "city": "string",
        "country": "string",
        "postalCode": "string",
        "state": "string"
      },
      "source": "string",
      "subTotal": "string",
      "tax1": "string",
      "tax1Rate": "string",
      "tax2": "string",
      "tax2Rate": "string",
      "timestamp": "string",
      "total": "string"
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
| `billingAddress.address1` | string |  |
| `billingAddress.city` | string |  |
| `billingAddress.country` | string |  |
| `billingAddress.postalCode` | string |  |
| `billingAddress.state` | string |  |
| `contactName` | string |  |
| `currencyId` | string |  |
| `customerId` | string |  |
| `dueDate` | date |  |
| `email` | string |  |
| `inventoryStatus` | string |  |
| `isCancelled` | boolean |  |
| `isCompleted` | boolean |  |
| `isInvoiced` | boolean |  |
| `isPrioritized` | boolean |  |
| `isQuote` | boolean |  |
| `isTaxInclusive` | boolean |  |
| `lastModifiedById` | string |  |
| `locationId` | string |  |
| `nonCustomerCost.isPercent` | boolean |  |
| `nonCustomerCost.value` | string |  |
| `orderDate` | date |  |
| `orderFreight` | string |  |
| `orderNumber` | string |  |
| `paidDate` | date |  |
| `paymentStatus` | string |  |
| `paymentTermsId` | string |  |
| `phone` | string |  |
| `pricingSchemeId` | string |  |
| `requestedShipDate` | date |  |
| `salesOrderId` | string |  |
| `shippedDate` | date |  |
| `shippingAddress.address1` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.postalCode` | string |  |
| `shippingAddress.state` | string |  |
| `source` | string |  |
| `subTotal` | string |  |
| `tax1` | string |  |
| `tax1Rate` | string |  |
| `tax2` | string |  |
| `tax2Rate` | string |  |
| `timestamp` | string |  |
| `total` | string |  |

## Native endpoint

Through the native inFlow Inventory API, this operation is `PUT /sales-orders` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-or-update-sales-order.md) for the provider-specific parameters and requirements.


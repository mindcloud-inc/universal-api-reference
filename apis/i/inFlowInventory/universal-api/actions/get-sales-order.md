# inFlow Inventory: Get Sales Order

Retrieves an existing sales order from inFlow Inventory.

```
GET https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a inFlow Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-sales-order?connectionId=$CONNECTION_ID&salesOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "salesOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inFlowInventory/latest/actions/get-sales-order?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `salesOrderId` | string | yes | The inFlow sales order ID. |

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

Through the native inFlow Inventory API, this operation is `GET /sales-orders/:salesOrderId` (base URL `https://cloudapi.inflowinventory.com/{{credentials.companyId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sales-order.md) for the provider-specific parameters and requirements.


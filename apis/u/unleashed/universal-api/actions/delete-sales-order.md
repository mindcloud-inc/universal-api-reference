# Unleashed: Delete Sales Order

Deletes an existing sales order from Unleashed.

```
DELETE https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/delete-sales-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/delete-sales-order?connectionId=$CONNECTION_ID&orderGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/delete-sales-order?${params}`, {
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
| `orderGuid` | string | yes | The Unleashed sales order GUID. |

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

Through the native Unleashed API, this operation is `DELETE /SalesOrders/:orderGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sales-order.md) for the provider-specific parameters and requirements.


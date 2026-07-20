# Katana: Retrieve Manufacturing Order

Retrieves a manufacturing order by ID from Katana.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-manufacturing-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-manufacturing-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/retrieve-manufacturing-order?${params}`, {
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
| `id` | number | yes | Manufacturing order id |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualQuantity": "string",
      "additionalInfo": "string",
      "batchTransactions": [
        "string"
      ],
      "createdAt": "string",
      "deletedAt": "string",
      "doneDate": "string",
      "id": 1,
      "ingredientAvailability": "string",
      "isLinkedToSalesOrder": true,
      "locationId": 1,
      "materialCost": 1,
      "operationsCost": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "plannedQuantity": 1,
      "productionDeadlineDate": "string",
      "salesOrderDeliveryDeadline": "string",
      "salesOrderId": 1,
      "salesOrderRowId": 1,
      "serialNumbers": [
        {
          "id": 1,
          "resourceId": 1,
          "resourceType": "string",
          "serialNumber": "string",
          "transactionDate": "string",
          "transactionId": "string"
        }
      ],
      "status": "string",
      "subassembliesCost": 1,
      "totalActualTime": 1,
      "totalCost": 1,
      "totalPlannedTime": 1,
      "updatedAt": "string",
      "variantId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualQuantity` | string |  |
| `additionalInfo` | string |  |
| `batchTransactions` | array<string> |  |
| `createdAt` | string |  |
| `deletedAt` | string |  |
| `doneDate` | string |  |
| `id` | number |  |
| `ingredientAvailability` | string |  |
| `isLinkedToSalesOrder` | boolean |  |
| `locationId` | number |  |
| `materialCost` | number |  |
| `operationsCost` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `plannedQuantity` | number |  |
| `productionDeadlineDate` | string |  |
| `salesOrderDeliveryDeadline` | string |  |
| `salesOrderId` | number |  |
| `salesOrderRowId` | number |  |
| `serialNumbers` | array<object> |  |
| `serialNumbers[].id` | number |  |
| `serialNumbers[].resourceId` | number |  |
| `serialNumbers[].resourceType` | string |  |
| `serialNumbers[].serialNumber` | string |  |
| `serialNumbers[].transactionDate` | string |  |
| `serialNumbers[].transactionId` | string |  |
| `status` | string |  |
| `subassembliesCost` | number |  |
| `totalActualTime` | number |  |
| `totalCost` | number |  |
| `totalPlannedTime` | number |  |
| `updatedAt` | string |  |
| `variantId` | number |  |

## Native endpoint

Through the native Katana API, this operation is `GET /manufacturing_orders/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-manufacturing-order.md) for the provider-specific parameters and requirements.


# Katana: List Manufacturing Orders

Lists manufacturing orders in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-manufacturing-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-manufacturing-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-manufacturing-orders?${params}`, {
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
| `ids[]` | array<number> | no | Filters manufacturing orders by an array of IDs |
| `status` | string | no | Filters manufacturing orders by a status. |
| `orderNo` | string | no | Filters manufacturing orders by an order number. |
| `locationId` | number | no | Filters manufacturing orders by location. |
| `isLinkedToSalesOrder` | boolean | no | Filters based on whether a manufacturing order is linked to a sales order or not. |
| `includeDeleted` | boolean | no | Soft-deleted data is excluded from result set by default. Set to true to include it. |
| `createdAtMin` | string | no | Minimum value for created_at range. Must be compatible with ISO 8601 format |
| `createdAtMax` | string | no | Maximum value for created_at range. Must be compatible with ISO 8601 format |
| `updatedAtMin` | string | no | Minimum value for updated_at range. Must be compatible with ISO 8601 format |
| `updatedAtMax` | string | no | Maximum value for updated_at range. Must be compatible with ISO 8601 format |

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

Through the native Katana API, this operation is `GET /manufacturing_orders` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-manufacturing-orders.md) for the provider-specific parameters and requirements.


# Katana: List Purchase Orders

Lists purchase orders in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-purchase-orders?${params}`, {
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
| `ids[]` | array<number> | no | Filters purchase orders by an array of IDs |
| `orderNo` | string | no | Filters purchase orders by an order number |
| `entityType` | string | no | Filters purchase orders by an entity type |
| `status` | string | no | Filters purchase orders by a status |
| `billingStatus` | string | no | Filters purchase orders by a billing status |
| `currency` | string | no | Filters purchase orders by a currency |
| `locationId` | number | no | Filters purchase orders by a location |
| `trackingLocationId` | number | no | Filters purchase orders by a tracking location |
| `supplierId` | number | no | Filters purchase orders by a supplier |
| `extend[]` | array<string> | no | Array of objects that need to be added to the response |
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
      "additionalInfo": "string",
      "billingStatus": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultGroupId": 1,
      "deletedAt": "string",
      "entityType": "string",
      "expectedArrivalDate": "string",
      "id": 1,
      "ingredientAvailability": "string",
      "ingredientExpectedDate": "string",
      "lastDocumentStatus": "string",
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "purchaseOrderRows": [
        {
          "batchTransactions": [
            {
              "batchId": 1,
              "quantity": 1
            }
          ],
          "conversionDate": "string",
          "conversionRate": 1,
          "createdAt": "string",
          "currency": "string",
          "deletedAt": "string",
          "groupId": 1,
          "id": 1,
          "landedCost": "string",
          "pricePerUnit": 1,
          "purchaseOrderId": 1,
          "purchaseUom": "string",
          "purchaseUomConversionRate": 1,
          "quantity": 1,
          "receivedDate": "string",
          "taxRateId": 1,
          "total": 1,
          "totalInBaseCurrency": 1,
          "updatedAt": "string",
          "variantId": 1
        }
      ],
      "status": "string",
      "supplier": {
        "comment": "string",
        "createdAt": "string",
        "currency": "string",
        "deletedAt": "string",
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "updatedAt": "string"
      },
      "supplierId": 1,
      "total": 1,
      "totalInBaseCurrency": 1,
      "trackingLocationId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string |  |
| `billingStatus` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultGroupId` | number |  |
| `deletedAt` | string |  |
| `entityType` | string |  |
| `expectedArrivalDate` | string |  |
| `id` | number |  |
| `ingredientAvailability` | string |  |
| `ingredientExpectedDate` | string |  |
| `lastDocumentStatus` | string |  |
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `purchaseOrderRows` | array<object> |  |
| `purchaseOrderRows[].batchTransactions` | array<object> |  |
| `purchaseOrderRows[].batchTransactions[].batchId` | number |  |
| `purchaseOrderRows[].batchTransactions[].quantity` | number |  |
| `purchaseOrderRows[].conversionDate` | string |  |
| `purchaseOrderRows[].conversionRate` | number |  |
| `purchaseOrderRows[].createdAt` | string |  |
| `purchaseOrderRows[].currency` | string |  |
| `purchaseOrderRows[].deletedAt` | string |  |
| `purchaseOrderRows[].groupId` | number |  |
| `purchaseOrderRows[].id` | number |  |
| `purchaseOrderRows[].landedCost` | string |  |
| `purchaseOrderRows[].pricePerUnit` | number |  |
| `purchaseOrderRows[].purchaseOrderId` | number |  |
| `purchaseOrderRows[].purchaseUom` | string |  |
| `purchaseOrderRows[].purchaseUomConversionRate` | number |  |
| `purchaseOrderRows[].quantity` | number |  |
| `purchaseOrderRows[].receivedDate` | string |  |
| `purchaseOrderRows[].taxRateId` | number |  |
| `purchaseOrderRows[].total` | number |  |
| `purchaseOrderRows[].totalInBaseCurrency` | number |  |
| `purchaseOrderRows[].updatedAt` | string |  |
| `purchaseOrderRows[].variantId` | number |  |
| `status` | string |  |
| `supplier` | object |  |
| `supplier.comment` | string |  |
| `supplier.createdAt` | string |  |
| `supplier.currency` | string |  |
| `supplier.deletedAt` | string |  |
| `supplier.email` | string |  |
| `supplier.id` | number |  |
| `supplier.name` | string |  |
| `supplier.updatedAt` | string |  |
| `supplierId` | number |  |
| `total` | number |  |
| `totalInBaseCurrency` | number |  |
| `trackingLocationId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `GET /purchase_orders` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-purchase-orders.md) for the provider-specific parameters and requirements.


# Katana: List Inventory Movements

Lists inventory movements in your Katana account.

```
GET https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-inventory-movements
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-inventory-movements?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/katana/latest/actions/list-inventory-movements?${params}`, {
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
| `ids[]` | array<number> | no | Filters inventory movements by an array of IDs |
| `variantIds[]` | array<number> | no | Filters inventory movements by an array of variant ids |
| `locationId` | number | no | Filters inventory movements by a location_id |
| `resourceType` | string | no | Filters inventory movements by a resource type |
| `resourceId` | number | no | Filters inventory movements by a resource_id |
| `causedByOrderNo` | string | no | Filters inventory movements by a caused_by_order_no |
| `causedByResourceId` | number | no | Filters inventory movements by a caused_by_resource_id |
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
      "averageCostAfter": 1,
      "balanceAfter": 1,
      "causedByOrderNo": "string",
      "causedByResourceId": 1,
      "createdAt": "string",
      "id": 1,
      "locationId": 1,
      "movementDate": "string",
      "quantityChange": 1,
      "rank": 1,
      "resourceId": 1,
      "resourceType": "string",
      "updatedAt": "string",
      "valueInStockAfter": 1,
      "valuePerUnit": 1,
      "variantId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `averageCostAfter` | number |  |
| `balanceAfter` | number |  |
| `causedByOrderNo` | string |  |
| `causedByResourceId` | number |  |
| `createdAt` | string |  |
| `id` | number |  |
| `locationId` | number |  |
| `movementDate` | string |  |
| `quantityChange` | number |  |
| `rank` | number |  |
| `resourceId` | number |  |
| `resourceType` | string |  |
| `updatedAt` | string |  |
| `valueInStockAfter` | number |  |
| `valuePerUnit` | number |  |
| `variantId` | number |  |

## Native endpoint

Through the native Katana API, this operation is `GET /inventory_movements` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-movements.md) for the provider-specific parameters and requirements.


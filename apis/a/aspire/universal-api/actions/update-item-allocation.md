# Aspire: Update Item Allocation



```
PUT https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-item-allocation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Aspire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-item-allocation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ItemAllocationId": 1,
  "InventoryLocationID": 1,
  "CatalogItemID": 1,
  "WorkTicketID": 1,
  "Quantity": "string",
  "AllocationDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aspire/latest/actions/update-item-allocation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ItemAllocationId": 1,
    "InventoryLocationID": 1,
    "CatalogItemID": 1,
    "WorkTicketID": 1,
    "Quantity": "string",
    "AllocationDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ItemAllocationId` | list<number> | yes |  |
| `InventoryLocationID` | list<number> | yes |  |
| `CatalogItemID` | list<number> | yes |  |
| `WorkTicketID` | list<number> | yes |  |
| `Quantity` | string | yes |  |
| `AllocationDate` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Aspire API returns.

## Native endpoint

Through the native Aspire API, this operation is `PUT ItemAllocations` (base URL `https://{{credentials.environment}}.youraspire.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item-allocation.md) for the provider-specific parameters and requirements.


# Dukaan: Update Inventory

Updates inventory quantities in Dukaan.

```
PUT https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/update-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dukaan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/update-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inventoryItemUuid": "inventory-item-uuid",
  "inventoryList[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dukaan/latest/actions/update-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inventoryItemUuid": "inventory-item-uuid",
    "inventoryList[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inventoryItemUuid` | string | yes | Inventory item UUID from Dukaan inventory data. Example: `inventory-item-uuid`. |
| `inventoryList[]` | array<object> | yes | Warehouse inventory quantity updates. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "inventory_list": [
        {}
      ],
      "modified_at": "2026-05-07T12:00:00.000Z",
      "quantity_available": 1,
      "uuid": "string",
      "warehouse": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Inventory item ID |
| `inventory_list` | array<object> | Updated inventory quantities by warehouse |
| `modified_at` | date | Last modified timestamp |
| `quantity_available` | number | Available quantity |
| `uuid` | string | Inventory item UUID |
| `warehouse` | number | Warehouse ID |

## Native endpoint

Through the native Dukaan API, this operation is `PATCH api/store/seller/seller-warehouse-inventory/:inventoryItemUuid/` (base URL `https://api.mydukaan.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory.md) for the provider-specific parameters and requirements.


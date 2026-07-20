# Cerbo: Update Inventory

Updates an existing inventory item in Cerbo.

```
PUT https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/update-inventory', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The inventory item ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Name of the inventory item |
| `nickname` | string | no | Short nickname |
| `charge_id` | number | no | ID of the associated charge |
| `preferred_stock_level` | number | no | Target stock level |
| `current_quantity` | number | no | Current quantity in stock |
| `preferred_restock_level` | number | no | Restock trigger level |
| `manufacturer` | string | no | Manufacturer name |
| `expiration_date` | date | no | Expiration date (must be in the future) |
| `lot_number` | string | no | Lot number |
| `discontinued` | boolean | no | Whether item is discontinued |
| `date_discontinued` | date | no | Discontinuation date |
| `external_identifier` | string | no | External system identifier |
| `location` | string | no | Location name |
| `package_properties` | object | no | Package-specific properties (only provided fields are updated) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "current_quantity": 1,
      "id": 1,
      "linked_product_id": 1,
      "linked_product_type": "https://example.com",
      "name": "Ava Chen",
      "preferred_stock_level": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge_id` | number |  |
| `created` | date |  |
| `current_quantity` | number |  |
| `id` | number |  |
| `linked_product_id` | number |  |
| `linked_product_type` | string |  |
| `name` | string |  |
| `preferred_stock_level` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `PATCH /inventory/:id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory.md) for the provider-specific parameters and requirements.


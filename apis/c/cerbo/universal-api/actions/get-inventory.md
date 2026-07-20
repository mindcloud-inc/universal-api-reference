# Cerbo: Get Inventory

Retrieves inventory item details from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-inventory?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/get-inventory?${params}`, {
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
| `id` | number | yes | The inventory item ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `include_deleted` | boolean | no | Set to true to retrieve soft-deleted items. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "current_quantity": 1,
      "discontinued": true,
      "expiration_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "linked_product_id": 1,
      "linked_product_type": "https://example.com",
      "lot_number": "string",
      "manufacturer": "string",
      "name": "Ava Chen",
      "nickname": "Ava Chen",
      "package_properties": {},
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
| `discontinued` | boolean |  |
| `expiration_date` | date |  |
| `id` | number |  |
| `linked_product_id` | number |  |
| `linked_product_type` | string |  |
| `lot_number` | string |  |
| `manufacturer` | string |  |
| `name` | string |  |
| `nickname` | string |  |
| `package_properties` | object |  |
| `preferred_stock_level` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /inventory/:id` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory.md) for the provider-specific parameters and requirements.


# Cerbo: List Inventory

Retrieves inventory records from Cerbo.

```
GET https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/list-inventory?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | no | Filter by inventory type (e.g., "Drug (RX)", "General"). Uses partial matching. |
| `manufacturer` | string | no | Filter by manufacturer name. Uses partial matching. |
| `include_deleted` | string | no | Set to the string 'true' to include soft-deleted items. Other values are ignored. |
| `include_discontinued` | string | no | Set to the string 'true' to include discontinued items. Other values are ignored. |

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
| `preferred_stock_level` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `GET /inventory` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory.md) for the provider-specific parameters and requirements.


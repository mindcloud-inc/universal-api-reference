# Cratejoy: List Inventory Levels

Retrieves inventory levels from Cratejoy.

```
GET https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-inventory-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cratejoy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-inventory-levels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cratejoy/latest/actions/list-inventory-levels?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "confidence": 1,
      "id": 1,
      "out_of_stock_purchases": true,
      "product_id": 1,
      "product_instance_id": 1,
      "quantity_on_hand": 1,
      "track_inventory": true,
      "type": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidence` | number |  |
| `id` | number |  |
| `out_of_stock_purchases` | boolean |  |
| `product_id` | number |  |
| `product_instance_id` | number |  |
| `quantity_on_hand` | number |  |
| `track_inventory` | boolean |  |
| `type` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Cratejoy API, this operation is `GET /v1/inventory/` (base URL `https://api.cratejoy.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-inventory-levels.md) for the provider-specific parameters and requirements.


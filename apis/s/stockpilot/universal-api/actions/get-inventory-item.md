# Stockpilot: Get Inventory Item

Retrieves an inventory item from Stockpilot.

```
GET https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-inventory-item?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/get-inventory-item?${params}`, {
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
| `id` | number | no | Inventory item ID Example: `769555`. |
| `sku` | string | no | Inventory SKU Example: `COD-INV-20260401-1738`. |
| `barcode` | string | no | Inventory barcode Example: `5901234123458`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "barcode": "string",
      "id": 1,
      "is_active": true,
      "item_name": "Ava Chen",
      "product_id": 1,
      "quantity": 1,
      "sku": "string",
      "stock_threshold": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `barcode` | string | Inventory barcode |
| `id` | number | Inventory item ID |
| `is_active` | boolean | Whether the item is active |
| `item_name` | string | Inventory item name |
| `product_id` | number | Parent product ID |
| `quantity` | number | Available quantity |
| `sku` | string | Inventory SKU |
| `stock_threshold` | number | Configured stock threshold |

## Native endpoint

Through the native Stockpilot API, this operation is `GET /inventory/get` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inventory-item.md) for the provider-specific parameters and requirements.


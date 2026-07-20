# Stockpilot: Update Inventory Item

Updates an existing inventory item in Stockpilot.

```
PUT https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/update-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/update-inventory-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/update-inventory-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | no | Internal Stockpilot product ID Example: `769555`. |
| `itemName` | string | no | Name of the item Example: `Codex Inventory Item 20260401 1738`. |
| `sku` | string | no | Stock Keeping Unit Example: `COD-INV-20260401-1738`. |
| `barcode` | string | no | Product barcode (EAN) Example: `5901234123458`. |
| `quantity` | number | no | Stock quantity Example: `11`. |
| `basePrice` | number | no | Base price Example: `26`. |
| `retailPrice` | number | no | Retail price |
| `purchasePrice` | number | no | Purchase price |
| `wholesalePrice` | number | no | Wholesale price |
| `salePrice` | number | no | Sale price |
| `weight` | string | no | Weight as string |
| `length` | number | no | Length |
| `width` | number | no | Width |
| `height` | number | no | Height |
| `vatClass` | string | no | VAT class name |
| `condition` | string | no | Condition |
| `stockThreshold` | number | no | Minimum stock threshold for alerts |
| `moq` | number | no | Minimum order quantity |
| `assignBinLocation` | string | no | Assign bin location Example: `A1-001-01`. |
| `removeBinLocation` | string | no | Remove bin location |
| `threshold` | string | no | Threshold using format like 5u or 33w Example: `5u`. |
| `isActive` | boolean | no | Is the product active |

## Response

```json
{
  "success": true,
  "data": [
    {
      "product_id": 1,
      "sku": "string",
      "updated_fields": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `product_id` | number |  |
| `sku` | string |  |
| `updated_fields` | array<string> |  |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /inventory/update` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inventory-item.md) for the provider-specific parameters and requirements.


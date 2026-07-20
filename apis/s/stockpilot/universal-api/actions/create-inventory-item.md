# Stockpilot: Create Inventory Item

Creates a new inventory item in Stockpilot.

```
POST https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-inventory-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stockpilot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-inventory-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "660724",
  "sku": "COD-INV-20260401",
  "itemName": "Codex Inventory Item 20260401",
  "barcode": "5901234123457"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stockpilot/latest/actions/create-inventory-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "660724",
    "sku": "COD-INV-20260401",
    "itemName": "Codex Inventory Item 20260401",
    "barcode": "5901234123457"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | Product database ID Example: `660724`. |
| `sku` | string | yes | Stock keeping unit Example: `COD-INV-20260401`. |
| `itemName` | string | yes | Inventory item name Example: `Codex Inventory Item 20260401`. |
| `barcode` | string | yes | Item barcode Example: `5901234123457`. |
| `barcodeType` | string | no | Barcode type Default: `EAN`. |
| `quantity` | number | no | Available quantity Default: `10`. |
| `moq` | number | no | Minimum order quantity Default: `1`. |
| `stockThreshold` | number | no | Minimum stock threshold Default: `2`. |
| `purchasePrice` | number | no | Purchase price Default: `12.5`. |
| `wholesalePrice` | number | no | Wholesale price Default: `18.5`. |
| `basePrice` | number | no | Base price Default: `25`. |
| `weight` | string | no | Weight value Default: `0.5`. |
| `length` | number | no | Item length Default: `10`. |
| `width` | number | no | Item width Default: `5`. |
| `height` | number | no | Item height Default: `3`. |
| `condition` | string | no | Item condition Default: `NEW`. |
| `vatClass` | string | no | VAT class Default: `standard_rate`. |
| `isActive` | boolean | no | Whether the item is active Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item_id": 1,
      "sku": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item_id` | number | Created Stockpilot inventory item ID |
| `sku` | string | Inventory SKU |

## Native endpoint

Through the native Stockpilot API, this operation is `POST /inventory/create` (base URL `https://api.stockpilot.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inventory-item.md) for the provider-specific parameters and requirements.


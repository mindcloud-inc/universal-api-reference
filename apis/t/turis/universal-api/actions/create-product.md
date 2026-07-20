# Turis: Create Product

Creates a new product in Turis.

```
POST https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "case_quantity": 1,
  "category_id": 1,
  "category_ids[]": [
    1
  ],
  "name": "Ava Chen",
  "sku": "string",
  "stock": 1,
  "unit_cost": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "case_quantity": 1,
    "category_id": 1,
    "category_ids[]": [1],
    "name": "Ava Chen",
    "sku": "string",
    "stock": 1,
    "unit_cost": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `case_quantity` | number | yes | Case quantity for the product. |
| `category_id` | list<number> | yes | Primary category ID. |
| `category_ids[]` | array<number> | yes | Product category IDs. |
| `currentPrice[].currency_id` | number | no | Currency for the current price. |
| `currentPrice[].price` | number | no | Current price amount. |
| `is_product_free` | boolean | no | Whether the product is free. |
| `is_shown` | boolean | no | Whether the product is shown. |
| `name` | string | yes | Product name. |
| `recommendedRetailPrice[].currency_id` | number | no | Currency for the recommended retail price. |
| `recommendedRetailPrice[].price` | number | no | Recommended retail price amount. |
| `sku` | string | yes | Product SKU. |
| `stock` | number | yes | Initial stock quantity. |
| `supplier` | string | no | Product supplier. |
| `unit_cost` | number | yes | Unit cost of the product. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brandId": 1,
      "ean": "string",
      "hsCode": "string",
      "id": 1,
      "inheritPricesVariantId": "string",
      "name": "Ava Chen",
      "sku": "string",
      "supplier": "string",
      "unitCost": 1,
      "variantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brandId` | number |  |
| `ean` | string |  |
| `hsCode` | string |  |
| `id` | number |  |
| `inheritPricesVariantId` | string |  |
| `name` | string |  |
| `sku` | string |  |
| `supplier` | string |  |
| `unitCost` | number |  |
| `variantId` | string |  |

## Native endpoint

Through the native Turis API, this operation is `POST /api/public/v1/products` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.


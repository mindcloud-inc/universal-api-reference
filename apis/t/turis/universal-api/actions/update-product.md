# Turis: Update Product

Updates an existing product in Turis.

```
PUT https://connect.mindcloud.co/v1/universal/turis/latest/actions/update-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/turis/latest/actions/update-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turis/latest/actions/update-product', {
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
      "variantId": 1
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
| `variantId` | number |  |

## Native endpoint

Through the native Turis API, this operation is `PATCH /api/public/v1/products/:productId` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product.md) for the provider-specific parameters and requirements.


# Turis: List Products

Retrieves products from Turis.

```
GET https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Turis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turis/latest/actions/list-products?${params}`, {
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

Through the native Turis API, this operation is `GET /api/public/v1/products` (base URL `https://{{credentials.tenant}}.turis.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.


# Kladana: List Products

Lists products in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-products?${params}`, {
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
      "archived": true,
      "article": "string",
      "barcodes": [
        {}
      ],
      "buyPrice": {},
      "code": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "externalCode": "string",
      "id": "string",
      "meta": {},
      "minPrice": {},
      "name": "Ava Chen",
      "pathName": "Ava Chen",
      "productFolder": {},
      "salePrices": [
        {}
      ],
      "shared": true,
      "uom": {},
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the product is archived. |
| `article` | string | Product article or SKU. |
| `barcodes` | array<object> | Product barcodes. |
| `buyPrice` | object | Buy price. |
| `code` | string | Internal code. |
| `created` | date | Creation timestamp. |
| `description` | string | Product description. |
| `externalCode` | string | External code. |
| `id` | string | Product UUID. |
| `meta` | object | Kladana metadata reference. |
| `minPrice` | object | Minimum sale price. |
| `name` | string | Product name. |
| `pathName` | string | Folder path name. |
| `productFolder` | object | Product folder reference. |
| `salePrices` | array<object> | Sale prices. |
| `shared` | boolean | Whether the product is shared. |
| `uom` | object | Unit of measure. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/product` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.


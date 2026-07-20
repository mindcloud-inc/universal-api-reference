# Kladana: Get Product

Retrieves a product record from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product?connectionId=$CONNECTION_ID&id=7944ef04-f831-11e5-7a69-971500188b19" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "7944ef04-f831-11e5-7a69-971500188b19"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-product?${params}`, {
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
| `id` | string | yes | Kladana product ID from the Product resource URL. Example: `7944ef04-f831-11e5-7a69-971500188b19`. |

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

Through the native Kladana API, this operation is `GET /entity/product/{id}` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.


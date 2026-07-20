# Sumtracker: List Products

Retrieves products from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-products?${params}`, {
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
| `barcode` | string | no | Product barcode. |
| `name` | string | no | Product name. |
| `sku` | string | no | Product SKU. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "name": "Ava Chen",
          "sku": "string",
          "variantName": "Ava Chen",
          "barcode": "string",
          "bundleType": "string",
          "uom": "string",
          "created": "2026-05-07T12:00:00.000Z",
          "updated": "2026-05-07T12:00:00.000Z",
          "wavgLandedCost": "string",
          "notes": "string",
          "imageUrl": "https://example.com",
          "categories": {},
          "tags": {},
          "id": 1
        }
      ],
      "count": 1,
      "next": "string",
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].name` | string |  |
| `results[].sku` | string |  |
| `results[].variantName` | string |  |
| `results[].barcode` | string |  |
| `results[].bundleType` | string |  |
| `results[].uom` | string |  |
| `results[].created` | date |  |
| `results[].updated` | date |  |
| `results[].wavgLandedCost` | string |  |
| `results[].notes` | string |  |
| `results[].imageUrl` | string |  |
| `results[].categories` | object |  |
| `results[].tags` | object |  |
| `results[].id` | number |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/products/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.


# Sumtracker: List Stock Levels

Retrieves stock levels from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-levels?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-levels?${params}`, {
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
| `cursor` | string | no | Cursor returned by the previous 2025-11 stock-level response. |
| `product` | number | no | Product ID. Either product or warehouse is required by Sumtracker. |
| `warehouse` | number | no | Warehouse ID. Either warehouse or product is required by Sumtracker. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "id": 1,
          "updated": "2026-05-07T12:00:00.000Z",
          "productId": 1,
          "product": {
            "id": 1,
            "created": "2026-05-07T12:00:00.000Z",
            "updated": "2026-05-07T12:00:00.000Z",
            "name": "Ava Chen",
            "sku": "string",
            "variantName": "Ava Chen",
            "barcode": "string",
            "categories": [
              "string"
            ],
            "tags": [
              "string"
            ],
            "imageUrl": "https://example.com",
            "notes": "string",
            "bundleType": "string",
            "wavgLandedCost": "string",
            "uom": "string"
          },
          "warehouseId": 1,
          "inStock": 1,
          "incoming": 1,
          "available": 1,
          "booked": 1
        }
      ],
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
| `results[].id` | number |  |
| `results[].updated` | date |  |
| `results[].productId` | number |  |
| `results[].product.id` | number |  |
| `results[].product.created` | date |  |
| `results[].product.updated` | date |  |
| `results[].product.name` | string |  |
| `results[].product.sku` | string |  |
| `results[].product.variantName` | string |  |
| `results[].product.barcode` | string |  |
| `results[].product.categories` | array<string> |  |
| `results[].product.tags` | array<string> |  |
| `results[].product.imageUrl` | string |  |
| `results[].product.notes` | string |  |
| `results[].product.bundleType` | string |  |
| `results[].product.wavgLandedCost` | string |  |
| `results[].product.uom` | string |  |
| `results[].warehouseId` | number |  |
| `results[].inStock` | number |  |
| `results[].incoming` | number |  |
| `results[].available` | number |  |
| `results[].booked` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-11/stock/levels/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-levels.md) for the provider-specific parameters and requirements.


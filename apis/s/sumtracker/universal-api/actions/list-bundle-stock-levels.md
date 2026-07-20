# Sumtracker: List Bundle Stock Levels

Retrieves bundle stock levels from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-bundle-stock-levels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-bundle-stock-levels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-bundle-stock-levels?${params}`, {
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
| `cursor` | string | no | Cursor returned by the previous 2025-11 bundle stock-level response. |
| `product` | number | no | Bundle product ID. |
| `warehouse` | number | no | Warehouse ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "product": {
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
            "categories": [
              "string"
            ],
            "tags": [
              "string"
            ],
            "id": 1
          },
          "components": [
            {
              "product": {
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
                "categories": [
                  "string"
                ],
                "tags": {},
                "id": 1
              },
              "inStock": 1,
              "available": 1,
              "booked": 1,
              "componentQuantity": 1,
              "possibleBundles": 1,
              "id": 1,
              "productId": 1,
              "warehouseId": 1
            }
          ],
          "inStock": 1,
          "available": 1,
          "booked": 1,
          "id": 1,
          "productId": 1,
          "warehouseId": 1
        }
      ],
      "next": {},
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].product.name` | string |  |
| `results[].components[].product.name` | string |  |
| `results[].product.sku` | string |  |
| `results[].product.variantName` | string |  |
| `results[].product.barcode` | string |  |
| `results[].components[].product.sku` | string |  |
| `results[].components[].product.variantName` | string |  |
| `results[].components[].product.barcode` | string |  |
| `results[].product.bundleType` | string |  |
| `results[].product.uom` | string |  |
| `results[].components[].product.bundleType` | string |  |
| `results[].components[].product.uom` | string |  |
| `results[].product.created` | date |  |
| `results[].product.updated` | date |  |
| `results[].components[].product.created` | date |  |
| `results[].components[].product.updated` | date |  |
| `results[].inStock` | number |  |
| `results[].available` | number |  |
| `results[].booked` | number |  |
| `results[].components[].inStock` | number |  |
| `results[].components[].available` | number |  |
| `results[].components[].booked` | number |  |
| `results[].components[].componentQuantity` | number |  |
| `results[].components[].possibleBundles` | number |  |
| `results[].product.wavgLandedCost` | string |  |
| `results[].components[].product.wavgLandedCost` | string |  |
| `results[].product.notes` | string |  |
| `results[].components[].product.notes` | string |  |
| `results[].product.imageUrl` | string |  |
| `results[].product.categories[]` | string |  |
| `results[].product.tags[]` | string |  |
| `results[].components[].product.imageUrl` | string |  |
| `results[].components[].product.categories[]` | string |  |
| `results[].components[].product.tags` | object |  |
| `results[].id` | number |  |
| `results[].productId` | number |  |
| `results[].warehouseId` | number |  |
| `results[].product.id` | number |  |
| `results[].components[].product.id` | number |  |
| `results[].components[].id` | number |  |
| `results[].components[].productId` | number |  |
| `results[].components[].warehouseId` | number |  |
| `next` | object |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-11/stock/levels/bundles/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bundle-stock-levels.md) for the provider-specific parameters and requirements.


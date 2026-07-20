# Sumtracker: List Bundle Components

Retrieves bundle components from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-bundle-components
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-bundle-components?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-bundle-components?${params}`, {
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
      "results": [
        {
          "component": {
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
          "quantity": 1,
          "id": 1,
          "productId": 1,
          "componentId": 1
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
| `results[].component.name` | string |  |
| `results[].component.sku` | string |  |
| `results[].component.variantName` | string |  |
| `results[].component.barcode` | string |  |
| `results[].component.bundleType` | string |  |
| `results[].component.uom` | string |  |
| `results[].component.created` | date |  |
| `results[].component.updated` | date |  |
| `results[].quantity` | number |  |
| `results[].component.wavgLandedCost` | string |  |
| `results[].component.notes` | string |  |
| `results[].component.imageUrl` | string |  |
| `results[].component.categories[]` | string |  |
| `results[].component.tags` | object |  |
| `results[].id` | number |  |
| `results[].productId` | number |  |
| `results[].componentId` | number |  |
| `results[].component.id` | number |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/products/bundles/lines/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bundle-components.md) for the provider-specific parameters and requirements.


# Sumtracker: List Stock Adjustment Document Lines

Retrieves stock adjustment document lines from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-adjustment-document-lines
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-adjustment-document-lines?connectionId=$CONNECTION_ID&limit=25&offset=0&document_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "document_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-stock-adjustment-document-lines?${params}`, {
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
| `document_id` | string | yes | Stock adjustment document ID. |

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
          "adjustmentType": "string",
          "isComplete": true,
          "created": "2026-05-07T12:00:00.000Z",
          "quantity": 1,
          "id": 1,
          "productId": 1,
          "warehouseId": 1,
          "documentId": 1,
          "reason": "string"
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
| `results[].product.name` | string |  |
| `results[].product.sku` | string |  |
| `results[].product.variantName` | string |  |
| `results[].product.barcode` | string |  |
| `results[].adjustmentType` | string |  |
| `results[].isComplete` | boolean |  |
| `results[].product.bundleType` | string |  |
| `results[].product.uom` | string |  |
| `results[].created` | date |  |
| `results[].product.created` | date |  |
| `results[].product.updated` | date |  |
| `results[].quantity` | number |  |
| `results[].product.wavgLandedCost` | string |  |
| `results[].product.notes` | string |  |
| `results[].product.imageUrl` | string |  |
| `results[].product.categories[]` | string |  |
| `results[].product.tags[]` | string |  |
| `results[].id` | number |  |
| `results[].productId` | number |  |
| `results[].warehouseId` | number |  |
| `results[].documentId` | number |  |
| `results[].product.id` | number |  |
| `results[].reason` | string |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/stock/adjustment/documents/:document_id/lines/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-stock-adjustment-document-lines.md) for the provider-specific parameters and requirements.


# Fourthwall: List Products

Retrieves a paginated list of products from Fourthwall.

```
GET https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/list-products?${params}`, {
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
| `search` | string | no | Search products by keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {
        "type": "string"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "images": [
        {
          "height": 1,
          "id": "string",
          "transformedUrl": "https://example.com",
          "url": "https://example.com",
          "width": 1
        }
      ],
      "name": "Ava Chen",
      "slug": "string",
      "state": {
        "type": "string"
      },
      "thumbnailImage": {
        "height": 1,
        "id": "string",
        "transformedUrl": "https://example.com",
        "url": "https://example.com",
        "width": 1
      },
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "variants": [
        {
          "attributes": {
            "description": "string"
          },
          "dimensions": {
            "height": 1,
            "length": 1,
            "unit": "string",
            "width": 1
          },
          "id": "string",
          "images": [
            {
              "height": 1,
              "id": "string",
              "transformedUrl": "https://example.com",
              "url": "https://example.com",
              "width": 1
            }
          ],
          "name": "Ava Chen",
          "sku": "string",
          "stock": {
            "type": "string"
          },
          "thumbnailImage": {
            "height": 1,
            "id": "string",
            "transformedUrl": "https://example.com",
            "url": "https://example.com",
            "width": 1
          },
          "unitCost": {
            "currency": "string",
            "value": 1
          },
          "unitPrice": {
            "currency": "string",
            "value": 1
          },
          "weight": {
            "unit": "string",
            "value": 1
          }
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access.type` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `images[].height` | number |  |
| `images[].id` | string |  |
| `images[].transformedUrl` | string |  |
| `images[].url` | string |  |
| `images[].width` | number |  |
| `name` | string |  |
| `slug` | string |  |
| `state.type` | string |  |
| `thumbnailImage.height` | number |  |
| `thumbnailImage.id` | string |  |
| `thumbnailImage.transformedUrl` | string |  |
| `thumbnailImage.url` | string |  |
| `thumbnailImage.width` | number |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `variants[].attributes.description` | string |  |
| `variants[].dimensions.height` | number |  |
| `variants[].dimensions.length` | number |  |
| `variants[].dimensions.unit` | string |  |
| `variants[].dimensions.width` | number |  |
| `variants[].id` | string |  |
| `variants[].images[].height` | number |  |
| `variants[].images[].id` | string |  |
| `variants[].images[].transformedUrl` | string |  |
| `variants[].images[].url` | string |  |
| `variants[].images[].width` | number |  |
| `variants[].name` | string |  |
| `variants[].sku` | string |  |
| `variants[].stock.type` | string |  |
| `variants[].thumbnailImage.height` | number |  |
| `variants[].thumbnailImage.id` | string |  |
| `variants[].thumbnailImage.transformedUrl` | string |  |
| `variants[].thumbnailImage.url` | string |  |
| `variants[].thumbnailImage.width` | number |  |
| `variants[].unitCost.currency` | string |  |
| `variants[].unitCost.value` | number |  |
| `variants[].unitPrice.currency` | string |  |
| `variants[].unitPrice.value` | number |  |
| `variants[].weight.unit` | string |  |
| `variants[].weight.value` | number |  |

## Native endpoint

Through the native Fourthwall API, this operation is `GET /open-api/v1.0/products` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.


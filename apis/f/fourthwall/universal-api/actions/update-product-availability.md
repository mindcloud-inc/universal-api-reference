# Fourthwall: Update Product Availability

Updates a product's storefront availability in Fourthwall.

```
PUT https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/update-product-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fourthwall `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/update-product-availability" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": "string",
  "available": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fourthwall/latest/actions/update-product-availability', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": "string",
    "available": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | string | yes | The product ID. |
| `available` | boolean | yes | Whether the product should be available for sale. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access": {
        "type": "string"
      },
      "additionalInformation": {
        "guaranteeAndReturns": "string"
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
| `additionalInformation.guaranteeAndReturns` | string |  |
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

Through the native Fourthwall API, this operation is `PUT /open-api/v1.0/products/:productId/availability` (base URL `https://api.fourthwall.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-product-availability.md) for the provider-specific parameters and requirements.


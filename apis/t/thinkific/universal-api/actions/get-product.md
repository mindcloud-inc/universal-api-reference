# Thinkific: Get Product

Retrieves a product record from Thinkific.

```
GET https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-product?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-product?${params}`, {
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
| `id` | number | yes | Product identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cardImageUrl": "https://example.com",
      "collectionIds": [
        1
      ],
      "createdAt": "string",
      "daysUntilExpiry": 1,
      "description": "string",
      "hasCertificate": true,
      "hidden": true,
      "id": 1,
      "keywords": "string",
      "name": "Ava Chen",
      "position": 1,
      "price": 1,
      "private": true,
      "productableId": 1,
      "productableType": "string",
      "productPrices": [
        {}
      ],
      "relatedProductIds": [
        1
      ],
      "seoDescription": "string",
      "seoTitle": "string",
      "slug": "string",
      "status": "string",
      "subscription": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cardImageUrl` | string |  |
| `collectionIds` | array<number> |  |
| `createdAt` | string |  |
| `daysUntilExpiry` | number |  |
| `description` | string |  |
| `hasCertificate` | boolean |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `keywords` | string |  |
| `name` | string |  |
| `position` | number |  |
| `price` | number |  |
| `private` | boolean |  |
| `productableId` | number |  |
| `productableType` | string |  |
| `productPrices` | array<object> |  |
| `relatedProductIds` | array<number> |  |
| `seoDescription` | string |  |
| `seoTitle` | string |  |
| `slug` | string |  |
| `status` | string |  |
| `subscription` | boolean |  |

## Native endpoint

Through the native Thinkific API, this operation is `GET /products/:id` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-product.md) for the provider-specific parameters and requirements.


# Omnisend: Create Product

Creates a new product in Omnisend.

```
POST https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "url": "https://example.com",
  "variants[].id": "string",
  "variants[].status": "string",
  "variants[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "url": "https://example.com",
    "variants[].id": "string",
    "variants[].status": "string",
    "variants[].url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `categoryIDs[]` | array<string> | no |  |
| `createdAt` | date | no |  |
| `currency` | string | no |  |
| `defaultImageUrl` | string | no |  |
| `description` | string | no |  |
| `id` | string | yes |  |
| `images[]` | array<string> | no |  |
| `status` | string | no |  |
| `tags[]` | array<string> | no |  |
| `title` | string | no |  |
| `type` | string | no |  |
| `updatedAt` | date | no |  |
| `url` | string | yes |  |
| `variants[]` | array<object> | no |  |
| `variants[].defaultImageUrl` | string | no |  |
| `variants[].description` | string | no |  |
| `variants[].id` | string | yes |  |
| `variants[].images[]` | array<string> | no |  |
| `variants[].price` | number | no |  |
| `variants[].sku` | string | no |  |
| `variants[].status` | string | yes | Required per verified runtime. Use one of: inStock, outOfStock, notAvailable. |
| `variants[].strikeThroughPrice` | number | no |  |
| `variants[].title` | string | no |  |
| `variants[].url` | string | yes |  |
| `vendor` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `POST /v5/products` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.


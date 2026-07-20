# Omnisend: Replace Product

Replaces an existing product in Omnisend.

```
PUT https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/replace-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Omnisend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/replace-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "productID": "string",
  "url": "https://example.com",
  "variants[].id": "string",
  "variants[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnisend/latest/actions/replace-product', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "productID": "string",
    "url": "https://example.com",
    "variants[].id": "string",
    "variants[].url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `currency` | string | no |  |
| `id` | string | yes |  |
| `productID` | string | yes | Unique Omnisend product identifier. |
| `status` | string | no |  |
| `title` | string | no |  |
| `url` | string | yes |  |
| `variants[]` | array<object> | no |  |
| `variants[].defaultImageUrl` | string | no |  |
| `variants[].description` | string | no |  |
| `variants[].id` | string | yes |  |
| `variants[].images[]` | array<string> | no |  |
| `variants[].price` | number | no |  |
| `variants[].sku` | string | no |  |
| `variants[].status` | string | no |  |
| `variants[].strikeThroughPrice` | number | no |  |
| `variants[].title` | string | no |  |
| `variants[].url` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Omnisend API returns.

## Native endpoint

Through the native Omnisend API, this operation is `PUT /v5/products/:productID` (base URL `https://api.omnisend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-product.md) for the provider-specific parameters and requirements.


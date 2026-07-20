# Modelry: Create Product



```
POST https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-product
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modelry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "product.title": "string",
  "product.sku": "string",
  "product.description": "string",
  "product.batchId": "string",
  "product.tags[]": [
    "string"
  ],
  "product.dimensions": "string",
  "product.externalUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "product.title": "string",
    "product.sku": "string",
    "product.description": "string",
    "product.batchId": "string",
    "product.tags[]": ["string"],
    "product.dimensions": "string",
    "product.externalUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `product.title` | string | yes | Product title from Modelry docs. |
| `product.sku` | string | yes | Unique product SKU. |
| `product.description` | string | yes | Product description. |
| `product.batchId` | string | yes | Modeling batch identifier. |
| `product.tags[]` | array<string> | yes | Array of product tags. |
| `product.dimensions` | string | yes | Product dimensions string. |
| `product.externalUrl` | string | yes | External product URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "batchId": "string",
        "createdAt": "string",
        "description": "string",
        "sku": "string",
        "tags": [
          "string"
        ],
        "title": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.batchId` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.description` | string |  |
| `attributes.sku` | string |  |
| `attributes.tags[]` | string |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Modelry API, this operation is `POST /v1/products` (base URL `https://api.modelry.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product.md) for the provider-specific parameters and requirements.


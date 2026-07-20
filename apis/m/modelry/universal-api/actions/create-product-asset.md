# Modelry: Create Product Asset



```
POST https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-product-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modelry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-product-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "blobId": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/modelry/latest/actions/create-product-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "blobId": "string",
    "tags[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | Modelry product ID. |
| `blobId` | string | yes | Signed blob ID from upload. |
| `tags[]` | array<string> | yes | Asset tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "byteSize": 1,
        "createdAt": "string",
        "fileName": "Ava Chen",
        "tags": [
          "string"
        ],
        "type": "string",
        "url": "https://example.com"
      },
      "id": "string",
      "relationships": {
        "modelingRequest": {
          "data": {}
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.byteSize` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.fileName` | string |  |
| `attributes.tags[]` | string |  |
| `attributes.type` | string |  |
| `attributes.url` | string |  |
| `id` | string |  |
| `relationships.modelingRequest.data` | object |  |
| `type` | string |  |

## Native endpoint

Through the native Modelry API, this operation is `POST /v1/products/:product_id/assets` (base URL `https://api.modelry.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-product-asset.md) for the provider-specific parameters and requirements.


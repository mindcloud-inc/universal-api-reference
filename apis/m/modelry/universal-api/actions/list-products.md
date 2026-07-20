# Modelry: List Products



```
GET https://connect.mindcloud.co/v1/universal/modelry/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Modelry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/modelry/latest/actions/list-products?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/modelry/latest/actions/list-products?${params}`, {
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
      "attributes": {
        "batchId": {},
        "createdAt": "string",
        "description": "string",
        "sku": "string",
        "sourceLabel": "string",
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
| `attributes.batchId` | object |  |
| `attributes.createdAt` | string |  |
| `attributes.description` | string |  |
| `attributes.sku` | string |  |
| `attributes.sourceLabel` | string |  |
| `attributes.tags[]` | string |  |
| `attributes.title` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Modelry API, this operation is `GET /v1/products` (base URL `https://api.modelry.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.


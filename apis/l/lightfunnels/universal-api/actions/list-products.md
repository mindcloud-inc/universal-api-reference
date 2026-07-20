# Lightfunnels: List Products



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-products?${params}`, {
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
      "products": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "id": "string",
              "name": "Ava Chen",
              "slug": "string"
            }
          }
        ],
        "pageInfo": {
          "endCursor": "string",
          "hasNextPage": true
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `products` | object | Product connection. |
| `products.edges` | array<object> | Product edges. |
| `products.edges[].cursor` | string | Pagination cursor. |
| `products.edges[].node` | object | Product node. |
| `products.edges[].node.id` | string | Product id. |
| `products.edges[].node.name` | string | Product name. |
| `products.edges[].node.slug` | string | Product slug. |
| `products.pageInfo` | object | Pagination info. |
| `products.pageInfo.endCursor` | string | Last cursor. |
| `products.pageInfo.hasNextPage` | boolean | Whether more products exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-products.md) for the provider-specific parameters and requirements.


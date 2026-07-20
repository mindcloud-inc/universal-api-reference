# Lightfunnels: List Orders



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-orders?${params}`, {
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
      "orders": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "createdAt": "string",
              "id": "string",
              "name": "Ava Chen",
              "total": 1
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
| `orders` | object | Order connection. |
| `orders.edges` | array<object> | Order edges. |
| `orders.edges[].cursor` | string | Pagination cursor. |
| `orders.edges[].node` | object | Order node. |
| `orders.edges[].node.createdAt` | string | Order creation timestamp. |
| `orders.edges[].node.id` | string | Order id. |
| `orders.edges[].node.name` | string | Order name. |
| `orders.edges[].node.total` | number | Order total. |
| `orders.pageInfo` | object | Pagination info. |
| `orders.pageInfo.endCursor` | string | Last cursor. |
| `orders.pageInfo.hasNextPage` | boolean | Whether more orders exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.


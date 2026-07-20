# Nautical: List Orders

Retrieves a list of orders from Nautical.

```
GET https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nautical `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nautical/latest/actions/list-orders?${params}`, {
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
      "data": {
        "orders": {
          "edges": [
            {
              "node": {
                "created": "string",
                "id": "string",
                "number": "string",
                "status": "string"
              }
            }
          ],
          "pageInfo": {
            "endCursor": "string",
            "hasNextPage": true
          }
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
| `data.orders.edges[].node.created` | string | Order created timestamp. |
| `data.orders.edges[].node.id` | string | Order id. |
| `data.orders.edges[].node.number` | string | Order number. |
| `data.orders.edges[].node.status` | string | Order status. |
| `data.orders.pageInfo.endCursor` | string | Cursor for the next page. |
| `data.orders.pageInfo.hasNextPage` | boolean | Whether another page exists. |

## Native endpoint

Through the native Nautical API, this operation is `POST graphql/` (base URL `https://api.mpconsole.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.


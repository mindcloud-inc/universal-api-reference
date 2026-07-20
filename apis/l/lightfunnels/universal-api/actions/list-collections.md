# Lightfunnels: List Collections



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-collections?${params}`, {
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
      "collections": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "id": "string",
              "name": "Ava Chen"
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
| `collections` | object | Collection connection. |
| `collections.edges` | array<object> | Collection edges. |
| `collections.edges[].cursor` | string | Pagination cursor. |
| `collections.edges[].node` | object | Collection node. |
| `collections.edges[].node.id` | string | Collection id. |
| `collections.edges[].node.name` | string | Collection name. |
| `collections.pageInfo` | object | Pagination info. |
| `collections.pageInfo.endCursor` | string | Last cursor. |
| `collections.pageInfo.hasNextPage` | boolean | Whether more collections exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-collections.md) for the provider-specific parameters and requirements.


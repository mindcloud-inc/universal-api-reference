# Lightfunnels: List Funnels



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-funnels
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-funnels?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-funnels?${params}`, {
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
      "funnels": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "id": "string",
              "name": "Ava Chen",
              "published": true,
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
| `funnels` | object | Funnel connection. |
| `funnels.edges` | array<object> | Funnel edges. |
| `funnels.edges[].cursor` | string | Pagination cursor. |
| `funnels.edges[].node` | object | Funnel node. |
| `funnels.edges[].node.id` | string | Funnel id. |
| `funnels.edges[].node.name` | string | Funnel name. |
| `funnels.edges[].node.published` | boolean | Whether the funnel is published. |
| `funnels.edges[].node.slug` | string | Funnel slug. |
| `funnels.pageInfo` | object | Pagination info. |
| `funnels.pageInfo.endCursor` | string | Last cursor. |
| `funnels.pageInfo.hasNextPage` | boolean | Whether more funnels exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-funnels.md) for the provider-specific parameters and requirements.


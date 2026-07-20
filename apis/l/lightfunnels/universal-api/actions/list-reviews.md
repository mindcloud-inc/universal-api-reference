# Lightfunnels: List Reviews



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-reviews?${params}`, {
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
      "reviews": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "id": "string",
              "name": "Ava Chen",
              "published": true,
              "rate": 1
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
| `reviews` | object | Review connection. |
| `reviews.edges` | array<object> | Review edges. |
| `reviews.edges[].cursor` | string | Pagination cursor. |
| `reviews.edges[].node` | object | Review node. |
| `reviews.edges[].node.id` | string | Review id. |
| `reviews.edges[].node.name` | string | Reviewer name. |
| `reviews.edges[].node.published` | boolean | Whether the review is published. |
| `reviews.edges[].node.rate` | number | Review rating. |
| `reviews.pageInfo` | object | Pagination info. |
| `reviews.pageInfo.endCursor` | string | Last cursor. |
| `reviews.pageInfo.hasNextPage` | boolean | Whether more reviews exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.


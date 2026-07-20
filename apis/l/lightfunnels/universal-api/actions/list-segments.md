# Lightfunnels: List Segments



```
GET https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-segments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-segments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/list-segments?${params}`, {
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
      "segments": {
        "edges": [
          {
            "cursor": "string",
            "node": {
              "description": "string",
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
| `segments` | object | Segment connection. |
| `segments.edges` | array<object> | Segment edges. |
| `segments.edges[].cursor` | string | Pagination cursor. |
| `segments.edges[].node` | object | Segment node. |
| `segments.edges[].node.description` | string | Segment description. |
| `segments.edges[].node.id` | string | Segment id. |
| `segments.edges[].node.name` | string | Segment name. |
| `segments.pageInfo` | object | Pagination info. |
| `segments.pageInfo.endCursor` | string | Last cursor. |
| `segments.pageInfo.hasNextPage` | boolean | Whether more segments exist. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segments.md) for the provider-specific parameters and requirements.


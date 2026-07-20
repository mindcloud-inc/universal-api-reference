# Curator: List Posts

Retrieves posts for a feed in Curator.

```
GET https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Curator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-posts?connectionId=$CONNECTION_ID&feedId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "feedId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/curator/latest/actions/list-posts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedId` | string | yes | ID of the feed whose posts should be listed. |
| `limit` | number | no | Optional page size. |
| `after` | string | no | Pagination cursor for the next page. |
| `before` | string | no | Pagination cursor for the previous page. |
| `networkId` | number | no | Optional network filter. |
| `sourceType` | number | no | Optional source type filter. |
| `status` | string | no | Optional post status filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {}
      ],
      "cache": {},
      "networks": [
        1
      ],
      "pagination": {},
      "postCount": 1,
      "posts": [
        {}
      ],
      "sources": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> |  |
| `cache` | object |  |
| `networks` | array<number> |  |
| `pagination` | object |  |
| `postCount` | number |  |
| `posts` | array<object> |  |
| `sources` | array<object> |  |
| `success` | boolean |  |

## Native endpoint

Through the native Curator API, this operation is `GET /v1/feeds/:FEED_ID/posts` (base URL `https://api.curator.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.


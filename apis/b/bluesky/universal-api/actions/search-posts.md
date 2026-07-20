# Bluesky: Search Posts

Finds Bluesky posts matching a search query.

```
GET https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/search-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bluesky `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/search-posts?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bluesky/latest/actions/search-posts?${params}`, {
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
| `q` | string | yes | Search text for matching posts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cursor": "string",
      "hitsTotal": 1,
      "posts": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cursor` | string |  |
| `hitsTotal` | number |  |
| `posts` | array<object> |  |

## Native endpoint

Through the native Bluesky API, this operation is `GET /xrpc/app.bsky.feed.searchPosts` (base URL `{{credentials.pdsUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-posts.md) for the provider-specific parameters and requirements.


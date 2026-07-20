# Tophhie Cloud: List Blog Posts

Retrieves blog posts from Tophhie Cloud.

```
GET https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/list-blog-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tophhie Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/list-blog-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tophhieCloud/latest/actions/list-blog-posts?${params}`, {
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
| `page` | number | no | Specific page from the results. Default: `1`. |
| `limit` | number | no | Number of posts to return. Default: `15`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "next_page": "https://example.com",
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
| `next_page` | string | URL for the next page of posts. |
| `posts` | array<object> | Blog post rows. |

## Native endpoint

Through the native Tophhie Cloud API, this operation is `GET /blog/posts` (base URL `https://api.tophhie.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blog-posts.md) for the provider-specific parameters and requirements.


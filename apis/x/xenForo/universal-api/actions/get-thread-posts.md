# XenForo: Get Thread Posts

Retrieves posts from a thread in XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-thread-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-thread-posts?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-thread-posts?${params}`, {
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
| `id` | number | yes | ID of the thread whose posts should be returned. Example: `123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "current_page": 1,
        "total": 1
      },
      "posts": [
        {
          "message": "string",
          "post_date": 1,
          "post_id": 1,
          "thread_id": 1,
          "user_id": 1,
          "username": "Ava Chen",
          "view_url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.current_page` | number |  |
| `pagination.total` | number |  |
| `posts` | array<object> |  |
| `posts[].message` | string |  |
| `posts[].post_date` | number |  |
| `posts[].post_id` | number |  |
| `posts[].thread_id` | number |  |
| `posts[].user_id` | number |  |
| `posts[].username` | string |  |
| `posts[].view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /threads/:id/posts` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread-posts.md) for the provider-specific parameters and requirements.


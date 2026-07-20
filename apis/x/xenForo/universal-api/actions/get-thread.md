# XenForo: Get Thread

Retrieves the specified thread from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-thread?connectionId=$CONNECTION_ID&id=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-thread?${params}`, {
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
| `id` | number | yes | ID of the thread to retrieve. Example: `123`. |
| `withPosts` | boolean | no | If true, include a page of posts with the thread response. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `withFirstPost` | boolean | no | If true, include the first post in the thread response. |
| `withLastPost` | boolean | no | If true, include the last post in the thread response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "current_page": 1
      },
      "posts": [
        {
          "message": "string",
          "post_id": 1,
          "thread_id": 1,
          "username": "Ava Chen"
        }
      ],
      "thread": {
        "node_id": 1,
        "reply_count": 1,
        "thread_id": 1,
        "title": "string",
        "username": "Ava Chen",
        "view_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.current_page` | number |  |
| `posts` | array<object> |  |
| `posts[].message` | string |  |
| `posts[].post_id` | number |  |
| `posts[].thread_id` | number |  |
| `posts[].username` | string |  |
| `thread.node_id` | number |  |
| `thread.reply_count` | number |  |
| `thread.thread_id` | number |  |
| `thread.title` | string |  |
| `thread.username` | string |  |
| `thread.view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /threads/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-thread.md) for the provider-specific parameters and requirements.


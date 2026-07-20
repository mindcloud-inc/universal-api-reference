# XenForo: Get Forum Threads

Retrieves a page of forum threads from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-forum-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-forum-threads?connectionId=$CONNECTION_ID&id=2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-forum-threads?${params}`, {
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
| `id` | number | yes | ID of the forum whose threads should be returned. Example: `2`. |
| `unread` | boolean | no | Filters to unread threads only. Ignored for guests. |

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
      "threads": [
        {
          "last_post_date": 1,
          "node_id": 1,
          "post_date": 1,
          "reply_count": 1,
          "thread_id": 1,
          "title": "string",
          "username": "Ava Chen",
          "view_count": 1,
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
| `threads` | array<object> |  |
| `threads[].last_post_date` | number |  |
| `threads[].node_id` | number |  |
| `threads[].post_date` | number |  |
| `threads[].reply_count` | number |  |
| `threads[].thread_id` | number |  |
| `threads[].title` | string |  |
| `threads[].username` | string |  |
| `threads[].view_count` | number |  |
| `threads[].view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /forums/:id/threads` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-forum-threads.md) for the provider-specific parameters and requirements.


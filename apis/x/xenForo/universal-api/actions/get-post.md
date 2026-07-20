# XenForo: Get Post

Retrieves the specified post from XenForo.

```
GET https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-post?connectionId=$CONNECTION_ID&id=456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/get-post?${params}`, {
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
| `id` | number | yes | ID of the post to retrieve. Example: `456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "post": {
        "message": "string",
        "post_date": 1,
        "post_id": 1,
        "thread_id": 1,
        "user_id": 1,
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
| `post.message` | string |  |
| `post.post_date` | number |  |
| `post.post_id` | number |  |
| `post.thread_id` | number |  |
| `post.user_id` | number |  |
| `post.username` | string |  |
| `post.view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `GET /posts/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.


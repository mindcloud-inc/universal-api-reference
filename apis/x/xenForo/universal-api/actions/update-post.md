# XenForo: Update Post

Updates an existing post in XenForo.

```
PUT https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the post to update. Example: `456`. |
| `message` | string | no | Updated post message body. Example: `Updated post body.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `silent` | boolean | no | If true and permissions allow, this edit will not show a last edited indication. |

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
      },
      "success": true
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
| `success` | boolean |  |

## Native endpoint

Through the native XenForo API, this operation is `POST /posts/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.


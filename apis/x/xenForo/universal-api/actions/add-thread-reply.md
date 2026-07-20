# XenForo: Add Thread Reply

Creates a reply post in XenForo.

```
POST https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/add-thread-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/add-thread-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "threadId": "123",
  "message": "Thanks for the update."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/add-thread-reply', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "threadId": "123",
    "message": "Thanks for the update."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `threadId` | number | yes | ID of the thread to reply to. Example: `123`. |
| `message` | string | yes | Reply message body. Example: `Thanks for the update.`. |

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

Through the native XenForo API, this operation is `POST /posts/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-thread-reply.md) for the provider-specific parameters and requirements.


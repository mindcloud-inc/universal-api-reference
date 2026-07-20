# XenForo: Update Thread

Updates an existing thread in XenForo.

```
PUT https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/update-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/update-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/update-thread', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the thread to update. Example: `123`. |
| `title` | string | no | New thread title. Example: `Updated thread title`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `discussionOpen` | boolean | no | Whether the thread should be open for replies. |
| `sticky` | boolean | no | Whether the thread should be sticky. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true,
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
| `success` | boolean |  |
| `thread.node_id` | number |  |
| `thread.reply_count` | number |  |
| `thread.thread_id` | number |  |
| `thread.title` | string |  |
| `thread.username` | string |  |
| `thread.view_url` | string |  |

## Native endpoint

Through the native XenForo API, this operation is `POST /threads/:id/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-thread.md) for the provider-specific parameters and requirements.


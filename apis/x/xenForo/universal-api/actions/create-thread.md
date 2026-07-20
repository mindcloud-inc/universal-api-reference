# XenForo: Create Thread

Creates a new thread in XenForo.

```
POST https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/create-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a XenForo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/create-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nodeId": "2",
  "title": "Welcome to our community",
  "message": "Introduce the topic here."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/xenForo/latest/actions/create-thread', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nodeId": "2",
    "title": "Welcome to our community",
    "message": "Introduce the topic here."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nodeId` | number | yes | ID of the forum to create the thread in. Example: `2`. |
| `title` | string | yes | Title of the thread. Example: `Welcome to our community`. |
| `message` | string | yes | Body of the first post in the thread. Example: `Introduce the topic here.`. |

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

Through the native XenForo API, this operation is `POST /threads/` (base URL `{{credentials.baseUrl}}/2310/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-thread.md) for the provider-specific parameters and requirements.


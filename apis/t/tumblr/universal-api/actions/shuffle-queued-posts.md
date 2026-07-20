# Tumblr: Shuffle Queued Posts

Shuffles queued posts in a Tumblr blog.

```
PUT https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/shuffle-queued-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/shuffle-queued-posts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blogIdentifier": "mindcloudapps"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/shuffle-queued-posts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blogIdentifier": "mindcloudapps"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blogIdentifier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blogIdentifier` | string |  |

## Native endpoint

Through the native Tumblr API, this operation is `POST /v2/blog/:blogIdentifier/posts/queue/shuffle` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/shuffle-queued-posts.md) for the provider-specific parameters and requirements.


# Tumblr: Reorder Queued Posts

Reorders queued posts in a Tumblr blog.

```
PUT https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/reorder-queued-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/reorder-queued-posts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blogIdentifier": "mindcloudapps",
  "postId": "1772822948"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/reorder-queued-posts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blogIdentifier": "mindcloudapps",
    "postId": "1772822948"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `blogIdentifier` | string | yes | Any Tumblr blog identifier for the target blog. Example: `mindcloudapps`. |
| `postId` | string | yes | ID of the queued post to move. Example: `1772822948`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `insertAfter` | string | no | Queued post ID to move the post after, or 0 to move it to the top. Default: `0`. Example: `0`. |

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

Through the native Tumblr API, this operation is `POST /v2/blog/:blogIdentifier/posts/queue/reorder` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reorder-queued-posts.md) for the provider-specific parameters and requirements.


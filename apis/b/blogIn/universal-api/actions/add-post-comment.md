# BlogIn: Add Post Comment

Adds a comment to a BlogIn post.

```
POST https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/add-post-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/add-post-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "text": "string",
  "author.id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/add-post-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "text": "string",
    "author.id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the post to comment on. |
| `text` | string | yes | The HTML text of the comment. |
| `author.id` | number | yes | The ID of the author of the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approved": true,
      "approved_at": "string",
      "author": {},
      "created_at": "string",
      "id": 1,
      "parent": 1,
      "text": "string",
      "votes_down": 1,
      "votes_up": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approved` | boolean |  |
| `approved_at` | string |  |
| `author` | object |  |
| `created_at` | string |  |
| `id` | number |  |
| `parent` | number |  |
| `text` | string |  |
| `votes_down` | number |  |
| `votes_up` | number |  |

## Native endpoint

Through the native BlogIn API, this operation is `POST /posts/:id/comments` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-post-comment.md) for the provider-specific parameters and requirements.


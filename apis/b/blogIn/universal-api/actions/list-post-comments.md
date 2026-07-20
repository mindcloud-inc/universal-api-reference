# BlogIn: List Post Comments

Retrieves comments for a BlogIn post.

```
GET https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-post-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BlogIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-post-comments?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blogIn/latest/actions/list-post-comments?${params}`, {
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
| `id` | number | yes | The ID of the post whose comments to list. |

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

Through the native BlogIn API, this operation is `GET /posts/:id/comments` (base URL `https://blogin.co/api/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-comments.md) for the provider-specific parameters and requirements.


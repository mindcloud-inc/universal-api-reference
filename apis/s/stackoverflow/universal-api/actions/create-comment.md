# Stackoverflow: Create Comment

Creates a new comment in Stackoverflow.

```
POST https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "comment_id": 1,
      "post_id": 1,
      "score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `comment_id` | number |  |
| `post_id` | number |  |
| `score` | number |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `POST /posts/[:id]/comments/add` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.


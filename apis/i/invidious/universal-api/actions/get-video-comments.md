# Invidious: Get Video Comments



```
GET https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invidious `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-comments?connectionId=$CONNECTION_ID&id=dQw4w9WgXcQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "dQw4w9WgXcQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-video-comments?${params}`, {
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
| `continuation` | string | no | Continuation token for the next chunk of comments. |
| `id` | string | yes | Video ID to fetch comments for. Example: `dQw4w9WgXcQ`. |
| `sortBy` | string | no | Comment sort order: top or new. |
| `source` | string | no | Comment source: youtube or reddit. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentCount": 1,
      "comments": [
        {}
      ],
      "continuation": "string",
      "videoId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentCount` | number |  |
| `comments` | array<object> |  |
| `continuation` | string |  |
| `videoId` | string |  |

## Native endpoint

Through the native Invidious API, this operation is `GET /comments/:id` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-comments.md) for the provider-specific parameters and requirements.


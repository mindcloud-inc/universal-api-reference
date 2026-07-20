# YouTube: List Comments

Retrieves comments or replies from YouTube.

```
GET https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouTube `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "part": "snippet"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-comments?${params}`, {
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
| `part` | string | yes | Comma-separated comment resource parts to include. Default: `snippet`. |
| `parentId` | string | no | Retrieve replies for a top-level comment ID. |
| `id` | string | no | Comma-separated list of comment IDs. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `textFormat` | string | no | Comment text format, html or plainText. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "etag": "string",
      "id": "string",
      "kind": "string",
      "snippet": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string |  |
| `id` | string |  |
| `kind` | string |  |
| `snippet` | object |  |

## Native endpoint

Through the native YouTube API, this operation is `GET /youtube/v3/comments` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-comments.md) for the provider-specific parameters and requirements.


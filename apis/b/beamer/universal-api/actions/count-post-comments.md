# Beamer: Count Post Comments

Retrieves a post comment count from Beamer.

```
GET https://connect.mindcloud.co/v1/universal/beamer/latest/actions/count-post-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beamer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beamer/latest/actions/count-post-comments?connectionId=$CONNECTION_ID&postId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beamer/latest/actions/count-post-comments?${params}`, {
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
| `postId` | number | yes |  |
| `dateFrom` | string | no |  |
| `dateTo` | string | no |  |
| `language` | string | no |  |
| `search` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Beamer API returns.

## Native endpoint

Through the native Beamer API, this operation is `GET /v0/posts/:postId/comments/count` (base URL `https://api.getbeamer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-post-comments.md) for the provider-specific parameters and requirements.


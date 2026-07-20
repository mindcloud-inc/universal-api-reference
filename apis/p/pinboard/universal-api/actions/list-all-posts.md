# Pinboard: List All Posts



```
GET https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-all-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-all-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-all-posts?${params}`, {
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
| `fromdt` | date | no | Return bookmarks created after this time. |
| `meta` | boolean | no | Include change detection metadata. |
| `results` | number | no | Number of results to return. |
| `start` | number | no | Offset value. |
| `tag` | string | no | Filter by up to three tags. |
| `todt` | date | no | Return bookmarks created before this time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "extended": "string",
      "hash": "string",
      "href": "string",
      "meta": "string",
      "shared": "string",
      "tags": "string",
      "time": "2026-05-07T12:00:00.000Z",
      "toread": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Bookmark title. |
| `extended` | string | Extended description or notes. |
| `hash` | string | Bookmark hash. |
| `href` | string | Bookmark URL. |
| `meta` | string | Change detection signature when requested. |
| `shared` | string | Public visibility flag returned by Pinboard. |
| `tags` | string | Space-delimited bookmark tags. |
| `time` | date | Bookmark creation timestamp. |
| `toread` | string | Unread flag returned by Pinboard. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /posts/all` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-posts.md) for the provider-specific parameters and requirements.


# Pinboard: List Posts



```
GET https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinboard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-posts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinboard/latest/actions/list-posts?${params}`, {
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
| `dt` | date | no | Return results bookmarked on this day. |
| `meta` | boolean | no | Include change detection metadata. |
| `tag` | string | no | Filter by up to three tags. |
| `url` | string | no | Return the bookmark for this URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "posts": [
        {}
      ],
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Timestamp for the response payload. |
| `posts` | array<object> | Matching bookmarks. |
| `user` | string | Pinboard username. |

## Native endpoint

Through the native Pinboard API, this operation is `GET /posts/get` (base URL `https://api.pinboard.in/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.


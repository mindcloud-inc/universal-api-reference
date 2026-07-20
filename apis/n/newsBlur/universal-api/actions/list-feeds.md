# NewsBlur: List Feeds

Retrieves subscribed feeds from NewsBlur.

```
GET https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NewsBlur `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newsBlur/latest/actions/list-feeds?${params}`, {
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
| `includeFavicons` | boolean | no | Include favicons inline in the feeds response. |
| `flat` | boolean | no | Return a flat folder structure instead of nested folders. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `updateCounts` | boolean | no | Force recalculation of unread counts on all feeds. This can slow the request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authenticated": true,
      "categories": [
        "string"
      ],
      "feeds": {},
      "flat_folders": {},
      "folders": [
        {}
      ],
      "inactive_feeds": [
        1
      ],
      "result": "string",
      "social_feeds": {},
      "social_profile": {},
      "starred_count": 1,
      "user": {},
      "user_id": 1,
      "user_profile": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authenticated` | boolean | Whether the session is authenticated. |
| `categories` | array<string> | NewsBlur feed categories. |
| `feeds` | object | Subscribed feeds keyed by feed ID. |
| `flat_folders` | object | Flattened folder lookup. |
| `folders` | array<object> | Folder tree. |
| `inactive_feeds` | array<number> | Inactive feed IDs. |
| `result` | string | Result status. |
| `social_feeds` | object | Social feeds keyed by ID. |
| `social_profile` | object | Social profile for the authenticated user. |
| `starred_count` | number | Total saved story count. |
| `user` | object | Authenticated user summary. |
| `user_id` | number | Authenticated NewsBlur user ID. |
| `user_profile` | object | Authenticated user profile. |

## Native endpoint

Through the native NewsBlur API, this operation is `GET /reader/feeds` (base URL `https://www.newsblur.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feeds.md) for the provider-specific parameters and requirements.

